<script lang="ts">
	let date = '05-12-25 8:00';
	let futueDate = new Date(date).getTime();
	let differenceInDays: Number;

	function calc() {
		let timeInBetween = futueDate - new Date().getTime();
		differenceInDays = Math.round(timeInBetween / (1000 * 3600 * 24));
	}
	calc();
	setInterval(calc, 5000);
</script>

<slot>Days until finals: {differenceInDays} days</slot>
