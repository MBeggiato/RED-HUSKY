<script lang="ts">
    import { SquareArrowOutUpRight } from 'lucide-svelte';

    let { text, url, isExternal } = $props();
</script>

<span class="link-container gap-1">
    <a href={url} target="_blank">{text}</a>
    {#if isExternal}
        <SquareArrowOutUpRight size={16}/>
    {/if}
</span>

<style>
    .link-container {
        display: inline-flex;
        align-items: center;
    }
    a {
        color: var(--color-primary);
        text-decoration: underline;
    }
</style>
