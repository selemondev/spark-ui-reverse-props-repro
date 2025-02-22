<script setup lang="ts">
const packages = [
  {
    id: 1,
    name: "Vue",
    icon: "https://api.iconify.design/logos:vue.svg",
    description:
      "An approachable, performant and versatile framework for building web user interfaces.",
    link: "https://vuejs.org/",
  },

  {
    id: 2,
    name: "Pinia",
    icon: "https://api.iconify.design/logos:pinia.svg",
    description:
      "The intuitive store that is type safe, extensible, and modular by design.",
    link: "https://pinia.vuejs.org/",
  },

  {
    id: 3,
    name: "Vue Router",
    icon: "https://api.iconify.design/logos:vue.svg",
    description:
      "The expressive, configurable and convenient routing for Vue.js applications.",
    link: "https://router.vuejs.org/",
  },

  {
    id: 4,
    name: "Eslint",
    icon: "https://api.iconify.design/vscode-icons:file-type-eslint.svg",
    description:
      "ESLint is an open source project that statically analyzes your code to quickly find problems.",
    link: "https://eslint.org/",
  },

  {
    id: 5,
    name: "Vitest",
    icon: "https://api.iconify.design/logos:vitest.svg",
    description:
      "The next generation testing framework powered by Vite. It's fast!",
    link: "https://vitest.dev/",
  },

  {
    id: 6,
    name: "TypeScript",
    icon: "https://api.iconify.design/vscode-icons:file-type-typescript-official.svg",
    description:
      "TypeScript is a strongly typed programming language that builds on JavaScript.",
    link: "https://www.typescriptlang.org/",
  },
  {
    id: 7,
    name: "TailwindCss",
    icon: "https://api.iconify.design/devicon:tailwindcss.svg",
    description:
      "Tailwind CSS is a utility-first CSS framework for rapidly building modern websites.",
    link: "https://tailwindcss.com/",
  },
  {
    id: 8,
    name: "TanStack Vue Query",
    icon: "https://vue-query-next-gen.vercel.app/vue-query.png",
    description:
      "The missing data fetching library for fetching, caching and updating asynchronous data.",
    link: "https://tanstack.com/query/latest/docs/framework/vue/overview",
  },
  {
    id: 9,
    name: "Vercel",
    icon: "https://api.iconify.design/vscode-icons:file-type-vercel.svg",
    description:
      "The Frontend Cloud. Build, scale, and secure a faster, personalized web.",
    link: "https://vercel.com/",
  },
  {
    id: 10,
    name: "Netlify",
    icon: "https://api.iconify.design/vscode-icons:file-type-netlify.svg",
    description:
      "The essential platform for the delivery of exceptional and dynamic web experiences.",
    link: "https://www.netlify.com/",
  },
  {
    id: 10,
    name: "Vue Devtools",
    icon: "https://devtools-next.vuejs.org/logo-mini.svg",
    description:
      "Vue DevTools is a tool designed to enhance the Vue developer experience.",
    link: "https://devtools-next.vuejs.org/",
  },
  {
    id: 11,
    name: "VueUse",
    icon: "https://api.iconify.design/logos:vueuse.svg",
    description:
      "A collection of essential Vue composition utilities based on the composition API.",
    link: "https://vueuse.org/guide/",
  },
];
</script>
<template>
  <main class="grid w-full min-h-screen place-items-center">
    <div class="flex flex-col w-[700px] space-y-6 items-center">
      <div>
        <img
          src="https://api.iconify.design/logos:vue.svg"
          alt="Vue Logo"
          class="w-14 h-14"
        />
      </div>

      <div>
        <h2 class="font-sans text-4xl font semibold">
          Welcome To Create Vue 3 App
        </h2>
      </div>

      <div class="w-full">
        <div
          class="grid auto-rows-[185px] place-items-center grid-cols-3 gap-3"
        >
          <div v-for="pkg in packages" :key="pkg.id">
            <div
              class="row-span-1 p-4 cursor-pointer gradient-border rounded-xl border-1 border-slate-400/10 bg-neutral-100 dark:bg-neutral-950"
            >
              <a
                :href="pkg.link"
                target="_blank"
                class="flex flex-col items-center space-y-3"
              >
                <div
                  class="grid w-12 h-12 rounded-md bg-neutral-800 place-items-center"
                >
                  <img :src="pkg.icon" :alt="pkg.name" class="w-7 h-7" />
                </div>

                <div>
                  <h2 class="text-lg">{{ pkg.name }}</h2>
                </div>

                <div>
                  <p class="text-[12px] text-gray-300 text-center">
                    {{ pkg.description }}
                  </p>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
