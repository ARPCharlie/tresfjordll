<template>
  <div class="bg-white">
    <header class="absolute inset-x-0 top-0 z-50">
      <nav
        class="flex items-center justify-between p-4 sm:p-6 lg:px-8"
        aria-label="Global"
      >
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="font-bold text-lg sm:text-xl">Tresfjord Lyd & Lys</span>
          </a>
        </div>
        <div class="flex lg:hidden">
          <button
            type="button"
            class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = true"
          >
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a
            v-for="item in navigation"
            :key="item.name"
            :href="item.href"
            class="text-sm font-semibold leading-6 text-gray-900"
            >{{ item.name }}</a
          >
        </div>
      </nav>
      <Dialog
        as="div"
        class="lg:hidden"
        @close="mobileMenuOpen = false"
        :open="mobileMenuOpen"
      >
        <div class="fixed inset-0 z-50" />
        <DialogPanel
          class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
        >
          <div class="flex items-center justify-between">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="font-bold text-lg sm:text-xl">Tresfjord Lyd & Lys</span>
            </a>
            <button
              type="button"
              class="-m-2.5 rounded-md p-2.5 text-gray-700"
              @click="mobileMenuOpen = false"
            >
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a
                  v-for="item in navigation"
                  :key="item.name"
                  :href="item.href"
                  @click="mobileMenuOpen = false"
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                  >{{ item.name }}</a
                >
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>

    <div class="relative isolate px-4 sm:px-6 pt-14 lg:px-8">
      <div
        class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
        aria-hidden="true"
      >
        <div
          class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
          style="
            clip-path: polygon(
              74.1% 44.1%,
              100% 61.6%,
              97.5% 26.9%,
              85.5% 0.1%,
              80.7% 2%,
              72.5% 32.5%,
              60.2% 62.4%,
              52.4% 68.1%,
              47.5% 58.3%,
              45.2% 34.5%,
              27.5% 76.7%,
              0.1% 64.9%,
              17.9% 100%,
              27.6% 76.8%,
              76.1% 97.7%,
              74.1% 44.1%
            );
          "
        />
      </div>
      <div class="mx-auto max-w-2xl py-24 sm:py-32 lg:py-40">
        <div class="hidden sm:mb-8 sm:flex sm:justify-center"></div>
        <div class="text-center">
          <h1
            class="text-balance text-3xl sm:text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl lg:text-7xl"
          >
            Tresfjord Lyd & Lys
          </h1>
          <p class="mt-6 text-lg sm:text-xl leading-8 text-gray-800">
            Proffesjonell lyd, lys og scene til alle dine arragement.
          </p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a
              href="#contact"
              class="rounded-md border-2 py-2 px-4 sm:py-3 sm:px-6 text-lg sm:text-xl border-black bg-transparrent hover:bg-black hover:text-white text-black font-bold"
              >Kontakt oss</a
            >
          </div>
        </div>
      </div>
      <div
        class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
        aria-hidden="true"
      >
        <div
          class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]"
          style="
            clip-path: polygon(
              74.1% 44.1%,
              100% 61.6%,
              97.5% 26.9%,
              85.5% 0.1%,
              80.7% 2%,
              72.5% 32.5%,
              60.2% 62.4%,
              52.4% 68.1%,
              47.5% 58.3%,
              45.2% 34.5%,
              27.5% 76.7%,
              0.1% 64.9%,
              17.9% 100%,
              27.6% 76.8%,
              76.1% 97.7%,
              74.1% 44.1%
            );
          "
        />
      </div>
    </div>
  </div>
  <div class="bg-white py-16 sm:py-24 lg:py-32">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <p
          class="mt-2 text-3xl sm:text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl"
        >
          Hva vi leverer
        </p>
        <p class="mt-6 text-lg sm:text-xl leading-8 text-gray-700">
          Her er en oversikt over hvilke tjenester vi leverer.
        </p>
      </div>
      <div class="mx-auto mt-12 sm:mt-16 lg:mt-20 max-w-2xl lg:max-w-4xl">
        <dl
          class="grid max-w-xl grid-cols-1 gap-x-6 gap-y-8 sm:gap-x-8 sm:gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16"
        >
          <div
            v-for="feature in features"
            :key="feature.name"
            class="relative pl-16 sm:pl-20"
          >
            <dt
              class="font-semibold leading-7 text-gray-900 text-lg sm:text-xl md:text-2xl"
            >
              <div
                class="absolute left-0 top-0 flex h-12 w-12 sm:h-16 sm:w-16 items-center justify-center rounded-lg bg-black"
              >
                <component
                  :is="feature.icon"
                  class="h-5 w-5 sm:h-6 sm:w-6 text-white"
                  aria-hidden="true"
                />
              </div>
              {{ feature.name }}
            </dt>
            <dd class="mt-2 text-base sm:text-lg md:text-xl leading-7 text-gray-600">
              {{ feature.description }}
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
  <div class="bg-white py-16 sm:py-24 lg:py-32">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 sm:text-5xl">
          Informasjon
        </h2>
      </div>
      <div class="mt-10">
        <div class="grid grid-cols-1 gap-6 sm:gap-8 md:grid-cols-2 lg:grid-cols-3">
          <div class="bg-gray-50 rounded-lg p-4 sm:p-6 shadow-md">
            <h3 class="text-lg sm:text-xl font-semibold text-gray-900 mb-2">Plassering</h3>
            <p class="text-gray-600 text-base sm:text-lg">
              Noe om hvor vi har lager og hvor vi lever til kanskje???
            </p>
          </div>
          <div class="bg-gray-50 rounded-lg p-4 sm:p-6 shadow-md">
            <h3 class="text-lg sm:text-xl font-semibold text-gray-900 mb-2">Noe</h3>
            <p class="text-gray-600 text-base sm:text-lg">
              Du fer virkelig finne på nokko sprell her altså, øyvind.
            </p>
          </div>
          <div class="bg-gray-50 rounded-lg p-4 sm:p-6 shadow-md">
            <h3 class="text-lg sm:text-xl font-semibold text-gray-900 mb-2">Noe annet</h3>
            <p class="text-gray-600 text-base sm:text-lg">
              Åsså kanskje nokko lite her, om d e aktuelt?
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="bg-white py-16 sm:py-24 lg:py-32">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-4xl sm:text-5xl md:text-6xl font-bold text-center mb-8 sm:mb-12">Crewet</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 bg-black text-black p-4 sm:p-6 py-16 sm:py-24">
        <div v-for="member in crewMembers" :key="member.id" class="flex flex-col items-center mx-auto bg-white py-4 sm:py-6 rounded-md w-full sm:w-80 lg:w-96">
          <img :src="member.image" :alt="member.name" class="w-32 h-32 sm:w-40 sm:h-40 object-fit rounded-full mb-4">
          <h3 class="text-xl sm:text-2xl font-semibold mb-2">{{ member.name }}</h3>
          <p class="text-gray-800 text-base sm:text-lg">{{ member.job }}</p>
        </div>
      </div>
    </div>
  </div>
  <div class="bg-white py-16 sm:py-24 lg:py-32">
    <div class="container w-full sm:w-3/4 md:w-1/2 lg:w-1/3 mx-auto px-4 sm:px-6">
      <h2 class="text-4xl sm:text-5xl md:text-6xl font-bold text-center mb-8 sm:mb-12">Kontakt oss</h2>
      <div class="gap-6 sm:gap-8 p-4 sm:p-6 py-16 sm:py-24 bg-black flex justify-center">
        <div class="flex flex-col items-center bg-white p-4 sm:p-6 rounded-md w-full sm:w-96">
          <img src="https://via.placeholder.com/150" alt="Kontakt person" class="w-32 h-32 sm:w-40 sm:h-40 object-fit rounded-full mb-4">
          <h3 class="text-xl sm:text-2xl font-semibold mb-2">Øyvind Rypdal</h3>
          <p class="text-base sm:text-lg">Telefon: 95250532</p>
          <p class="text-base sm:text-lg">E-post: oyvind.rypdal@hotmail.com</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { Dialog, DialogPanel } from "@headlessui/vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";
