<script>
	import { fns, AppShell, Navbar, Header, Title, Divider, SimpleGrid } from '@svelteuidev/core';
    import { SvelteUIProvider } from '@svelteuidev/core';
</script>

<SvelteUIProvider>
    <AppShell>
        <Navbar width={{
            sm: 200,
            lg: 200,
            base: 100
        }} slot="navbar">
            <nav>
                <SimpleGrid cols={1}>
                    <div style="padding-top: 1.5em">
                        <a href="/">Home</a>
                    </div>
                    <Divider/>
                    <div>
                        <a href="/input-page">Text input app</a>
                    </div>
                    <Divider/>
                    <div>
                        <a href="/increase-counter-page">Increase counter</a>
                    </div> 
                    <Divider/>  
                    <div>
                        <a href="/decrease-counter-page">Decrease counter</a>
                    </div> 
                </SimpleGrid>
            </nav>
        </Navbar>
        <Header height="3em" slot="header">
            <Title style="padding-top: 0.15em; padding-left: 0.6em" order={1} variant='gradient' gradient={{from: 'blue', to: 'red', deg: 45}}>
                Labs task 
            </Title>
        </Header>
    
        <slot></slot>
    </AppShell>
</SvelteUIProvider>

    <style>
    a {
        text-decoration: none;
        color: black;
        padding-left: 1em;
        font-size: 20px;
    }
    a:hover {
        color: indianred;
    }
    div > a {
        text-align: center;
    }
</style>