<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		
		<switch checked="true"></switch>
		<mycomponent01 v-on:click_out="click_out01"></mycomponent01>
		
		
		 
	</view>
</template>

<script>
	import mycomponent01 from "@/components/mycomponent01.vue"
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			click_out01: function(){
				console.log("click in index.vue ");
			}

		},
		components:{
			mycomponent01,
		}
	}
</script>

<style>
	.content {
        display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