import {
  SpeakerWaveIcon,
  LightBulbIcon,
  VideoCameraIcon,
  MusicalNoteIcon,
} from "@heroicons/vue/24/outline";

const mobileMenuOpen = ref(false);

const navigation = [
  { name: "Hjem", href: "#" },
  { name: "Tjenester", href: "#services" },
  { name: "Info", href: "#info" },
  { name: "Crew", href: "#crew" },
  { name: "Kontakt", href: "#contact" },
];

const features = [
  {
    name: "Lyd",
    description: "Lyd utstyr til høy kvalitet.",
    icon: SpeakerWaveIcon,
  },
  {
    name: "Lys",
    description: "Profesjonelle fiksturer og lys miksing.",
    icon: LightBulbIcon,
  },
  {
    name: "AV",
    description: "Filming, streaming og display.",
    icon: VideoCameraIcon,
  },
  {
    name: "Scene",
    description: "Scene utstyr til alle typer arrangementer.",
    icon: MusicalNoteIcon,
  },
];

const crewMembers = [
  {
    id: 1,
    name: "Øyvind",
    job: "Big boss",
    image: "https://picsum.photos/200/300"
  },
  {
    id: 2,
    name: "Kristoffer",
    job: "Lika å klage",
    image: "https://picsum.photos/200/300"
  },
  {
    id: 3,
    name: "Remi",
    job: "Trøtt til tides",
    image: "https://picsum.photos/200/300"
  },
  {
    id: 4,
    name: "Martinus",
    job: "Spiss kompetent i inkompetanse",
    image: "https://picsum.photos/200/300"
  },
  {
    id: 5,
    name: "E d fleir?",
    job: "Production Manager",
    image: "https://picsum.photos/200/300"
  },
  {
    id: 6,
    name: "Muligens...",
    job: "Event Coordinator",
    image: "https://picsum.photos/200/300"
  }
];
</script>
