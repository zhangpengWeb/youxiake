<template>
	<header>
		选择城市
		<i class='iconfont' @click='toHome'>&#xe6fe;</i>
	</header>
</template>

<script>
export default{
	methods:{
		toHome(){
			this.$router.push({
				path:"/"
			})
		}
	}
}
</script>

<style scoped>
header{
	background: #fed101;
	text-align: center;
	height: 1.173rem;
	line-height: 1.173rem;
	color: #333;
	font-size:.4rem;
	position: relative;
}
header i{
	position: absolute;
	right: .3rem;
	font-weight: 700;
}
</style>