// app/products/spare-parts/disc-blade/page.tsx

import Image from "next/image";

export const metadata = {
  title: "Disc Blade Manufacturer | High Wear Resistant Agricultural Disc Blade",
  description:
    "High quality disc blade for disc harrow. Boron steel material, OEM supported, wear resistant. Fast global delivery.",
  keywords:
    "disc blade, disc harrow blade, agricultural disc blade, notched disc blade, farming disc blade",
  alternates: {
    canonical: "https://your-domain.com/disc-blade",
  },
};

export default function DiscBladePage() {
  return (
    <main className="text-gray-900">

      {/* HERO */}
      <section className="bg-green-800 text-white text-center py-20 px-6">
        <h1 className="text-4xl font-bold">
          Heavy Duty Disc Blade for Agriculture
        </h1>
        <p className="mt-4 text-lg">
          Boron Steel | Wear Resistant | OEM Supported
        </p>

        <a
          href="#quote"
          className="mt-6 inline-block bg-orange-500 px-6 py-3 rounded"
        >
          Get Quote Now
        </a>
      </section>

      {/* IMAGE + VIDEO */}
      <section className="max-w-6xl mx-auto grid md:grid-cols-2 gap-10 py-16 px-6">

        {/* IMAGE */}
        <div>
          <Image
            src="/images/seed/discblade.jpg"
            alt="disc blade agricultural"
            width={600}
            height={400}
            className="rounded"
          />
        </div>

        {/* VIDEO */}
        <div className="aspect-video w-full">
          <iframe
            className="w-full h-full rounded"
            src="https://youtu.be/znTKwVyMO84?si=gptPx-2bGt8R97nZ"
            title="Disc Blade Working Video"
            allowFullScreen
          />
        </div>

      </section>

      {/* WHAT IS DISC BLADE */}
      <section className="max-w-4xl mx-auto px-6 py-10">
        <h2 className="text-2xl font-bold mb-4">What is Disc Blade?</h2>
        <p>
          Disc blades are key components of agricultural disc harrows used for
          soil cutting, residue mixing, and land preparation.
        </p>
      </section>

      {/* FEATURES */}
      <section className="bg-gray-100 py-16 px-6">
        <div className="max-w-6xl mx-auto grid md:grid-cols-3 gap-6">

          <div className="bg-white p-6 rounded shadow">
            <h3 className="font-bold">Boron Steel Material</h3>
            <p>High strength and long service life</p>
          </div>

          <div className="bg-white p-6 rounded shadow">
            <h3 className="font-bold">Heat Treated</h3>
            <p>Hardness up to HRC 52</p>
          </div>

          <div className="bg-white p-6 rounded shadow">
            <h3 className="font-bold">OEM Custom</h3>
            <p>Size and design customization available</p>
          </div>

        </div>
      </section>

      {/* APPLICATION */}
      <section className="max-w-4xl mx-auto px-6 py-10">
        <h2 className="text-2xl font-bold mb-4">Applications</h2>
        <ul className="list-disc pl-5 space-y-2">
          <li>Soil preparation</li>
          <li>Crop residue cutting</li>
          <li>Weed control</li>
          <li>Land leveling</li>
        </ul>
      </section>

      {/* COMPARISON */}
      <section className="bg-white py-16 px-6 max-w-6xl mx-auto">
        <h2 className="text-2xl font-bold mb-6">
          Why Our Disc Blade is Better?
        </h2>

        <table className="w-full border text-center">
          <thead className="bg-gray-200">
            <tr>
              <th className="p-3">Feature</th>
              <th>Our Blade</th>
              <th>Normal Blade</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td className="p-3">Material</td>
              <td>Boron Steel</td>
              <td>Carbon Steel</td>
            </tr>
            <tr>
              <td className="p-3">Hardness</td>
              <td>HRC 45–52</td>
              <td>HRC 25–35</td>
            </tr>
            <tr>
              <td className="p-3">Lifespan</td>
              <td>Long</td>
              <td>Short</td>
            </tr>
          </tbody>
        </table>
      </section>

      {/* QUOTE FORM */}
      <section id="quote" className="bg-gray-100 py-16 px-6">
        <div className="max-w-xl mx-auto">
          <h2 className="text-2xl font-bold mb-4">Request a Quote</h2>

          <form className="flex flex-col gap-4">
            <input className="p-3 border" placeholder="Name" />
            <input className="p-3 border" placeholder="Email" />
            <input className="p-3 border" placeholder="Country" />
            <textarea
              className="p-3 border"
              placeholder="Your requirement"
            />

            <button className="bg-orange-500 text-white py-3">
              Send Inquiry
            </button>
          </form>
        </div>
      </section>

      {/* STICKY CTA */}
      <div className="fixed bottom-0 left-0 w-full bg-orange-500 text-center py-3">
        <a href="#quote" className="text-white font-bold">
          👉 Get Best Price Now
        </a>
      </div>

      {/* WHATSAPP */}
      <a
        href="https://wa.me/8619743003775"
        target="_blank"
        className="fixed bottom-20 right-5 bg-green-500 text-white p-4 rounded-full"
      >
        💬
      </a>

    </main>
  );
}