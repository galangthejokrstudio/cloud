<script>
    const features = [
        { icon: "ri-cloud-line", title: "Penyimpanan Awan", description: "Unggah dan unduh file dari perangkat apa pun.", coming_soon: false },
        { icon: "ri-share-line", title: "Berbagi File", description: "Bagikan file dengan siapa pun yang memiliki tautan.", coming_soon: false },
        { icon: "ri-lock-line", title: "Keamanan Berkas", description: "Lindungi file Anda dengan langkah-langkah keamanan tingkat lanjut.", coming_soon: false },
        { icon: "ri-compass-3-line", title: "Watermark Costum", description: "Sinkronkan file Anda di beberapa perangkat.", coming_soon: true },
    ]
</script>

<section class="py-24" id="features">
    <div class="container mx-auto px-4">
        <h1 class="text-center font-extrabold text-4xl mb-4">
            <span class="relative">
            Our <span class="text-primary">Features</span>
        </span>
        </h1>
        <p class="text-center opacity-70 max-w-2xl mx-auto mb-12">Temukan kekuatan solusi cloud kami dengan fitur-fitur luar biasa yang dirancang untuk mengamankan data Anda dan menyederhanakan alur kerja Anda.</p>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
            {#each features as feature}
            <div class="border border-gray px-6 py-4 rounded-lg relative flex flex-col">
                <div class="absolute -top-5 bg-white">
                    <i class="{feature.icon} text-primary text-4xl"></i>
                </div>

                <div class="relative {feature.coming_soon ? 'blur-sm' : ''} mt-4">
                    <h3 class="text-xl font-semibold mb-2">{feature.title}</h3>
                    <p class="opacity-70">{feature.description}</p>
                </div>

                {#if feature.coming_soon}
                <div class="absolute inset-0 flex items-center justify-center z-20">
                    <span class="font-extrabold p-0.5 bg-primary text-white px-4 rounded-full uppercase"><i class="ri-time-line"></i> Coming Soon</span>
                </div>
                {/if}
            </div>
            {/each}
        </div>
    </div>
</section>
