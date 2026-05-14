<template>
  <section class="hero relative min-h-[90vh] flex items-center justify-center overflow-hidden">
    <!-- 1. 背景图区域 -->
    <div class="absolute inset-0 z-0">
      <img 
        src="/img/hero-bg.jpg" 
        alt="Hecoth Agriculture & Construction Machinery" 
        class="w-full h-full object-cover"
      >
      <!-- 渐变遮罩层：从左深右浅，确保文字可读性，同时不完全遮盖机器美感 -->
      <div class="absolute inset-0 bg-gradient-to-r from-slate-900/80 via-slate-900/50 to-transparent"></div>
    </div>

    <!-- 2. 内容区域 -->
    <ClientOnly>
      <div v-scroll-group class="container mx-auto px-4 relative z-10">
        <div class="max-w-4xl">
          <!-- 小标题/欢迎语 -->
          <div class="mb-6 w-fit flex items-center gap-3 bg-white/10 border border-white/20 px-4 py-2 rounded-full backdrop-blur-md">
            <span class="w-2 h-2 rounded-full bg-green-400 animate-pulse shadow-[0_0_8px_#4ade80]"></span>
            <p class="text-white text-xs font-bold tracking-[0.2em] uppercase">
              {{ siteConfig?.hero?.welcomeText || 'Reliable Sourcing Partner Since 2009' }}
            </p>
          </div>

          <!-- 主标题：直接点出行业，建立第一印象 -->
          <h1 class="text-4xl md:text-6xl lg:text-7xl font-extrabold text-white leading-[1.1] mb-8">
            {{ siteConfig?.hero?.mainHeading || 'High-Quality Agricultural & Construction Machinery' }}
          </h1>

          <!-- 副标题：强调 16 年经验和拼箱优势 -->
          <p class="text-gray-200 text-lg md:text-xl leading-relaxed mb-12 max-w-2xl">
            {{ siteConfig?.hero?.subtitle || 'With over 16 years of industry expertise, we specialize in delivering durable machinery and spare parts with professional container consolidation services.' }}
          </p>

          <!-- 呼吁行动按钮 -->
          <div class="flex flex-col sm:flex-row gap-5 mb-16">
            <NuxtLink to="/products"
              class="bg-green-600 text-white px-8 py-4 rounded-lg hover:bg-green-700 transition-all font-bold text-center shadow-lg shadow-green-900/20">
              {{ siteConfig?.hero?.ctaButton || 'Explore Products' }}
            </NuxtLink>
            <NuxtLink to="/contact"
              class="bg-white/10 text-white border border-white/30 backdrop-blur-sm px-8 py-4 rounded-lg hover:bg-white hover:text-slate-900 transition-all font-bold text-center">
              {{ siteConfig?.hero?.secondaryButton || 'Get a Free Quote' }}
            </NuxtLink>
          </div>

          <!-- 统计数据：视觉化展示公司实力 -->
          <div class="grid grid-cols-2 md:grid-cols-4 gap-8 py-8 border-t border-white/10">
            <div class="text-left">
              <p class="text-4xl font-bold text-white mb-1">16+</p>
              <p class="text-gray-400 text-sm uppercase tracking-wider">Years Experience</p>
            </div>
            <div class="text-left">
              <p class="text-4xl font-bold text-white mb-1">30+</p>
              <p class="text-gray-400 text-sm uppercase tracking-wider">Countries Served</p>
            </div>
            <div class="text-left">
              <p class="text-4xl font-bold text-white mb-1">100%</p>
              <p class="text-gray-400 text-sm uppercase tracking-wider">Quality Inspected</p>
            </div>
            <div class="text-left">
              <div class="flex items-center gap-2">
                <Phone class="w-5 h-5 text-green-400" />
                <span class="text-xl font-bold text-white whitespace-nowrap">+86 136 5661 7631</span>
              </div>
              <p class="text-gray-400 text-sm uppercase tracking-wider mt-1">24/7 Support</p>
            </div>
          </div>
        </div>
      </div>
    </ClientOnly>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { Phone } from 'lucide-vue-next'

const siteConfig = ref<any>({})

onMounted(async () => {
  try {
    const response = await fetch('/setting.json')
    if (response.ok) {
      const data = await response.json()
      siteConfig.value = { ...siteConfig.value, ...data }
    }
  } catch (e) {
    console.warn("Setting.json not found, using default values.")
  }
})
</script>

<style scoped>
/* 针对移动端的微调 */
@media (max-width: 768px) {
  .hero {
    min-height: 100vh;
  }
}
</style>