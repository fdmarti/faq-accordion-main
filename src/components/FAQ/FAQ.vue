<template>
	<div class="faq-card">
		<section class="title-faq">
			<img src="/images/icon-star.svg" alt="icon svg star" />
			<h1>FAQs</h1>
		</section>
		<section class="options">
			<OptionComponent
				v-for="question in Questions"
				:title="question.title"
				:content="question.content"
			/>
		</section>
	</div>
</template>

<script setup>
	import './FAQ.css';
	import { OptionComponent } from '../shared';
	import { Questions } from '../../data/Questions.js';
</script>
