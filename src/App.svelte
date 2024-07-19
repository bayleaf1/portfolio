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
      description:
        "A cellular automaton simulation where cells live or die based on neighboring cells, creating evolving patterns without needing further input.",
      demoLink: "https://game-of-life-21310.web.app",
      codeLink: "https://github.com/bayleaf1/react-game-of-life",
    },
    {
      img: "img/site.webp",
      title: "Digital agency",
      technologies: ["nuxt", "vue", "ant"],
      description:
        "Landing for digital agency with multiple sections, hero, about, clients, features, services, team, contact us",
      demoLink: "https://foodie-php-dathlyo6wq-uc.a.run.app",
      codeLink: "https://github.com/bayleaf1/foodie-php",
    },
  ];
</script>

<div class="max-w-[1440px] mx-auto px-2 py-10">
  <div class="flex gap-6 lg:gap-8 flex-col lg:flex-row">
   
    <div class="text-center flex flex-col md:flex-row gap-4 items-center lg:flex-col md:justify-center lg:justify-start lg:items-center lg:mt-14">
      <div
        class="shadow-lg w-[150px] h-[150px] lg:w-[200px] lg:h-[200px] border rounded-full"
      ></div>

      <div class="flex flex-col items-center">
        <p class="text-2xl">Dinu</p>
        <p class="text-sm px-4 text-center">Full stack. 3 y.e. Javascript, Node, php </p>
        <div class="text-sm mt-2">
          <div class="flex items-center gap-1">
            <ion-icon class="text-lg visible" name={"mail-outline"}
            ></ion-icon><a href="mailto:dinucontdelucru@gmail.com"
              >dinucontdelucru@gmail.com</a
            >
          </div>
          <div class="flex items-center gap-1 mt-1">
            <ion-icon class="text-lg visible" name={"call-outline"}
            ></ion-icon><a href="tel:+37379552160">+37379552160</a>
          </div>
        </div>
      </div>
    </div>

    <div class="">
      <p class="text-primary text-3xl font-medium text-center">Projects</p>
      <div class="flex gap-14 flex-wrap justify-center mt-4">
        {#each projects as project}
          <div class="max-w-xs">
            <a
              target="_blank"
              href={project.demoLink}
              class="border shadow-sm p-0 rounded h-[300px] cursor-pointer block"
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
              <p class="text-sm text-center min-h-20">{project.description}</p>
              <div class="flex justify-center gap-6">
                {#each [{ link: project.demoLink, icon: "desktop-outline", label: "Demo" }, { link: project.codeLink, icon: "code-outline", label: "Code" }] as item}
                  <a
                    href={item.link}
                    target="_blank"
                    class="flex gap-2 text-lg items-center pb-1.5 px-1 border-b-2 border-primary cursor-pointer"
                  >
                    <ion-icon class="text-lg visible" name={item.icon}
                    ></ion-icon>
                    <span>{item.label}</span>
                  </a>
                {/each}
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
</div>
