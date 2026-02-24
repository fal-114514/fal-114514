<!-- README -->
<div align="center">

<h1>ファル / Fal</h1>

<img src="static/avatar.png" width="80" height="80" style="border-radius: 50%; margin-top: -20px; border: 2px solid #707070ff;" alt="ファル / Fal" />

<br />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Lexend&size=14&duration=3500&pause=1000&color=A1A1AA&center=true&vCenter=true&width=380&lines=Flutter+を学習中...;基本AI任せ。;Discord+にて活動中。)](https://git.io/typing-svg)

<br />

![Svelte](https://img.shields.io/badge/Svelte-FF3E00?style=for-the-badge&logo=svelte&logoColor=white) ![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white) ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)

<a href="https://git.io/streak-stats">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=fal-114514&theme=tokyonight&hide_border=true&locale=ja&date_format=%5BY.%5Dn.j&width=300" alt="GitHub Streak" />
</a>

<br />

<a href="https://discord.com/users/1353729242906497084">
  <img src="https://lanyard.cnrad.dev/api/1353729242906497084?showDisplayName=true&bg=1a1b27&theme=dark" />
</a>

</div>

<br />

<!-- Source -->
<details>
<summary>View Source</summary>

```svelte
<script lang="ts">
  import { onMount } from "svelte";
  import { fade, fly } from "svelte/transition";

  let isMounted = false;

  const profile = {
    name: "ファル / Fal",
    bio: "技術ない",
    avatar: "/avatar.png",
    links: [
      {
        label: "Discord Status",
        url: "https://discord.com/users/1353729242906497084",
      },
    ],
  };

  onMount(() => {
    isMounted = true;
  });
</script>

<svelte:head>
  <title>{profile.name}</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
  <link
    href="https://fonts.googleapis.com/css2?family=Lexend:wght@300;400;500;600&family=LINE+Seed+JP:wght@400;700&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<div class="min-h-screen bg-[#0d1117] text-zinc-100 overflow-x-hidden flex flex-col">
  {#if isMounted}
    <main
      class="
        flex-grow
        mx-auto
        px-6
        py-24 sm:py-32
        max-w-md
        flex flex-col items-center
      "
    >

      <div
        in:fly={{ y: 10, duration: 800 }}
        class="mb-12"
      >
        <img
          src={profile.avatar}
          alt={profile.name}
          class="
            w-20 h-20
            rounded-full object-cover
            border-2 border-zinc-700
          "
          on:error={(e) =>
            ((e.currentTarget as HTMLImageElement).src =
              "https://ui-avatars.com/api/?name=" +
              profile.name +
              "&background=f4f4f5&color=71717a&size=80")}
        />
      </div>

      <div
        in:fly={{ y: 10, duration: 800, delay: 100 }}
        class="text-center mb-16 space-y-4"
      >
        <h1 class="text-2xl font-semibold tracking-tight font-jp">
          {profile.name}
        </h1>
        <p class="text-sm text-zinc-400 font-jp leading-relaxed max-w-xs mx-auto">
          {profile.bio}
        </p>
      </div>

      <div
        in:fly={{ y: 10, duration: 800, delay: 200 }}
        class="w-full space-y-4"
      >
        <div class="flex justify-center gap-2">
          <img src="https://img.shields.io/badge/Svelte-FF3E00?style=for-the-badge&logo=svelte&logoColor=white" alt="Svelte" />
          <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" />
          <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
        </div>

        <div class="flex flex-col items-center gap-4">
          <a href="https://git.io/streak-stats">
            <img src="https://github-readme-streak-stats.herokuapp.com?user=fal-114514&theme=tokyonight&hide_border=true&locale=ja&date_format=%5BY.%5Dn.j&width=300" alt="GitHub Streak" />
          </a>

          {#each profile.links as link}
            <a
              href={link.url}
              target="_blank"
              rel="noopener noreferrer"
            >
              <img src="https://lanyard.cnrad.dev/api/1353729242906497084?showDisplayName=true&bg=1a1b27&theme=dark" alt={link.label} />
            </a>
          {/each}
        </div>
      </div>
    </main>
  {/if}
</div>
```

</details>
