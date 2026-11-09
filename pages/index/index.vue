<template>
	<view class="page">
		 <text class="text">
		 	使用分包的方式将插件放入分包，插件不占用主包体积。
			如果小程序插件只在某个分包中使用，无论从代码层面还是性能层面，插件放入分包都是最佳的解决办法。
		 </text>
		<text class="text">
			1、【跳转到分包首页】 
		</text>
		<button @click="gotoIndex" style="margin-top: 10px;">跳转到分包首页</button>
		
		<text class="text">
			2、【跳转到插件组件】 
		</text>
		<button @click="gotoComponent" style="margin-top: 10px;">跳转到插件组件</button>
		
		<text class="text">
			3、【跳转到图集组件】
		</text>
		<button @click="gotoImageComponent" style="margin-top: 10px;">跳转到图集组件</button>
 
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		onLoad() {
			// 测试场景ID由他人创建，可能不稳定，请替换为自己的。
		},
		methods: { 
			// 多图识别组件。
			gotoIndex() {
				wx.navigateTo({
					url: "/pkgPlugin/index/index",
					success: function(res) {}
				})
			},
			// 多图识别组件。
			gotoComponent() {
				wx.navigateTo({
					url: "/pkgPlugin/ar-viewer/index",
					success: function(res) {}
				})
			},
			gotoImageComponent() {
				wx.navigateTo({
					url: "/pkgPlugin/ar-collection/index",
					success: function(res) {}
				})
			}
		}
	}
</script>

<style>
	/* pages/index/index.wxss */
	.page {
		padding: 20px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding-bottom: 50px;
	}

	.text {
		color: #081828;
		font-size: 16px;
		margin-top: 10px;
	}

	.link-image {
		color: #576B95;
		font-size: 16px;
		margin: 0 10px;
	}
</style>