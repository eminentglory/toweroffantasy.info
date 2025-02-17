<script>
    import SvelteMarkdown from "svelte-markdown";
    import puzzles from "$lib/data/exploration/exploration.json";
    import SectionNavigation from "$lib/components/SectionNavigation.svelte";
    import { onMount } from "svelte";
    import AnchorJS from "anchor-js";
    import Ad from "$lib/components/Ad.svelte";
    onMount(() => {
        const anchors = new AnchorJS();
        anchors.add("h3");
    });
</script>

<svelte:head>
    <title>Exploration | Tower of Fantasy Index</title>
    <meta name="description" content="Exploration puzzles are a core feature of Tower of Fantasy. By completing them you can gain a considerable amount of black and gold nuclei, dark crystals, and other resources.">
    <meta property="og:title" content="Exploration" />
    <meta
        property="og:description"
        content="Exploration puzzles are a core feature of Tower of Fantasy. By completing them you can gain a considerable amount of nuclei, dark crystals, and other resources."
    />
    <meta
        property="og:image"
        content="/images/Icon/huobi/Gem004.webp"
    />
    <meta name="theme-color" content="#377dcb" />
</svelte:head>

<SectionNavigation links={["innars","miasmic swamp","abyss", "grayspace", "mirroria", "vera", "aesperia"]} />
<h1>Exploration</h1>

<Ad unit="Banner1" />

<h2 id="innars">Innars</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "innars") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h2>{puzzle.name}</h2>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<Ad unit="Banner2" />

<h2 id="miasmic-swamp">Miasmic Swamp</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "miasmic swamp") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h2>{puzzle.name}</h2>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<Ad unit="Banner3" />

<h2 id="abyss">Confounding Abyss</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "disorderly abyss") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h2>{puzzle.name}</h2>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<Ad unit="Banner4" />

<h2 id="grayspace">Grayspace & Twilight Zone</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "gray zone" || p.location === "dark zone") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h2>{puzzle.name}</h2>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<Ad unit="Banner5" />

<h2 id="mirroria">Mirroria</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "mirroria") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h2>{puzzle.name}</h2>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<Ad unit="Banner6" />

<h2 id="vera">Vera</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "vera") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h2>{puzzle.name}</h2>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<Ad unit="Banner7" />

<h2 id="aesperia">Aesperia</h2>
<div class="table-wrapper">
    <table class="bg-alternate">
        <thead>
            <th>Puzzle</th>
            <th>Solution</th>
        </thead>
        <tbody>
            {#each puzzles.filter(p => p.location === "aesperia") as puzzle}
                <tr>
                    <td>
                        <div class="img-and-name">
                            <img
                                src={`/images/exploration/${puzzle.imgSrc}.webp`}
                                alt={puzzle.name}
                                width="150"
                                height="120"
                                loading="lazy"
                            />
                            <h3>{puzzle.name}</h3>
                        </div>
                    </td>
                    <td>
                        <SvelteMarkdown source={puzzle.solution} />
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>