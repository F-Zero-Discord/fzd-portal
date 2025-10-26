<script lang="ts">
  import { Progress } from '@skeletonlabs/skeleton-svelte';
  let value = 42;
</script>

<section class="mx-auto max-w-3xl p-8 space-y-6">
  <header class="space-y-2">
    <h1 class="text-3xl font-semibold">Hello Skeleton 👋</h1>
    <p class="text-surface-500">Tailwind v4 + Skeleton, running on SWA.</p>
  </header>

  <div class="rounded-xl border border-surface-200/70 p-6">
    <h2 class="text-xl mb-4">Progress</h2>
    <Progress value={value} max={100} />
    <div class="mt-4 flex gap-2">
      <button class="btn variant-filled" on:click={() => (value = Math.min(100, value + 10))}>+10</button>
      <button class="btn variant-outline" on:click={() => (value = Math.max(0, value - 10))}>-10</button>
    </div>
  </div>

  <div class="flex items-center gap-3">
    <span class="font-medium">Theme:</span>
    <button class="btn variant-ghost" on:click={() => document.documentElement.setAttribute('data-theme', 'cerberus')}>Cerberus</button>
    <button class="btn variant-ghost" on:click={() => document.documentElement.setAttribute('data-theme', 'modern')}>Modern</button>
    <button class="btn variant-ghost" on:click={() => document.documentElement.setAttribute('data-theme', 'rocket')}>Rocket</button>
  </div>
</section>
