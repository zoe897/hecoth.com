//import Image from "next/image";

export const metadata = {
  title: "Disc Blade Manufacturer | Harrow Disc Blade Supplier",
  description:
    "High wear resistant disc blade for agriculture. Boron steel, OEM supported. Fast delivery worldwide.",
};

export default function DiscBladePage() {
  return (
    <main className="font-sans">

      {/* HERO */}
      <section className="bg-green-800 text-white text-center py-20 px-6">
        <h1 className="text-4xl font-bold mb-4">
          Heavy Duty Disc Blade Manufacturer
        </h1>
        <p className="mb-6">
          Longer Lifespan | High Hardness | OEM Supported
        </p>
        <a href="#quote" className="bg-orange-500 px-6 py-3 rounded">
          Get Quote Now
        </a>
      </section>

      {/* IMAGE + VIDEO */}
      <section className="py-16 px-6 max-w-6xl mx-auto grid md:grid-cols-2 gap-10 items-center">
        
        <div>
          <Image
            src="/images/seed/discblade.jpg"
            alt="disc blade"
            width={500}
            height={400}
            className="rounded"
          />
        </div>

        <div className="w-full h-[300px] md:h-[400px]">
          <iframe
            className="w-full h-full rounded"
            src="https://youtu.be/znTKwVyMO84?si=TgOdTqFpFGG55Djq"
            title="Disc Blade Working"
            allowFullScreen
          />
        </div>

      </section>

      {/* FEATURES */}
      <section className="py-16 px-6 bg-gray-100">
        <div className="max-w-6xl mx-auto grid md:grid-cols-3 gap-6">

          <div className="p-6 bg-white rounded shadow">
            <h3 className="font-bold mb-2">Boron Steel</h3>
            <p>Stronger and more wear resistant</p>
          </div>

          <div className="p-6 bg-white rounded shadow">
            <h3 className="font-bold mb-2">Heat Treatment</h3>
            <p>Hardness up to HRC 52</p>
          </div>

          <div className="p-6 bg-white rounded shadow">
            <h3 className="font-bold mb-2">OEM Available</h3>
            <p>Custom size and design supported</p>
          </div>

        </div>
      </section>

      {/* COMPARISON */}
      <section className="py-16 px-6 max-w-6xl mx-auto">
        <h2 className="text-2xl font-bold mb-6">
          Why Choose Our Disc Blade?
        </h2>

        <table className="w-full border">
          <thead>
            <tr className="bg-gray-200">
              <th className="p-3">Feature</th>
              <th>Our Blade</th>
              <th>Standard</th>
            </tr>
          </thead>
          <tbody>
            <tr className="text-center">
              <td className="p-3">Material</td>
              <td>Boron Steel</td>
              <td>Carbon Steel</td>
            </tr>
            <tr className="text-center">
              <td className="p-3">Hardness</td>
              <td>HRC 38–52</td>
              <td>HRC 25–35</td>
            </tr>
            <tr className="text-center">
              <td className="p-3">Lifespan</td>
              <td>Longer</td>
              <td>Short</td>
            </tr>
          </tbody>
        </table>
      </section>

      {/* FORM */}
      <section id="quote" className="py-16 px-6 bg-gray-100">
        <div className="max-w-xl mx-auto">
          <h2 className="text-2xl font-bold mb-4">Request a Quote</h2>

          <form className="flex flex-col gap-4">
            <input placeholder="Name" className="p-3 border" />
            <input placeholder="Email" className="p-3 border" />
            <textarea
              placeholder="Your requirements"
              className="p-3 border"
            />
            <button className="bg-orange-500 text-white p-3">
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