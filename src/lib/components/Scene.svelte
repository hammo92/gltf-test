<script lang="ts">
	import { T } from '@threlte/core';
	import { ContactShadows, Grid, OrbitControls } from '@threlte/extras';
	import Model from './models/Cowboy_Male.svelte';
</script>

<T.PerspectiveCamera makeDefault position={[-20, 20, 20]} fov={20}>
	<OrbitControls autoRotate enableZoom={false} enableDamping autoRotateSpeed={0.5} target.y={1.5} />
</T.PerspectiveCamera>

<T.DirectionalLight intensity={0.8} position.x={5} position.y={10} />
<T.AmbientLight intensity={0.2} />

<Grid
	position.y={-0.001}
	cellColor="#ffffff"
	sectionColor="#ffffff"
	sectionThickness={0}
	fadeDistance={25}
	cellSize={2}
/>

<ContactShadows scale={10} blur={2} far={2.5} opacity={0.5} />

<Model />
<Model position={[1, 1, 1]} />
