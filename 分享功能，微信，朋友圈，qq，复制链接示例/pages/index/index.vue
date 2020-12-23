<template>
	<view class="content">
		<button type="button" @click="shareOn">分享</button>
		<!-- 分享弹窗 -->
		<uni-popup ref="sharepopup" type="bottom">
			<share-btn :sharedataTemp="sharedata"></share-btn>
		</uni-popup>
	</view>
</template>

<script>
	import uniPopup from '../../components/uni-popup/uni-popup.vue';
	import shareBtn from '../../components/share-btn/share-btn.vue';
	export default {
		data() {
			return {
				sharedata: {
					type: 1,
					strShareUrl: "http://www.baidu.com",
					strShareTitle: "分享标题",
					strShareSummary: "分享总结",
					strShareImageUrl: "http://www.xuelejia.com/xljapp/h5/static/aboutUsLogo.png"
				},
			}
		},
		onLoad() {

		},
		methods: {
           shareOn(){
			   this.$refs.sharepopup.open();
		   }
		},
		components: {
			uniPopup,
			shareBtn
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
