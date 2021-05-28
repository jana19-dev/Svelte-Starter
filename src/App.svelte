<script>
  import { onMount } from 'svelte'

  let count = 0

  onMount(() => {
    const interval = setInterval(() => count++, 1000)
    return () => {
      clearInterval(interval)
    }
  })
</script>

<div class="h-screen">
  <header class="h-full flex flex-col items-center justify-center">
    <img src="/logo.svg" class="h-64 mb-12 animate-logo" alt="logo" />
    <p class="m-2">Edit <code class="bg-gray-300 px-2 py-1 rounded-md">src/App.svelte</code> and save to reload.</p>
    <p class="m-2">Page has been open for <code class="bg-gray-300 px-1 py-1 rounded-md">{count}</code> seconds.</p>
    <p class="m-2">
      <a class="text-red-500" href="https://svelte.dev" target="_blank" rel="noopener noreferrer">
        Learn {import.meta.env.SNOWPACK_PUBLIC_PROJECT_NAME}
      </a>
    </p>
  </header>
</div>
