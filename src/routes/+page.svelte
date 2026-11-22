<script lang="ts">
  const instagramUrl = 'https://www.instagram.com/renovando_uy/';
  const whatsappUrl = 'https://wa.me/59895713304';
  const services = [
    {
      title: 'Instalación y mantenimiento de aire acondicionado',
      desc: 'Instalación profesional, mantenimiento preventivo y correctivo para climatizar tus espacios con eficiencia energética.',
      img: '/ac.jpg'
    },
    {
      title: 'Obras en yeso',
      desc: 'Cielorrasos, tabiques y detalles en yeso con terminaciones prolijas y duraderas para renovar tus ambientes.',
      img: '/oy.jpg'
    },
    {
      title: 'Refrigeración automotriz',
      desc: 'Carga de gas, diagnóstico y reparación del aire acondicionado de tu vehículo para un confort óptimo.',
      img: '/rf.jpg'
    },
    {
      title: 'Electricidad residencial',
      desc: 'Instalaciones, mejoras y mantenimiento eléctrico con enfoque en seguridad, normativa y eficiencia.',
      img: '/er.webp'
    },
    {
      title: 'Instalación de cámaras de seguridad',
      desc: 'Montaje y configuración de CCTV para hogares y comercios, con asesoramiento personalizado.',
      img: '/cs.jpeg'
    }
  ];
</script>

<section class="relative h-[70vh] min-h-[480px] w-full overflow-hidden">
  <img
    src="/ia.jpg"
    alt="Trabajos técnicos y mantenimiento"
    class="absolute inset-0 h-full w-full object-cover"
    loading="eager"
    fetchpriority="high"
  />
  <div class="absolute inset-0 bg-black/50"></div>
  <div class="relative z-10 mx-auto flex h-full max-w-6xl flex-col items-center justify-center px-4 text-center text-white">
    <img src="/logo.jpeg" alt="renovando.uy" class="mb-6 h-16 w-auto drop-shadow" />
    <h1 class="text-3xl font-semibold md:text-5xl">renovando.uy</h1>
    <h2 class="text-2xl font-semibold md:text-2xl">tu confort, nuestra misión</h2>
    <p class="mt-3 max-w-2xl text-base md:text-lg">Servicios de instalación y mantenimiento para tu hogar y empresa.</p>
    <div class="mt-6 flex flex-wrap items-center justify-center gap-3">
      <a href={whatsappUrl} target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 rounded bg-green-500 px-5 py-3 font-medium text-white hover:bg-green-600 focus:outline-none focus:ring-2 focus:ring-green-300">
        <img src="https://cdn.simpleicons.org/whatsapp/FFFFFF" alt="WhatsApp" class="h-5 w-5" />
        <span>Escribinos por WhatsApp</span>
      </a>
      <a href={instagramUrl} target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 rounded bg-white/10 px-5 py-3 font-medium text-white backdrop-blur hover:bg-white/20 focus:outline-none focus:ring-2 focus:ring-white/40">
        <img src="https://cdn.simpleicons.org/instagram/FFFFFF" alt="Instagram" class="h-5 w-5" />
        <span>Instagram</span>
      </a>
    </div>
  </div>
</section>

<section id="servicios" class="mx-auto max-w-6xl px-4 py-12">
  <h2 class="mb-6 text-2xl font-semibold md:text-3xl">Servicios</h2>
  <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
    {#each services as service}
      <article class="overflow-hidden rounded-xl border bg-white shadow-sm">
        <img src={service.img} alt={service.title} class="h-40 w-full object-cover" loading="lazy" />
        <div class="p-4">
          <h3 class="text-lg font-semibold">{service.title}</h3>
          {#if service.desc}
            <p class="mt-1 text-sm text-gray-600">{service.desc}</p>
          {/if}
        </div>
      </article>
    {/each}
  </div>
</section>

<section id="sobre-nosotros" class="mx-auto max-w-6xl px-4 py-12">
  <h2 class="mb-4 text-2xl font-semibold md:text-3xl">Sobre nosotros</h2>
  <p class="max-w-3xl text-gray-700">
    Somos un emprendimiento radicado en <strong>Solís de Mataojo, Uruguay</strong>, brindando
    servicios para todo <strong>Canelones, Maldonado, Lavalleja y Montevideo</strong>. Nos capacitamos bajo los más
    altos estándares y cada trabajo se realiza con <strong>garantía de satisfacción</strong>.
  </p>
</section>

<section id="contacto" class="bg-gray-50 py-12">
  <div class="mx-auto max-w-6xl px-4">
    <h2 class="mb-4 text-2xl font-semibold md:text-3xl">Contacto</h2>
    <p class="mb-6 max-w-2xl text-gray-700">Estamos para ayudarte. Coordiná una visita o pedí tu presupuesto hoy.</p>
    <div class="flex flex-wrap gap-3">
      <a href={whatsappUrl} target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 rounded bg-green-500 px-5 py-3 font-medium text-white hover:bg-green-600 focus:outline-none focus:ring-2 focus:ring-green-300" aria-label="Abrir WhatsApp">
        <img src="https://cdn.simpleicons.org/whatsapp/FFFFFF" alt="WhatsApp" class="h-5 w-5" />
        <span>+598 95 713 304</span>
      </a>
      <a href={instagramUrl} target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 rounded bg-pink-600 px-5 py-3 font-medium text-white hover:bg-pink-700 focus:outline-none focus:ring-2 focus:ring-pink-300" aria-label="Abrir Instagram">
        <img src="https://cdn.simpleicons.org/instagram/FFFFFF" alt="Instagram" class="h-5 w-5" />
        <span>@renovando_uy</span>
      </a>
    </div>
  </div>
</section>

<footer class="border-t py-8">
  <div class="mx-auto flex max-w-6xl items-center justify-between px-4">
    <span class="text-sm text-gray-600">© renovando.uy {new Date().getFullYear()}</span>
    <a class="text-sm text-gray-600 hover:underline" href="#servicios">Servicios</a>
  </div>
</footer>


