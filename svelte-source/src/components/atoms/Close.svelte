<script lang="ts">
	import CloseSVG from './svgs/CloseSVG.svelte';
	import PanelStore from "../../stores/PanelStore";

	function closeClicked(): void {
		PanelStore.close();
	}
</script>

<div class={"close_bg w-full h-[60px] flex justify-center items-center cursor-pointer duration-200 "}
	on:click={() => closeClicked()}>
	<div class="close">
		<svelte:component this={CloseSVG}/>
	</div>
</div>

<style>
	.close {
		width: 40%;
		color: var(--color-grey);
	}
	.close:hover {
		width: 50%;
		color: var(--color-red);
	}
	.close_bg:hover {
		background-color: var(--color-darkestblue);
	}
</style>