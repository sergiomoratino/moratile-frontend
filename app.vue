<template>
  <div>
    <!-- Header -->
    <Header />

    <!-- Hero Section con Slider -->
    <section class="bg-gray-100 text-center">
      <h2 class="text-4xl font-bold text-gray-800 mb-4">
        Especialistas en Alicatados & Solados
      </h2>
      <p class="text-gray-600 max-w-2xl mx-auto">
        Transformamos tus espacios con acabados de calidad y atención al
        detalle.
      </p>
      <Slider />
    </section>

    <!-- Servicios -->
    <section id="services" class="py-16 bg-white">
      <div class="container mx-auto text-center">
        <h3 class="text-3xl font-bold text-gray-800 mb-8">
          Nuestros Servicios
        </h3>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="p-6 border rounded-lg shadow-sm">
            <h4 class="text-xl font-semibold text-gray-700">
              Alicatado de Cocinas
            </h4>
            <p class="text-gray-600 mt-2">
              Diseños modernos y clásicos para cocinas únicas.
            </p>
          </div>
          <div class="p-6 border rounded-lg shadow-sm">
            <h4 class="text-xl font-semibold text-gray-700">
              Revestimiento de Baños
            </h4>
            <p class="text-gray-600 mt-2">
              Impermeabilización y estilo en cada detalle.
            </p>
          </div>
          <div class="p-6 border rounded-lg shadow-sm">
            <h4 class="text-xl font-semibold text-gray-700">
              Solados y Pavimentos
            </h4>
            <p class="text-gray-600 mt-2">
              Pisos duraderos y estéticos para cualquier espacio.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Proyectos -->
    <section id="projects" class="py-16 bg-gray-100">
      <div class="container mx-auto text-center">
        <h3 class="text-3xl font-bold text-gray-800 mb-8">
          Proyectos Recientes
        </h3>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div
            v-for="n in 6"
            :key="n"
            class="h-48 bg-gray-200 rounded-lg"
          ></div>
        </div>
      </div>
    </section>

    <!-- Contacto -->
    <section id="contact" class="py-16 bg-white">
      <div class="container mx-auto text-center">
        <h3 class="text-3xl font-bold text-gray-800 mb-4">¿Hablamos?</h3>
        <p class="text-gray-600 mb-8">
          Ponte en contacto para transformar tus espacios.
        </p>
        <button
          class="px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-500"
        >
          Contactar
        </button>
      </div>
    </section>

    <!-- Footer -->
    <Footer />
  </div>
</template>