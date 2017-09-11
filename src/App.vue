<template>
	<div id="app" class="flex-col">

		<header class="keyline-bottom keyline-lighten0 title3d">map.coffee</header>
		<div class="stretch" style="position: relative;">
			<MapGL></MapGL>
		</div>

	</div>
</template>


<script>
	import MapGL from './components/Map/Map.vue'

	export default {
		components: {
			MapGL
		}
	}
</script>

<style>
	html {
		height: 100%;
	}

	#app {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		height: 100%;
		width: 100%;
	}

	.keyline-bottom {
		border-bottom-width: 1px;
		border-bottom-style: solid;
		border-bottom-color: rgba(0, 0, 0, 0.1);
	}

	.dark .keyline-lighten0, .keyline-lighten0 {
		border-top-color: rgba(255, 255, 255, 0.1);
		border-right-color: rgba(255, 255, 255, 0.1);
		border-bottom-color: rgba(255, 255, 255, 0.1);
		border-left-color: rgba(255, 255, 255, 0.1);
	}

	header {
		font-size: 2rem;
		line-height: 2rem;
		text-align: right;
		background-color: rgb(89, 91, 91);
		color: rgb(255, 255, 255);
		min-height: 50px;
	}

	.title3d {
		padding-top: 0px;
		padding-right: 1.25rem;
		padding-bottom: 0px;
		padding-left: 1.25rem;
		height: 3rem;
		line-height: 3rem;
		letter-spacing: 1px;
		color: rgb(198, 200, 200);
		text-shadow: rgba(0, 0, 0, 0.69) 0px -1px;
	}

	.fill-canvas {
		background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAUCAQAAAAngNWGAAAAGElEQVR4AWNgkMECsQA6KxxVOFjdPaoQAAMRFeEKd2mnAAAAAElFTkSuQmCC);
		background-size: 10px 10px
	}

</style>
