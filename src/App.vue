<template>
	<div>
		<button v-on:click="increment">Counter :{{ counter }}</button>
	</div>
</template>

<script>
import { onMounted, ref } from 'vue';

export default {
	setup() {
		// eslint-disable-next-line no-undef
		const counter = ref(0);
		const increment = () => counter.value++;

		onMounted(() => {
			console.log('마운트 출력완료');
		});

		return {
			counter,
			increment,
		};
	},
};
</script>

<style lang="scss" scoped></style>
