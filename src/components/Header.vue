<template>
	<header>
		<h1>{{ title }}</h1>
		<Button
			@btn-click="$emit('toggle-add-task')"
			:text="showAddTask ? 'Close' : 'Add Task'"
			:color="showAddTask ? 'red' : 'green'"
		/>
	</header>
</template>

<script>
import Button from "./Button";

export default {
	name: "Header",
	props: {
		title: String,
		showAddTask: Boolean,
	},
	components: {
		Button,
	},
};
// lot of interesting ways to set up props in vue.js, check 31:30 on the vue crash course https://www.youtube.com/watch?v=qZXt1Aom3Cs&list=LL&index=6
</script>

<style scoped>
/* scoped means that any styling declared here will only be used for this component */
header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
}
</style>
