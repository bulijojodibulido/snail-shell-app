<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	@import "./common/uni.css";
	/* page,view{
		display: flex;
	} */
	
	@font-face {
	  font-family: 'iconfont';  /* project id 1698511 */
	  src: url('//at.alicdn.com/t/font_1698511_foou1hgu68u.eot');
	  src: url('//at.alicdn.com/t/font_1698511_foou1hgu68u.eot?#iefix') format('embedded-opentype'),
	  url('//at.alicdn.com/t/font_1698511_foou1hgu68u.woff2') format('woff2'),
	  url('//at.alicdn.com/t/font_1698511_foou1hgu68u.woff') format('woff'),
	  url('//at.alicdn.com/t/font_1698511_foou1hgu68u.ttf') format('truetype'),
	  url('//at.alicdn.com/t/font_1698511_foou1hgu68u.svg#iconfont') format('svg');
	}
	.iconfont {
		font-family: "iconfont" !important;
		font-size: 16px;
		font-style: normal;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
	}
	.icon-vip1:before{
		content:'\e701';
	}
	.icon-order:before{
		content:'\e628';
	}.icon-unpaided:before{
		content:'\e612';
	}
	.icon-unserviced:before{
		content:'\e625';
	}
	.icon-unensured:before{
		content:'\e627';
	}
	.icon-unevaluated:before{
		content:'\e627';
	}
	.icon-postsale:before{
		content:'\e70b';
	}
	
	// 下方部分
	.icon-history:before{
		content:'\e614';
	}
	.icon-address:before{
		content:'\e67b';
	}
	.icon-share:before{
		content:'\e63e';
	}
	.icon-member:before{
		content:'\e63a';
	}
	.icon-service:before{
		content:'\e9b2';
	}
	.icon-setting:before{
		content:'\e613';
	}
	.icon-arrow-left:before{
		content:'\e632';
	}
	.icon-arrow-right:before{
		content: '\e60e';
	}
	.icon-edit:before{
		content: '\e6b0';
	}
	.icon-map:before{
		content: '\e629';
	}
	.icon-arrow-down:before{
		content: '\e648';
	}
	.icon-mobile:before{
		content: '\e791'
	}
	.icon-remark:before{
		content: '\e640'
	}
	.icon-coupon:before{
		content: '\e645'
	}
	.icon-sandy-clock:before{
		content: '\e66f'
	}
	.icon-floor-area:before{
		content: '\e61d'
	}
	.icon-wxpay:before {
		content: "\e600";
	}
	.icon-alipay:before {
	    content: "\e68a";
	}
	.icon-balance:before {
	    content: "\e78a";
	}
	.icon-ok:before{
		content: '\e63c';
	}
	/* public */
	
	
	
	
	
	view,
	scroll-view,
	swiper,
	swiper-item,
	cover-view,
	cover-image,
	icon,
	text,
	rich-text,
	progress,
	button,
	checkbox,
	form,
	input,
	label,
	radio,
	slider,
	switch,
	textarea,
	navigator,
	audio,
	camera,
	image,
	video {
		box-sizing: border-box;
	}
	/* 骨架屏替代方案 */
	.Skeleton {
		background: #f3f3f3;
		padding: 20upx 0;
		border-radius: 8upx;
	}
	
	/* 图片载入替代方案 */
	.image-wrapper {
		font-size: 0;
		background: #f3f3f3;
		border-radius: 4px;
	
		image {
			width: 100%;
			height: 100%;
			transition: .6s;
			opacity: 0;
	
			&.loaded {
				opacity: 1;
			}
		}
	}
	
	/*
		全局公共样式和字体图标
	*/

	.clamp {
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
		display: block;
	}
	
	.common-hover {
		background: #f5f5f5;
	}
	
	/*边框*/
	.b-b:after,
	.b-t:after {
		position: absolute;
		z-index: 3;
		left: 0;
		right: 0;
		height: 0;
		content: '';
		transform: scaleY(.5);
		border-bottom: 1px solid $border-color-base;
	}
	
	.b-b:after {
		bottom: 0;
	}
	
	.b-b:after {
		bottom: 0;
	}
	.b-t:after {
		top: 0;
	}
	
	/* button样式改写 */
	.s-pay-btn{
		display: flex;
		align-items: center;
		justify-content: center;
		width: 630upx;
		height: 84upx;
		margin: 0 auto 30upx;
		border-radius: 10upx;
		box-shadow: 1px 2px 5px rgba(219, 63, 96, 0.4);
		font-size: $font-lg;
		color: #fff;
		background-color: $base-color;
	}
	.s-normal-btn{
		display: flex;
		align-items: center;
		justify-content: center;
		width: 630upx;
		height: 84upx;
		margin: 0 auto 30upx;
		border-radius: 10upx;
		border: 1px solid #ccc;;
		box-shadow: 1px 2px 5px rgba(255, 255, 255, 0.4);
		font-size: $font-lg;
		color: $font-color-dark;
		background-color: #fff;
	}
	
	uni-button,
	button {
		height: 80upx;
		line-height: 80upx;
		font-size: $font-lg + 2upx;
		font-weight: normal;
	
		&.no-border:before,
		&.no-border:after {
			border: 0;
		}
	}
	
	uni-button[type=default],
	button[type=default] {
		color: $font-color-dark;
	}
	
	
	/* input 样式 */
	.input-placeholder {
		color: #999999;
	}
	
	.placeholder {
		color: #999999;
	}
</style>
