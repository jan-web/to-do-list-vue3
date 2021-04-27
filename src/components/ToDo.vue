<template>
	<div class="wrapper">
		<h4 class="text-center">Today tasks</h4>

		<el-space direction="vertical" :size="20" alignment="flex-start">
			<span v-if="tasks.length !== 0" >
				<span v-for="task in tasks" :key="task._id">
					<ElCheckbox v-model="task.checked" @click="isChecked(task._id)">{{
						task.name
					}}</ElCheckbox>
				</span>
			</span>

			<el-space :size="20">
				<ElInput
					placeholder="Add new task to to do list"
					v-model="input"
				></ElInput>
				<ElButton
					type="success"
					icon="el-icon-plus"
					circle
					@click="addNewTask"
				></ElButton>
			</el-space>
		</el-space>
	</div>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
	setup() {
		return {
			input: ref(""),
		};
	},
	data() {
		return {
			tasks: [],
		};
	},
	components: {},
	methods: {
		isChecked(mark) {
			console.log(mark);
		},
		addNewTask() {
			console.log(this.input);
			if (this.input) {
				this.tasks.push({
					_id: Math.random(),
					name: this.input,
					checked: false,
				});
				this.input = "";
			}
		},
	},
});
</script>

<style scoped lang="scss">
.wrapper {
	max-width: 280px;
	margin: auto;
}
.text-center {
	text-align: center;
}
.flex {
	display: flex;
	justify-content: left;
	align-items: center;
}
</style>
