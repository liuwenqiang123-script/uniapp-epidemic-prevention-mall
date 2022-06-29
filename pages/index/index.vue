<template>
	<view class="content">
		<view class="">导航跳转学习</view>
			<navigator url="/pages/detail/detail">跳转详情页</navigator>
			<navigator url="/pages/message/message" open-type="switchTab">跳转信息页</navigator>
		
		<uni-calendar 
		    :insert="true"
		    :lunar="true" 
		    :start-date="'2022-3-2'"
		    :end-date="'2023-5-20'"
		    @change="change"
		     />
		<image class="logo" src="/static/tabs/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
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
		change(e){
			console.log(e);
		},
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
