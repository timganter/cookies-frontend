<script lang="ts">
	let eatCookieResponse: any;

	const eatCookie = async () => {
		const response = await fetch('http://localhost:3333/eat-cookie', { credentials: 'include' });
		eatCookieResponse = await response.json();
	};

	let bakeCookieResponse: any;

	const bakeCookie = async () => {
		const response = await fetch('http://localhost:3333/bake-cookie', { credentials: 'include' });
		bakeCookieResponse = await response.json();
	};

	console.log('bakeCookieResponse', bakeCookieResponse);
	console.log('eatCookieResponse', eatCookieResponse);
</script>

<button on:click={bakeCookie}>Bake Cookie</button>

<button on:click={eatCookie}>Eat Cookie</button>

<h2>Bake Cookie Response</h2>

<code>{bakeCookieResponse?.value}</code>

<h2>Eat Cookie Response</h2>

<code>{eatCookieResponse?.value}</code>
