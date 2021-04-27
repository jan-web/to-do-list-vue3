<template>
		<!-- <el-row>
			<el-col :xs="2" :sm="4" :md="6" :lg="7" :xl="9"
				><div class="grid-content bg-purple"></div
			></el-col>
			<el-col :xs="10" :sm="8" :md="6" :lg="5" :xl="6"> -->
			<ToDo />

			<!-- </el-col>
			<el-col :xs="2" :sm="4" :md="6" :lg="7" :xl="9"
				><div class="grid-content bg-purple"></div
			></el-col>
		</el-row> -->

</template>

<script>

import ToDo from "@/components/ToDo.vue";

export default ({
	setup() {
		return {

		};
	},
	data() {
		return {

		};
	},
	components: {
		ToDo,
	},
});
</script>

<style>
/* #app {
	font-family: "Roboto", sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
} */
.el-row {
	margin-bottom: 20px;
	&:last-child {
		margin-bottom: 0;
	}
}
.el-col {
	border-radius: 4px;
}
.bg-purple-dark {
	background: #99a9bf;
}
.bg-purple {
	background: #d3dce6;
}
.bg-purple-light {
	background: #e5e9f2;
}
.grid-content {
	border-radius: 4px;
	min-height: 36px;
}
.row-bg {
	padding: 10px 0;
	background-color: #f9fafc;
}
</style>
