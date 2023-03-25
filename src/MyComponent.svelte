<script>
	export let title;
    let fruits = [
        {id: 1, text: 'Apple'},
        {id: 2, text: 'Orange'},
        {id: 3, text: 'Banana'},
        {id: 4, text: 'Mango'}
    ];
    let value = {id: 1, text: 'Apple'};
</script>

<div class="container">
    <div class="d-flex justify-content-center">
        <h1 class="mt-3">{title}</h1>
    </div>

    <div class="card">
        <div class="card-body">
            <h5 class="card-title">Card Title</h5>
            <h6 class="card-subtitle mb-2 text-muted">Card Subtitle</h6>
            <div class="row align-items-end">
                <div class="col-md-4">
                    <div class="form-group">
                        <label for="select-endweek-day">Select an option...</label>
                        <select bind:value label="Select Menu" class="form-control">
                            {#each fruits as fruit}
                              <option value={fruit}>{fruit.text}</option>
                            {/each}
                        </select>
                    </div>
                </div>
                <div class="col-md-4">
                    <p>Seleted: {value.id} - {value.text}</p>
                </div>
                <div class="col-md-2">
                    <button type="button" class="btn btn-primary align-middle">Salvar</button>
                </div>
            </div>
        </div>
    </div>
</div>