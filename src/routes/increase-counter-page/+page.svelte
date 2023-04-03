<script lang="ts">
    import { Button, theme } from "@svelteuidev/core";
    import { Paper } from "@svelteuidev/core";

    import { count } from '../stores';

    function increase() {
        count.update(n => n + 1);   
    }

    let countValue: number;

    const unsubscribe = count.subscribe(value => {
		countValue = value;
	});

</script>

<Paper override={{fontFamily: theme.fonts.standard}}>
    <h1>Increase counter</h1>

    <p>Counter is {countValue}</p>  
    <Button on:click={increase}>Increase</Button>
</Paper>


