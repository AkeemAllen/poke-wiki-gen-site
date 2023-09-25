<script lang="ts">
	import Navigation from '$lib/Navigation/Navigation.svelte';
	import { AppBar, AppShell, LightSwitch } from '@skeletonlabs/skeleton';
	import '../app.postcss';
</script>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-0 lg:w-64">
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<div class="flex items-center">
        <button class="lg:hidden btn btn-sm mr-4">
            <span>
                <svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
                    <rect width="100" height="20" />
                    <rect y="30" width="100" height="20" />
                    <rect y="60" width="100" height="20" />
                </svg>
            </span>
        </button>
        <strong class="text-xl uppercase">Poke Wiki Gen</strong>
    </div>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<LightSwitch />	
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/AkeemAllen/poke-wiki-gen"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<Navigation/>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
