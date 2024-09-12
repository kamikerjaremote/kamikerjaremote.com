<script>
    import { base } from '$app/paths';
    import config from "../config.js";
    let { title, socials } = config;
</script>

<footer class="px-4 md:px-16 mt-12 mb-6">
    <div class="bg-black p-8 rounded-2xl">
        <div class="text-center mb-4">
            <div class="text-xl text-white font-bold">Mari Tergabung di Dalam Komunitas Kami Kerja Remote (KKR)</div>
            <div class="text-gray-400">Bergabung dengan 79,000+ anggota dari seluruh Indonesia</div>
            <div class="flex justify-center gap-x-6 pt-4 text-white text-xl">
                {#each socials as social}
                    <a href="{social.url}" target="_blank" rel="noopener noreferrer">
                        <i class="{social.icon}"></i>
                    </a>
                {/each}
            </div>
        </div>

        <div class="flex justify-center gap-x-8 text-white">
            <span>&copy; { new Date().getFullYear() } <a href="{base}">{title}</a></span>
        </div>
    </div>
</footer>
