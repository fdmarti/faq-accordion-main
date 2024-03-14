<template>
	<div class="option" @click="handleClickShowContent">
		<div class="title-option">
			<h3>{{ title }}</h3>
			<img src="/images/icon-plus.svg" alt="icon option" class="icon-option" />
		</div>
		<div class="content-option" v-if="showContent">
			<p>{{ content }}</p>
		</div>
	</div>
</template>
<script setup>
	import './OptionComponent.css';
	import { ref } from 'vue';

	const props = defineProps({
		title: String,
		content: String,
	});

	const { title, content } = props;

	const showContent = ref(false);

	const handleClickShowContent = () => (showContent.value = !showContent.value);
</script>
