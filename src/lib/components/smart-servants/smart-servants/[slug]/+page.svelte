<script>
    import Advancements from "$lib/components/simulacrum/Advancements.svelte";
    import Abilities from "../../../lib/components/smart-servants/Abilities.svelte";
    import Header from "../../../lib/components/smart-servants/Header.svelte";
    import Effects from "../../../lib/components/smart-servants/Effects.svelte";
    import SectionNavigation from "$lib/components/SectionNavigation.svelte";
    import SvelteMarkdown from "svelte-markdown";
    import Youtube from "$lib/components/Youtube.svelte";
    import Ad from "$lib/components/Ad.svelte";
    import UpgradeMaterials from "$lib/components/smart-servants/UpgradeMaterials.svelte";

    export let data;
</script>

<svelte:head>
    <title>{data.name} | Tower of Fantasy Index</title>
    <meta
        name="description"
        content={`Information about the smart servant ${data.name}.`}
    />
    <meta property="og:title" content={data.name} />
    <meta
        property="og:description"
        content={`Information about the smart servant ${data.name}.`}
    />
    <meta
        property="og:image"
        content={`/images/UI/PetFight/icon/${data.imgSrc}.webp`}
    />
    <meta name="theme-color" content="#377dcb" />
</svelte:head>

<SectionNavigation
    links={["info", "advancements", "abilities", "upgrade materials"]}
/>

<h1>{data.name}</h1>
<span style="color: var(--text2)">
    {#if data.chinaOnly}
        <abbr title="China Exclusive" />
    {/if}
    Smart Servant
</span>

<Header data={data} />

<Ad unit="Banner1" />

<Advancements weapon={data} />

<Ad unit="Banner2" />

<Abilities data={data} />

<Ad unit="Banner3" />

<UpgradeMaterials gifts={data.bestGifts} />

{#if data.videoSrc}
    <h4 id="preview">Preview</h4>
    <Youtube
        source={data.videoSrc}
        caption={`The ${data.name} used in this video is ${data.starsInVideo}★`}
    />
{/if}
