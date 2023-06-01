<template>
	<div id="app">
		<h1>To-Do List</h1>
		<to-do-form></to-do-form>>
		<ul>
			<li v-for="item in ToDoItems" :key="item.id">
				<to-do-item :label="item.label" :done="true" :id="item.id"></to-do-item>
			</li>
		</ul>
	</div>
</template>

<script>

import ToDoItem from './components/ToDoItem.vue';
import ToDoForm from './components/ToDoForm.vue';

export default {
	name: "app",
	components: {
		ToDoItem,
		ToDoForm,
	},
	data() {
		return {
			ToDoItems: [
				{ label: "Learn vue", done: false },
				{ label: "Create vue project from CLI", done: true },
				{ label: "Have fun", done: true },
				{ label: "Create a To-Do list", done: false },
			]
		};
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
