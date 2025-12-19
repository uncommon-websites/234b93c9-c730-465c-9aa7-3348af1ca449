<script>
  const heroes = [
    {
      name: "PORTFOLIO FOUNDER",
      company: "Financial Services",
      image: "/generated/image-confident-founder-in-their-40s-working-a-1766108336562-0.webp", 
      alt: "Portfolio founder portrait"
    },
    {
      name: "PORTFOLIO FOUNDER",
      company: "Capital Markets",
      image: "/generated/image-female-entrepreneur-in-business-casual-r-1766108339357-1.webp",
      alt: "Portfolio founder portrait"
    },
    {
      name: "PORTFOLIO FOUNDER",
      company: "Technology",
      image: "/generated/image-mature-male-founder-in-thoughtful-pose-b-1766108341958-2.webp",
      alt: "Portfolio founder portrait"
    },
    {
      name: "PORTFOLIO FOUNDER",
      company: "Enterprise Software",
      image: "/generated/image-young-founder-presenting-to-team-in-conf-1766108344710-3.webp",
      alt: "Portfolio founder portrait"
    }
  ];
</script>

<section class="pt-32 pb-16 md:pt-48 md:pb-24 overflow-hidden">
  <div class="container mx-auto px-6 md:px-12 mb-16">
    <h1 class="font-display text-5xl md:text-7xl leading-[1.1] text-gray-900 max-w-4xl">
      Backing <span class="italic font-normal">bold founders</span><br />
      building the future.
    </h1>
  </div>

  <div class="pl-6 md:pl-12 overflow-x-auto pb-8 scrollbar-hide">
    <div class="flex space-x-1 min-w-max">
      {#each heroes as hero, i}
        <div class="relative group w-[300px] md:w-[400px]">
          <div class="aspect-[3/4] overflow-hidden bg-gray-100 relative">
            <img 
              src={hero.image} 
              alt={hero.alt}
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
            />
            {#if i === 0}
              <button class="absolute bottom-4 left-4 w-8 h-8 bg-white rounded-full flex items-center justify-center hover:scale-110 transition-transform" aria-label="Pause">
                <svg width="10" height="12" viewBox="0 0 10 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="3" height="12" rx="1.5" fill="black"/>
                  <rect x="7" width="3" height="12" rx="1.5" fill="black"/>
                </svg>
              </button>
              <div class="absolute bottom-0 left-0 w-full h-1 bg-gray-200">
                <div class="h-full bg-primary-700 w-1/3"></div>
              </div>
            {/if}
          </div>
          <div class="mt-4 flex items-baseline space-x-2">
            <span class="text-xs font-bold tracking-widest uppercase text-gray-900">{hero.name}</span>
            <span class="text-xs font-serif italic text-gray-500">{hero.company}</span>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
