<script>
	import { auth } from "../../lib/firebase/firebase.client";
	import { authStore } from "../../stores/authStore";

	/**
	 * @type {any}
	 */
	let email;
	authStore.subscribe((/** @type {{ currentUser: { email: any; }; }} */ curr) => {
		console.log("CURR", curr);
		email = curr?.currentUser?.email;
	});
</script>

{#if $authStore.currentUser}
	<h1>Current User: {email}</h1>
{/if}
