<script>
	const items = [
		{
			icon: 'icon',
			text: 'text',
			onClick: () => {
				console.log('click');
			}
		},
		{
			icon: 'icon2',
			text: 'text2',
			onClick: () => {
				console.log('click2');
			}
		},
		{
			icon: 'icon3',
			text: 'text3',
			onClick: () => {
				console.log('click3');
			}
		},
		{
			icon: 'icon4',
			text: 'text4',
			onClick: () => {
				console.log('click4');
			}
		}
	];
</script>

<div class="side-bar w-full h-full mx-auto flex justify-center overflow-auto">
	<div class="w-full mx-auto flex m-4 p-10">
        <nav class="list-nav">
            <!-- (optionally you can provide a label here) -->
            <!-- loop through the item in itesm -->
			{#each items as item}
            <ul>
                <li>
                    <button on:click={item.onClick} class="flex items-center w-full px-4 py-2">
                        <span class="badge bg-primary-500">{item.icon}</span>
                        <span class="flex-auto">{item.text}</span>
                    </button>
                </li>
                <!-- ... -->
            </ul>
			{/each}
        </nav>
	</div>
</div>
