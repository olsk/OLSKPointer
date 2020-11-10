<script>
export let OLSKPointerSize = 20;
export let OLSKPointerStroke = 2;
</script>

<div class="OLSKPointer" style="--OLSKPointerSize: { OLSKPointerSize }px; --OLSKPointerStroke: { OLSKPointerStroke }px; "></div>

<style>
.OLSKPointer {
	width: calc(var(--OLSKPointerSize) * 2);
	height: calc(var(--OLSKPointerSize) * 2);
	/*border: rgba(255, 255, 255, 0) var(--OLSKPointerStroke) solid;*/
	border-radius: calc(var(--OLSKPointerSize) * 2);

	position: absolute;
	top: 50%;
	left: 50%;
	z-index: 99999999;
	
	background: linear-gradient(#eee, #ddd);
	box-shadow:
		inset 0 -1px 1px rgba(0, 0, 0, 0.5),
		inset 0 1px 1px rgba(255, 255, 255, 0.8);
	opacity: 0.9;
}

:global(.OLSKPointerActive) {
	background: linear-gradient(#ddd, #eee) !important;
}
</style>
