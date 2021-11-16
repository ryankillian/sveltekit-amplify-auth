<script>
	import { Auth } from 'aws-amplify';

	const checkUser = () => {
		Auth.currentAuthenticatedUser()
			.then((user) => console.log({ user }))
			.catch((err) => console.log(err));
	};

	const signOut = () => {
		Auth.signOut()
			.then((data) => console.log(data))
			.catch((err) => console.log(err));
	};
</script>

<h1>Login page</h1>

<div>
	<button on:click={() => Auth.federatedSignIn()}>Sign In</button>
	<button on:click={checkUser}>Check User</button>
	<button on:click={signOut}>Sign Out</button>
</div>
