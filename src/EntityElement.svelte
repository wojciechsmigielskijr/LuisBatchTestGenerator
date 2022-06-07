<script>
    let EntityExists = false;

    function AddSubEntityBox(elem) {
        var inputEntity = document.createElement("input");
        inputEntity.placeholder = "Enter the Sub Entity."
        inputEntity.className = "LuisSubEntity";
        var inputEntityText = document.createElement("input");
        inputEntityText.placeholder = "Enter the text that features the Sub entity."
        inputEntityText.className = "SubEntityText";
        var ptag = document.createElement("p");

        var element = elem.srcElement.parentElement;

        console.log(element);

        element.append(ptag)
        element.append(inputEntity);
        element.append(inputEntityText);

    }
</script>

<p class="Entity">
    <p> <b>Entity</b> </p>
    <input class="LuisEntity" placeholder="Enter Your Entity">
    <input class="EntityText" placeholder="Enter Your the text of the entity">
    <p class="SubEntity">
        <button on:click={AddSubEntityBox} type="button">Add Sub Entity</button>
    </p>     