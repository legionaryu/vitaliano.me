<script lang="ts">
    import { MenuItemName } from "$lib/data/menu"
    
    export let offset = "4rem";
    export let nextSectionId: string;
    export let homeElement: HTMLElement;
</script>

<div bind:this={homeElement}>
    <div
        class="offset-block"
        id={MenuItemName.home}
        style="--offset-size:{offset}"
        >
    </div>
    <div class="home">
        <img class="logo" src="home/Logo_Vitaliano_trim_white.png" alt="Vitaliano">
    </div>
    <a class="arrow-down" href="#{nextSectionId}">🢃</a>
</div>

<style lang="scss">
    .home {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 50vmax;
        background-image: url("$img/home/Vitaliano_profile.jpg");
        background-position: 0 bottom;
        background-repeat: no-repeat;
        background-size: auto 105%;
    }

    .logo {
        height: auto;
        width: 45%;
    }

    .arrow-down {
        display: inline-block;
        font-size: xx-large;
        text-align: center;
        text-decoration: none;
        color: inherit;
        cursor: pointer;
        width: 100%;
    }
</style>