<script>
    // Exporting the project prop
    export let project;
</script>

<main class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-cyan-700 text-center cursor-pointer group hover:border-orange-500 duration-200">
    <!-- Icon Section -->
    <div class="place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200">
        <i class={project.icon} />
    </div>
    <!-- Project Name -->
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">
        {project.name}
    </h3>
    <!-- Slot for additional content -->
    <slot />
</main>