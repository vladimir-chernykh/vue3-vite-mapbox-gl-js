<script setup>
import { onMounted } from 'vue';
import 'mapbox-gl/dist/mapbox-gl.css';

import mapboxgl from 'mapbox-gl';
mapboxgl.accessToken = '<your-token>';

onMounted(() => {
  // TO MAKE THE MAP APPEAR YOU MUST
  // ADD YOUR ACCESS TOKEN FROM
  // https://account.mapbox.com
  const map = new mapboxgl.Map({
      container: 'map', // container ID
      style: 'mapbox://styles/mapbox/streets-v12', // style URL
      center: [-74.5, 40], // starting position [lng, lat]
      zoom: 9, // starting zoom
  });
})

</script>

<template>
  <div>
    Test
  </div>

  <div id="map" style="width:500px;height:500px;">
  </div>
</template>