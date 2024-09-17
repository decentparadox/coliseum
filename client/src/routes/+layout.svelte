<script lang="ts">
    import "../app.css"
    import Navbar from "$lib/Navbar.svelte";
</script>

<div class="p-4">
    <Navbar />
    <slot />
</div>