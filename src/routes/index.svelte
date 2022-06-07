<script>
import EntityElement from "/src/EntityElement.svelte";
	let UtteranceAmount = 0;

    function AddUtterance() {
        UtteranceAmount += 1;
    }

    function AddEntityBox() {
        const element = new EntityElement({
            target: document.getElementById("Entities")
        })
    }

</script>

<h1>Luis Batch Test Generator</h1>

<form width="100%">
    <input id="utterance" placeholder="Enter your utterance.">
    <input id="intent" placeholder="Enter your intent.">

    <p id="Entities">
        <button on:click={AddEntityBox} type="button" id="EntityButton">Add Entity</button>
        <entity></entity>
    </p>   
</form>

<p>
    <button on:click={AddUtterance}>Add Record</button>
</p>

<p>Amount of Utterance added: {UtteranceAmount}</p>
<button>Download JSON</button>