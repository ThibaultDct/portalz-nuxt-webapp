<!-- Please remove this file from your project -->
<template>
    <div class="flex flex-col w-45 h-full overflow-hidden bg-primary shadow">
        
      <div id="sidebar-top" class="flex flex-col">
        <a class="flex items-center w-full px-4 mt-3 hover:text-accent hover:bg-accent" href="#">
          <svg id="sw-js-blob-svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <linearGradient id="sw-gradient" x1="0" x2="1" y1="1" y2="0">
                <stop id="stop1" stop-color="rgba(248, 117, 55, 1)" offset="0%"></stop>
                <stop id="stop2" stop-color="rgba(251, 168, 31, 1)" offset="100%"></stop>
              </linearGradient>
            </defs>
            <path fill="url(#sw-gradient)" d="M21.4,-23.4C27.7,-20.3,32.8,-13.5,32.4,-7C32.1,-0.5,26.4,5.8,22.4,13.2C18.5,20.7,16.2,29.4,10.8,32.7C5.4,36,-3.1,33.9,-9.6,30C-16.2,26.1,-20.8,20.4,-24,14.2C-27.1,8,-28.8,1.3,-27,-4C-25.2,-9.4,-19.9,-13.4,-14.8,-16.7C-9.7,-20.1,-4.9,-22.8,1.4,-24.4C7.6,-26.1,15.1,-26.5,21.4,-23.4Z"
             width="100%" height="100%" transform="translate(50 50)" stroke-width="0" style="transition: all 0.3s ease 0s;">
            </path>
          </svg>
          <span class="ml-2 text-sm font-bold">Portalz</span>
		    </a>
        <hr class="bg-accent">
      </div>

      <div id="sidebar-content" class="flex flex-col mx-3 mt-1">
        <a class="flex items-center w-full h-12 px-3 mt-2 rounded hover:bg-gray-700 hover:text-gray-300" v-for="item in menuItems" :key="item.id" :href="item.url">
				  <span class="material-icons">{{ item.icon }}</span>
          <span class="ml-2 text-sm font-medium">{{ item.name }}</span>
			  </a>
      </div>

      <div id="sidebar-bottom" class="items-center mt-3 border-t">
        <a class="flex items-center justify-center w-12 h-12 mt-2 rounded hover:bg-gray-700 hover:text-gray-300" href="#">
				  <svg class="w-6 h-6 stroke-current" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
				 	  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
				  </svg>
			  </a>
      </div>

    </div>
</template>

<script>
import { menu } from "~/assets/menu";

export default {
  name: 'Sidebar',

  data: function() {
    return {
      menuItems: menu,
      active: true,
    }
  },

  computed: {
    isActive() {
      return this.active;
    },
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
}
</style>