<script context="module" lang="ts">
	export function load({ page }) {
		const { path } = page;
		if (path.startsWith('/foo')) {
			console.log('foo')
			return {
				status: 302,
				redirect: '/'
			}
		}
		return {}
	}
</script>

<h1>THIS IS A LAYOUT</h1>

<slot></slot>