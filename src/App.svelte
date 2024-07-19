<script>
  import "./app.css";

  const projects = [
    {
      img: "/img/site.webp",
      title: "eCommerce platform",
      technologies: ["php", "Laravel", "vue", "vuetify"],
      description:
        "An eCommerce platform where customers can order food and track the order status. It has an admin panel for handling orders.",
      demoLink: "https://foodie-php-dathlyo6wq-uc.a.run.app",
      codeLink: "https://github.com/bayleaf1/foodie-php",
    },
    {
      img: "img/site.webp",
      title: "Game of life",
      technologies: ["react"],
      description: "A cellular automaton simulation where cells live or die based on neighboring cells, creating evolving patterns without needing further input.",
      demoLink: "https://game-of-life-21310.web.app",
      codeLink: "https://github.com/bayleaf1/react-game-of-life",
    },
    // {
    //   img: "img/site.webp",
    //   title: "Digital agency",
    //   technologies: ["vue", "ant"],
    //   description: "Landing for digital agency with multiple sections, hero, about, clients, features, services, team, contact us",
    //   demoLink: "https://foodie-php-dathlyo6wq-uc.a.run.app",
    //   codeLink: "https://github.com/bayleaf1/foodie-php",
    // },
  ];
</script>

<div class="h-20 shadow-lg"></div>
<div class="max-w-[1240px] mx-auto px-5 py-10">
  <div class="flex gap-20 flex-wrap">
    {#each projects as project}
      <div class="max-w-xs">
        <a
          target="_blank"
          href={project.demoLink}
          class="border shadow-sm p-0 rounded h-[350px] cursor-pointer block"
        >
          <img
            src="img/site.webp"
            class="w-full h-full object-cover"
            alt="miss"
          />
        </a>
        <div class="px-2 flex flex-col items-center gap-3 mt-4">
          <p class="text-primary text-2xl">{project.title}</p>
          <div class="flex gap-3">
            {#each project.technologies as item}
              <div
                class="p-2 py-1 border border-primary rounded-md text-primary text-xs"
              >
                {item}
              </div>
            {/each}
          </div>
          <p class="text-sm text-center">{project.description}</p>
          <div class="flex justify-center gap-6">
            {#each [{ link: project.demoLink, icon: "desktop-outline", label: "Demo" }, { link: project.codeLink, icon: "code-outline", label: "Code" }] as item}
              <a
                href={item.link}
                target="_blank"
                class="flex gap-2 text-lg items-center pb-1.5 px-1 border-b-2 border-primary cursor-pointer"
              >
                <ion-icon class="text-lg visible" name={item.icon}></ion-icon>
                <span>{item.label}</span>
              </a>
            {/each}
          </div>
        </div>
      </div>
    {/each}
  </div>
</div>
