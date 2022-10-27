<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

import Navbar from './Components/Navbar.vue';

const users = [
  {
    name: 'Antoine Famibelle',
    position: 'Developpeur Front',
    img: 'https://antoinefamibelle-dev.com/_nuxt/img/3c9d5f5.jpg',
  },
  {
    name: 'Vincent Lemesle',
    position: 'Developpeur Back',
    img: '/Vincent.jpeg',
  },
  {
    name: 'Cyril De Lajudie',
    position: 'Developpeur Mobile',
    img: '/Cyril.jpeg',
  },
  {
    name: 'Gregoire Brasseur',
    position: 'Developpeur Mobile',
    img: '/Gregoire.jpeg',
  },
  {
    name: 'Jérémy Groizard',
    position: 'Developpeur Front',
    img: '/Jeremy.jpeg',
  }
]

const timeline = [
  {
    title: 'Première Beta',
    description: 'Sortie de la première version de l\'application pour tout le monde.',
    date: 'Juin 2022'
  },
  {
    title: 'Site Vitrine',
    description: 'Migration du site vitrine vers du Vue.js 3.',
    date: 'Septembre 2022'
  },
  {
    title: 'Présentation',
    description: 'Premiere présentation de l\'application à Epitech Paris.',
    date: 'Septembre 2022'
  },
];
</script>

<template>
  <Navbar />
  <a class="block p-6 max-w bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"> Qu'est ce que Fundy ?</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
      Nous, c’est Fundy, la première application de crowdfunding par l’arrondi sur vos transactions du quotidien.
    Notre objectif est de maximiser le financement des projets participatifs, tout en créant un lien de confiance entre les donateurs et les créateurs de projets.
    </p>
    <p class="mt-8 font-normal text-gray-700 dark:text-gray-400">
      50%, c’est le nombre de projets participatifs qui atteignent leur objectif en 2020.
      Un nombre de plus en plus en déclin, dû à plusieurs problématiques.
      Arnaques, manques d’informations, de contrôle ou encore de confiance.
    </p>
  </a>
  <a class="block p-6 max-w bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <div class="grid gap-4 grid-cols-1 md:grid-cols-3 ">
      <div v-for="user in users" :key="user.name">
        <a class="relative block bg-black group rounded-2xl p7">
          <img
            class="absolute inset-0 object-cover w-full h-full opacity-75 transition-opacity group-hover:opacity-50 p2"
            :src="user.img"
            alt=""
          />
          <div class="relative p-8">
            <p class="text-sm font-medium tracking-widest text-pink-500 uppercase">
              {{user.position}}
            </p>
            <p class="text-2xl font-bold text-white">{{user.name}}</p>
            <div class="mt-64"></div>
          </div>
        </a>
      </div>
    </div>
  </a>
  <a class="block p-6 max-w bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"> Timeline</h5>
    <ol class="items-center sm:flex">
    <li v-for="item in timeline" :key="item.title" class="relative mb-6 sm:mb-0">
        <div class="flex items-center">
            <div class="flex z-10 justify-center items-center w-6 h-6 bg-blue-200 rounded-full ring-0 ring-white dark:bg-blue-900 sm:ring-8 dark:ring-gray-900 shrink-0">
                <svg aria-hidden="true" class="w-3 h-3 text-blue-600 dark:text-blue-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"></path></svg>
            </div>
            <div class="hidden sm:flex w-full bg-gray-200 h-0.5 dark:bg-gray-700"></div>
        </div>
        <div class="mt-3 sm:pr-8">
            <h3 class="text-lg font-semibold text-gray-900 dark:text-white">{{item.title}}</h3>
            <time class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">{{item.date}}</time>
            <p class="text-base font-normal text-gray-500 dark:text-gray-400">{{item.description}}</p>
        </div>
    </li>
    </ol>
  </a>

<footer class="p-4 bg-white sm:p-6 dark:bg-gray-900">
    <div class="md:flex md:justify-between">
      <div class="mb-6 md:mb-0">
          <a href="http://eip.epitech.eu/2023/fundy" class="flex items-center">
              <img src="/icon.png" class="mr-3 h-8" alt="Fundy Logo">
              <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">Fundy</span>
          </a>
      </div>
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8">
    <div class="sm:flex sm:items-center sm:justify-between">
      <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2022 <a href="http://eip.epitech.eu/2023/fundy" class="hover:underline">Fundy</a>. All Rights Reserved.
      </span>
      <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">Contactez-nous ! <a href="http://eip.epitech.eu/2023/fundy" class="hover:underline">Fundy@gmail.com</a>
      </span>
      <div class="flex mt-4 space-x-6 sm:justify-center sm:mt-0">
          <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd"></path></svg>
              <span class="sr-only">Instagram page</span>
          </a>
      </div>
    </div>
</footer>

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
