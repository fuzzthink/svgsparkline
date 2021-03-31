<script>
export let d = {}
export let width = 200

import { onMount } from 'svelte'

let ref
onMount(() => {
  Dailychart.create(ref)
})
</script>

<div bind:this={ref} style="width:{width}px"
  data-mc-values={d.valuesStr}
  data-mc-close={d.close}
  data-mc-length={d.length}
  data-mc-segments={d.segments}
></div>