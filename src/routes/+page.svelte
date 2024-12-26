<script>
	import { onMount } from 'svelte';

	let texts = [
		// Affirmative
		"Yes", "Definitely", "Certainly", "Absolutely", "Of course",
		"Sure", "Agreed", "Alright", "Okay", "Fine", "Affirmative",
		"Indeed", "Aye", "Right", "Totally",

		// Negative
		"No", "Never", "Absolutely not", "Not at all", "Negative",
		"Nope", "Nah", "Not really", "No way", "By no means",

		// Uncertain
		"Maybe", "Perhaps", "Possibly", "Probably", "Could be",
		"Might be", "Unsure", "Not sure", "Doubtful", "It depends",

		// Hesitation
		"Hmm", "Err", "Uh-huh", "Well…", "Let me think",
		"I guess", "Not exactly",

		// Agreement/Disagreement Nuances
		"Sounds good", "Agreed", "Disagreed", "That works",
		"Not quite", "Fair enough",

		// Others
		"Why not", "I don’t think so"
	];
	let selectedText = "";

	function getRandomText() {
		const randomIndex = Math.floor(Math.random() * texts.length);
		selectedText = texts[randomIndex];
	}

	onMount(() => {
		getRandomText(); // Initialize with a random text
	});
</script>


<div class="my-auto pt-12">
<h1 class="text-2xl lg:text-6xl text-center">is Siravij At Central World!?</h1>
<h1 class="text-2xl lg:text-5xl text-center my-14">{selectedText}</h1>
<div class="  flex flex-col items-center">
<button class=" mx-auto w-fit content-center text-3xl bg-amber-400 hover:bg-amber-200 p-4 rounded-2xl" on:click={getRandomText}>Check again</button>
</div></div>