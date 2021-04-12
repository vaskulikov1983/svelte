<script>
	let name = 'Vasiliy';
	let age = 30;

	const counter = () => age++;  
	$: uppercaseName = name.toUpperCase();
	$: console.log(name);
	$: if (name === 'Fedor') {
		age = 34;
	}

	const changeName = () => name = 'Fedor';

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {uppercaseName}, and my age is {age}!</h1>
<button on:pointerdown = {counter}>Change age</button>
<button on:pointerdown="{changeName}">Change name</button>

