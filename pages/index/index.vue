<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title" id="ssss">测试一下fields测试一下fields测试一下fields测试一下fields测试一下fields测试一下fields测试一下fields测试一下fields测试一下fields测试一下fields</text>
		</view>
		<button @click="test">点我</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			test(){
				let view = uni.createSelectorQuery().select("#ssss");
				view.fields({
					size: true
				}, function(data){
					console.log(data);
				}).exec();
			}
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
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50upx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
