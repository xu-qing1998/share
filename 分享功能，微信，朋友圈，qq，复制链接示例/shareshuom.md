## 分享功能，qq，微信，朋友圈，复制链接

### 插件说明
1. 方便用户实现分享功能
2. 快捷方便，分享内容自定义
3. 注意在manifest.json配置分享
--------------------------
### 插件使用
1. 下载插件包,导出components文件。
2. 页面引用文件
```
		<!-- 引入插件 -->
			import uniPopup from '../../components/uni-popup/uni-popup.vue';
			import shareBtn from '../../components/sharebtn/sharebtn.vue';
		<!-- 注册插件 -->
			components: {
				uniPopup,
				shareBtn
			}
```
3. 页面中调用
```
        <uni-popup ref="sharepopup" type="bottom">
			<share-btn :sharedataTemp="sharedata"></share-btn>
		</uni-popup>
```
4. 触发分享弹窗
```
         this.$refs.sharepopup.open();
```
--------------------------------------------
### 参数说明
|变量名				|类型	|默认	|说明											|
|--					|--		|--		|--	
|sharedata			|object	|		|传给插件的分享内容												
|type				|Number	|1	|分享形式，具体请参照开发文档分享板块type值说明	|
|strShareUrl		|string	|	|分享的h5网址链接								|
|strShareTitle		|string	|	|分享标题名										|
|strShareSummary	|string	|	|分享内容介绍									|
|strShareImageUrl	|string	|	|分享的图片										|

