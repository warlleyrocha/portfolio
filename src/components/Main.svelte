<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Núcleo Corp', icon: 'fa-solid fa-record-vinyl', href: 'https://warlleyrocha.github.io/NucleoCorp/'},
        {name: 'Maisa Alves - Terapias Holísticas', icon: 'fa-solid fa-heart-circle-plus', href:'https://maisa-alves-terapias-integrativas.vercel.app/'},
        {name: 'Personal Page', icon: 'fa-solid fa-user', href:''},
        ];

        let benefits = [
            {name: 'a self taught developer', description: 'The technologies I use today, I learned on my own through forums, documentation, courses, and free internet resources.'},
            {name: 'clean code developer', description: 'I like to organize my code in a way that adopts a consistent pattern between tags and their instances, using more precise logical structures and fewer lines. This aims to optimize the maintenance process and the addition of new functions, making it more practical and dynamic.'},
            {name: '', description: ''},
        ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-[#00A40D]">Warlley</span> Rocha <br/>Front-End
                <span class="poppins text-[#00A40D]">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-[#00A40D]">favorite tech</span> includes HTML, CSS, JavaScript, React, TailwindCSS!
            </p>
            <a href="https://github.com/warlleyrocha" target="_blank" class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-[#00A40D] opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/image0.png"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]">
        </div>       
    </section>
    
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-[#00A40D]">see</span> my work?
            </h3>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Official website of the Núcleo Corporation record label, developed with <strong class="text-[#00A40D]">React and Tailwind CSS</strong></p>
            </Step>
            <Step step={steps[1]}>
                <p>Website template for integrative therapies developed with <strong class="text-[#00A40D]">Bootstrap</strong></p>
            </Step>
            <Step step={steps[2]}>
                <p>It's the page you're on right now! Developed with <strong class="text-[#00A40D]">Svelte and Tailwind CSS</strong></p>
            </Step>
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">

        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-[#00A40D] after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-[#00A40D] py-4">

        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-[#00A40D]">about</span> me</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>{benefit.description}</p>
                </div>
            </div>    
            {/each}
        </div>

    </section>
</main>
