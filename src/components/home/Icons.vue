<template>
	<div class='icons'>
		<ul>
			<li v-for='item in iconsList'>
				<img :src="item.imgUrl" alt="">
				<p>{{item.title}}</p>
			</li>
		</ul>
	</div>
</template>

<script>
export default{
	data () {
		return {
			iconsList:[
				{
					id:0,
					imgUrl:'img/icons1.png',
					title:"国内游"
				},
				{
					id:1,
					imgUrl:'img/icons2.png',
					title:"出境游"
				},
				{
					id:2,
					imgUrl:'img/icons3.png',
					title:"周边游"
				},
				{
					id:3,
					imgUrl:'img/icons4.gif',
					title:"当地玩乐"
				},
				{
					id:4,
					imgUrl:'img/icons5.png',
					title:"活动赛事"
				},
				{
					id:5,
					imgUrl:'img/icons6.png',
					title:"摄影游"
				},
				{
					id:6,
					imgUrl:'img/icons7.png',
					title:"亲子游"
				},
				{
					id:7,
					imgUrl:'img/icons8.png',
					title:"户外游"
				},
				{
					id:8,
					imgUrl:'img/icons9.png',
					title:"主题游"
				},
				{
					id:9,
					imgUrl:'img/icons1.png',
					title:"定制游"
				}
			]
		}
	}
}
</script>

<style scoped>
.icons{
	padding-top:.4rem;
	padding-bottom:.1rem;
	border-bottom:1px solid #eee;
}
ul{
	overflow: hidden;
}
ul li{
	width: 20%;
	float:left;
	margin-bottom:.4rem;
}
ul li img{
	margin-left:auto;
	margin-right: auto;
	display: block;
	width: 1.0666666667rem;
	height: 1.0666666667rem;
}
ul li p{
	font-size:.3733333333rem;
	text-align: center;
	margin-top:.1rem;
	color:#333;
}

</style>