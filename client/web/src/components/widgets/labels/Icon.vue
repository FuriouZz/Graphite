<template>
	<div class="icon" :class="`size-${String(size)}`">
		<slot></slot>
	</div>
</template>

<style lang="scss">
.icon {
	display: inline-block;
	flex: 0 0 auto;
	fill: var(--color-e-nearwhite);
	vertical-align: top;
	width: 16px;
	height: 16px;
	margin-left: 0;

	&.size-10 {
		width: 10px;
		height: 10px;
	}

	&.size-12 {
		width: 12px;
		height: 12px;
	}

	&.size-16 {
		width: 16px;
		height: 16px;
	}

	&.size-24 {
		width: 24px;
		height: 24px;
	}
}
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
	props: {
		size: { type: Number, required: true },
		gapAfter: { type: Boolean, default: false },
	},
});
</script>
