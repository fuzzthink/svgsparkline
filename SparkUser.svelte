<script>
import Sparkline from './Sparkline.svelte'

export let d = []

const sparkData = (d=[]) => {
  return {
    valuesStr: d.map(o => o.close).join(','),
    length: d.length,
    segments: C.batchDays,
    close: d.slice(-1)[0].close,
  }
}
</script>

<div>
  <Sparkline d={sparkData(d.quotes)}/>
</div>