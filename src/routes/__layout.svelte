<script>
	import Nav from '$lib/Nav.svelte';

	import { Amplify } from 'aws-amplify';
	import config from '../aws-exports.js';
	Amplify.configure(config);
</script>

<Nav />
<slot />
