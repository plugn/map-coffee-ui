<template>
	<div class="map" id="map-container"></div>
</template>

<script>
	import mapboxgl from 'mapbox-gl/dist/mapbox-gl.js'
	import glStyle from '../../style.conf'

	mapboxgl.accessToken = 'pk.eyJ1IjoicGx1Z24iLCJhIjoiY2o3Z2Q1dDNmMHo4MTJ4cW12ajNybTl5NCJ9.nmZeZpRdw87yq43Ben7lxg'

	let map;

	export default {
		data() {
			return {};
		},

		mounted() {
			this.initMap();
		},

		methods: {
			initMap() {
				map = new mapboxgl.Map({
					container: this.$el,
					center: [37, 55],
					zoom: 5,
					style: glStyle,
					hash: true // display current zoom and coordinates as a part of URL
				});

				let nav = new mapboxgl.NavigationControl();
				map.addControl(nav, 'top-left');
			}
		}
	}

</script>
<style src="mapbox-gl/dist/mapbox-gl.css"></style>

<style>
	.map {
		height: 100%;
		background-color: ghostwhite;
	}
</style>
