<template>
	<div class='like'>
		<div class='like-list' v-for='item in likeList'>
			<div class='like-top'>
				<div class='top-left'>
					<span>{{item.title}}</span>
				</div>
				<p class='top-right'>更多></p>
			</div>
			<div class='like-bottom'>
				<div 
					class='bottom-header'
					:style="{'background':'url('+item.imgUrl+') no-repeat center center' }"
					@click='toDetails(item)'
				>
					<div class='header-info'>
						<span>
							{{item.Introduction}}
						</span>
						<span>￥{{item.price}}起</span>
					</div>
				</div>
				<ul>
					<li 
						v-for='v in item.cityList'
						@click='toDetails'
					>
						<img :src="v.imgUrl">
						<span class='title'>{{v.title}}</span>
						<span class='price'>￥{{v.price}}起</span>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default{
	props:['likeList'],
	methods:{
		toDetails(item){
			this.$router.push({
				path:"/details",
				query:{
					item
				}
			})
		}
	}
}
</script>

<style scoped>
.like{
	padding-bottom:1.5rem;
	font-size:.35rem;
	margin-top:.7rem;
}
.like-list{
	margin-top:.4rem;
}
.like-top{
	display: flex;
	justify-content: space-between;
}
.like-top .top-left{
	position: relative;
}
.like-top .top-left:before{
	position: absolute;
	content:"";
	background: #fed101;
	width: .1rem;
    height: .48rem;
    top:0;
}
.like-top .top-left span{
	padding-left: .5rem;
	font-size:.5rem;
}
.like-top .top-right{
	padding-right: .5rem;
	color: #999;
	font-weight: 500;
	font-size:.4rem;

}

.like-bottom{
	padding:.3rem;
}
.like-bottom .bottom-header{
	position: relative;
	height: 4.4666666rem;
	width: 100%;
	background-size:100%;
}
.like-bottom .bottom-header .header-info{
	position: absolute;
	bottom:.26rem;
	left:.2rem;
	display: flex;
	justify-content: space-between;
}
.like-bottom .bottom-header .header-info span:nth-child(1){
	font-size:.5rem;
	color:#fff;
	font-weight: 700;
	width: 5.78rem;
	white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
}
.like-bottom .bottom-header .header-info span:nth-child(2){
	font-size:.5rem;
	color:orange;
	font-weight: 500;
	font-size:.45rem;
	margin-left:1rem;
}
.like-bottom ul{
	display: flex;
	justify-content: space-between;
	margin-top:.3rem;
}
.like-bottom ul li{
	width: 2.96rem;
}
.like-bottom ul li img{
	width: 100%;
	height: 1.9584rem;
}
.like-bottom ul li span.title{
	font-size:.35rem;
	display: block;
	margin-top:.2rem;
	height: .6933333rem;
	width: 100%;
	display: block;
	-webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
}
.like-bottom ul li span.price{
	margin-top:.2rem;
	display: block;
	font-size:.5rem;
	color:orange;
	font-weight: 500;
	font-size:.35rem;
}
</style>