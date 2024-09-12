<script>
    import { base } from '$app/paths';
    import config from "../config.js";
    import {page} from "$app/stores";
    let { title } = config;
    let ActiveMenu = $page.url.pathname;
    let MobileMenuActive = false;
</script>

<!-- Navigation -->
<nav class="px-6 py-6 md:px-16 items-center bg-white border-gray-200 dark:bg-gray-900 dark:border-gray-700">
    <div class="flex flex-wrap items-center justify-between mx-auto px-2">
        <a href="{base}" class="flex items-center"
           on:click={() => { ActiveMenu = `${base}/` }}
        >
            <img src="img/logo.jpeg" class="w-8" alt="Logo">
            <span class="pl-2 -mt-0.5  self-center text-xl font-semibold whitespace-nowrap dark:text-white">{title}</span>
        </a>
        <div class="flex md:order-2">
            <a href="https://www.facebook.com/groups/208155516383522" target="_blank" rel="noreferrer"
               class="flex gap-x-2 text-white rounded-lg px-5 py-2.5 text-center md:mr-3" style="background-color: #3b579d;">
                <i class="fa-solid fa-users pt-1"></i>
                Facebook
            </a>
            <button class="inline-flex items-center p-2 ml-3  text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
                on:click={() => { MobileMenuActive = !MobileMenuActive }}
            >
                <span class="sr-only">Open main menu</span>
                <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
            </button>
        </div>
    </div>
</nav>
