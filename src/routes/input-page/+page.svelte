<script lang="ts">
    import { TextInput, Button, Paper, theme } from '@svelteuidev/core';

    import { content } from '../stores';

    function clearContent() {
        $content = "";
    }
</script>
<Paper override={{fontFamily: theme.fonts.standard}}>
    <h1>Text input app</h1>

    <TextInput bind:value={$content} 
    placeholder="Try typing something..." 
    label={$content || "This text will change"}
    />

    <br/>

    <Button on:click={clearContent}>
        Click to clear
    </Button>   
</Paper>
