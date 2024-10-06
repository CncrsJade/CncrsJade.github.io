

 <script>
    import Step from "./prev.svelte";

    // Array of project
    let projects = [
        {
            name: "PractiPro",
            link: "https://github.com/CncrsJade/PractiPro.git",
        },
        {
            name: "Flower Shop",
            link: "https://github.com/CncrsJade/ONLINE-FLOWER-SHOP.git",
        },
        {
            name: "Rent House",
            link: "https://github.com/CncrsJade/OOP.git",
        },
    ];

    // Array of about sections
    let about = [
        {
            name: "College Life",
            icon: "fa-solid fa-school",
            description: "I am now on my 3rd year in college which I can say it's the climax of my college life plot. During my 3 years in college, I only joined few social activities like acquaintance party, sportfest wherein I only attended once a day for the week long event. 1st year and second year I joined futsal for the sportfest and been the class representative which I am a bit forced on taking responsibility. Gordon College is a good place to learn and explore your interests, I am grateful for the opportunities I have been given and I am excited to see what the future holds.",
        },
        {
            name: "Why Computer Science?",
            icon: "fa-solid fa-computer",
            description: "I choose computer science because I have interest on various high technologies and what will be the impact of the tech advancements in our daily lives. what caught my interest more is the machine learning and AI, I find it fascinating how AI can do tasks that requires human-like intelligence. I want to learn more about AI and how it can be applied in the real world. I used to think that this carrer path is easy and I can nail it but reality check; one must exert more effort in learning especially the curriculum is not what I expect it to be and the materials seems to be lacking.",

        },
        {
            name: "Career Interest",
            icon: "fa-solid fa-flag",
            description: "The career path I am more interested is Psychology. I want to be a psychologist, I want to help people with their mental health and I want to be a part of the solution to the mental health issues in the society. With combination of my interest in computer science, I wanna to know the behavior of the tech user, especially the law breaker and the one who abuses technology for bad purposes.",
        },
        {
            name: "Writing Hobbies",
            icon: "fa-solid fa-pen",
            description: "My Hobby is more on pen and paper, I like to write poems featuring mental health issues, social issues and ideology. I sometimes feature the life experiences of the people around me. I also write journal on my social obsevation, political perspectives, emotional state and other stuff.",
        },
        {
            name: "Gaming Hobby",
            icon: "fa-solid fa-gamepad",
            description: "I do play both Mobile games and PC games but I quit other games. I play mobile games (Mobile Legends, Rise Of Kingdoms) when I am upset and wishes to crush some players. PC games (Mine Craft, L4D2, Roblox) when I want to have fun with my friends and whenever I wishes to relax or wash away my worries.",
        },
    ];

    // Array of social media links
    let socials = [
        {
            name: "Gmail",
            icon: "fa-solid fa-square-envelope",
            description: "cancersyu0@gmail.com"
        },
        {
            name: "GitHub",
            icon: "fa-brands fa-github",
            link: "https://github.com/CncrsJade",
            description: "CncrsJade",
        },
        {
            name: "Facebook",
            icon: "fa-brands fa-facebook",
            description: "Jade S. Viñas",
        },
        {
            name: "Instagram",
            icon: "fa-brands fa fa-instagram",
            link: "https://www.instagram.com/jade.daldal/",
            description: "Jade",
        },
        {
            name: "Steam",
            icon: "fa-brands fa-steam",
            link:"https://steamcommunity.com/profiles/76561199260180182/",
            description: "cncrs",
        },
        {
            name: "Discord",
            icon: "fa-brands fa-discord",
            description: "cncrs6",
        },
    ];

</script>


<main class="flex flex-col flex-1 p-4">
    <!-- Introduction Section -->
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
        
        <h5 class="font-semibold text-3xl sm:text-4xl md:text-8xl">
            Jade S. Viñas
            <h3 class="font-semibold text-2xl sm:text-2xl md:text-6xl">
                <span class="poppins text-orange-700">BSCS Student</span>
            </h3>
        </h5>
        
            <p class="text-base sm:text-lg md:text-4xl">
                I’m currently studying at <span class="text-green-500"> Gordon College</span> under  <span class="text-orange-600"> College of Computer Studies</span> Department and I am
                taking a course; <span class="text-orange-400"> Bachelor of Science in Computer Science</span>
            </p>
            

        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/jade.png"}
                alt="img"
                class="object-cover z-[2] max-h-[100vh] square-full"
            />
        </div>
    </section>

    <!-- About Section -->
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    > 
        <div
        >
        <h6 class="text-large sm:text-xl md:text-4xl text-white font-bold">
            Additional Information &darr;
        </h6>
            
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-8xl">
            Jade S. Viñas
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each about as item, index}
            
                <div class="flex gap-6 sm:gap-8">
                    
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl press-start-font">
                            <i class={item.icon}></i>
                            {item.name}
                        </h3>
                        <p  class="text-justify">{item.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>

    <!-- Projects Section -->
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                <span class="poppins text-cyan-200">Check out my Projects</span>
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10 source-code-pro">
            {#each projects as project}
                <Step {project}>
                    <p class="text-justify">
                        {#if project.name === "PractiPro"}
                            <strong class="text-orange-400"> Angular Framework</strong> 
                            <br>
                            <strong class="text-blue-400">RestApi PHP</strong>
                        {:else if project.name === "Rent House"}
                            <strong class="text-yellow-400">Wep App</strong>
                            <br>
                            <strong class="text-blue-400">PHP Backend</strong>
                            <br>
                            <strong class="text-blue-400">HTML and CSS Frontend</strong>
                        {:else if project.name === "Flower Shop"}
                        <strong class="text-green-400">Web App</strong>
                            <br>
                        <strong class="text-blue-400">PHP Backend</strong>
                        <br>
                        <strong class="text-blue-400">HTML and CSS Frontend</strong>                        
                        {/if}
                    </p>

                    <div class="flex-1 flex justify-between gap-4 items-end">
                        <div class="ml-auto cursor-pointer hover:text-white duration-200 relative after:absolute after:top-0 after:h-full after:right-full after:bg-black after:w-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden">
                            <a href={project.link} class="text-blue-400 hover:text-white">Visit &rarr;</a>
                        </div>
                    </div>
                </Step>
            {/each}
        </div>
    </section>

    <!-- Social Media Section -->
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="social-info">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                Connect with Me.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                <span class="poppins text-orange-700">Contacts</span>
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            {#each socials as social}
                <Step project={social}>
                    {#if social.link}
                    <a href={social.link} class="text-blue-400 hover:text-white duration-200 relative after:absolute after:top-0 after:h-full after:left-0 after:w-0 after:duration-200 hover:after:w-full after:z-[-1] overflow-hidden" target="_blank" rel="noopener noreferrer">{social.description}</a>
                    {:else}
                        <p>{social.description}</p>
                    {/if}
                </Step>
            {/each}
        </div>
    </section>
</main>