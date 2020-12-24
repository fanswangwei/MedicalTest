<template>
	<view class="page-home">
		<view class="home-info">
			<image src="/static/images/home_index.png" mode="" />
		</view>
		<view class="home-list">
			<view class="home-list-title">
				<text class="title">模拟考试</text>
				<view class="tips">
					<text>距离2021年考试还有150天 </text>
					<text>2021年护考时间：预计5月15日-18日 </text>
				</view>
			</view>
			<view class="list-box">
				<view class="list-item" v-for="(item, index) in testList" :key="index">
					<text>药学专业知识（{{ index + 1 }}）</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			testList: [{}, {}, {}, {}, {}, {}, {}, {}, {}],
		}
	},
	onLoad() {},
	methods: {
		pageJump(path) {
			// uni.navigateTo({ url: path })
		},
	},
}
</script>

<style lang="scss" scoped>
.page-home {
	width: 100%;
	.home-info {
		width: 100%;
		height: 161px;
		position: relative;
		image {
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 161px;
		}
	}
	.title {
		font-family: 'PingFang SC';
		font-size: 18px;
		font-weight: 600;
		color: #666;
	}
	.home-list {
		padding: 10px 15px;
		.home-list-title {
			display: flex;
			align-items: center;
			justify-content: space-between;
			.title {
				width: 35%;
			}
			.tips {
				width: 65%;
				text {
					display: block;
					color: #666666;
					font-family: 'PingFang SC';
					font-size: 14px;
					line-height: 20px;
					text-align: right;
					&:last-child {
						line-height: 16px;
						font-size: 10px;
					}
				}
			}
		}
		.list-box {
			.list-item {
				width: 100%;
				height: 50px;
				line-height: 50px;
				box-sizing: border-box;
				text-align: center;
				border: 1px solid #008446;
				border-radius: 8px;
				margin-top: 10px;
				margin-bottom: 5px;
				text {
					color: #008476;
					font-size: 20px;
					font-weight: bold;
					line-height: 24px;
				}
			}
		}
	}
}
</style>
