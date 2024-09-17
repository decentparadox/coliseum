<script lang="ts">
    let src = "/favicon.png"
    import { page } from "$app/stores"
    import { SignIn, SignOut } from "@auth/sveltekit/components"
</script>
<div class="flex justify-between items-center pb-4">
<div class="w-8 h-8">
    <img {src} alt="Coliseum Logo">
</div>
<div class="flex gap-4 ">
    <a href="/scoreboard"><p>Scoreboard</p></a>
    <a href="/challenges"><p>Challenges</p></a>
    {#if $page.data.session}
    <a href="/profile"><p>Profile</p></a>
    <SignOut>
        <p>Sign out</p>
    </SignOut>
    {:else}
        <SignIn>
          <p>Register</p>
        </SignIn>
    {/if}
</div>
</div>