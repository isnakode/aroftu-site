<script>
  const menus = [
    { title: "Beranda", url: "/" },
    { title: "Kursus", url: "/" },
    { title: "Harga", url: "/" },
  ];
  const courses = [
    {
      img: "dart_basic.png",
      title: "Dart pemula",
      desc: "Belajar Dart dari dasar",
    },
    {
      img: "flutter_basic.png",
      title: "Flutter pemula",
      desc: "Belajar Fluter dari dasar",
    },
    {
      img: "flutter_widget.png",
      title: "Flutter widget",
      desc: "Belajar Lebih dalam setiap widget di flutter",
    },
    {
      img: "flutter_animation.png",
      title: "Animasi di Flutter",
      desc: "Belajar Animasi agar aplikasi lebih interaktif",
    },
    {
      img: "flutter_firebase.png",
      title: "Flutter & firebase",
      desc: "Belajar integrasi Flutter dan Firebase",
    },
    {
      img: "flutter_state.png",
      title: "State management di Flutter",
      desc: "Belajar State management di Flutter",
    },
  ];
</script>

<div class="drawer">
  <input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
  <div class="drawer-content flex flex-col">
    <div class="navbar py-0 w-full">
      <div class="flex-none lg:hidden">
        <label
          for="my-drawer-3"
          aria-label="open sidebar"
          class="btn btn-square btn-ghost"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            class="inline-block h-6 w-6 stroke-current"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            ></path>
          </svg>
        </label>
      </div>
      <div class="mx-2 flex-1 px-2 font-black text-2xl">
        <span class="text-primary">Aroftu</span>
        <span class="text-secondary">Flutter</span>
      </div>
      <div class="hidden flex-none lg:block">
        <ul class="menu menu-horizontal">
          {#each menus as menu}
            <li><a class="text-lg" href={menu.url}>{menu.title}</a></li>
          {/each}
        </ul>
      </div>
    </div>
    <div class="flex flex-col items-center text-center p-8 pt-16 gap-4">
      <h1
        class="lg:text-5xl text-3xl relative uppercase md:w-1/2 leading-tight font-black"
      >
        <span
          class="absolute top-0 right-0 p-2 bg-red-400 text-lg text-white rounded-lg rotate-45"
          >Coming soon</span
        >
        Jadi developer Android dengan
        <span class="text-secondary">Flutter</span>
      </h1>
      <p class="text-lg md:w-1/2">
        Belajar Flutter dari dasar hingga bisa membuat aplikasimu sendiri
      </p>
      <button class="btn btn-primary btn-lg">Mulai belajar</button>
      <div class="p-8 rounded-xl bg-secondary w-full mt-16">
        <h2 class="text-2xl text-white font-bold mb-8">
          Belasan tutorial interaktif
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
          {#each courses as course}
            <a
              href="/"
              class="rounded-xl transition-transform hover:-translate-y-2 p-2 bg-white border-white overflow-hidden"
            >
              <img
                src="/img/{course.img}"
                class="rounded-lg"
                alt={course.title}
              />
              <div class="px-4 pb-2">
                <p class="font-bold py-2 text-lg">{course.title}</p>
                <p>{course.desc}</p>
              </div>
            </a>
          {/each}
        </div>
        <a href="/" class="mt-8 inline-block text-lg link text-white"
          >Lihat semua kursus >></a
        >
      </div>
    </div>
  </div>
  <div class="drawer-side">
    <label for="my-drawer-3" aria-label="close sidebar" class="drawer-overlay"
    ></label>
    <ul class="menu bg-base-200 min-h-full w-80 p-4">
      {#each menus as menu}
        <li><a href={menu.url}>{menu.title}</a></li>
      {/each}
    </ul>
  </div>
</div>
