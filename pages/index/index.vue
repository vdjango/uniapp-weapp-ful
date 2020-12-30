<template>
	<view>
		<!-- <u-navbar title="剑未配妥，出门已是江湖"></u-navbar> --> 
		<u-swiper @change="swiper_change" :list="image_list" :mode="swiper.mode" :height="swiper.height" :border-radius="swiper.radius"></u-swiper>
		 
		<view class="content_top" :style="'background:' +image_list[swiper.index].color+ ';'">
			<view class="wrap">
			    <h1> 汉服之美·一醉千年! 
				</h1>
			    <p>以汉服光影人的视角，记录汉服美好瞬间！这里是汉服摄影。照片还是视频？这里统统都有
				</p>
			    <span><a class="learnmore" href="#">我要·约棚</a></span>
			</view>
		</view>
		 
		<view class="content-grids">
		    <view class="wrap">
		        <view class="grid">
		            <a href="#"><img :src="require('assets/grids/1.jpg')" title="image-name"/></a>
		            <h3>我是一号棚</h3>
		            <p>
						这里是，是很长的 一号棚介绍。
						以汉服光影人的视角，记录汉服美好瞬间！这里是汉服摄影。
					</p>
		            <a class="button" href="#">查看详情</a>
		        </view>
				
		            <view class="grid">
		                <a href="#"><img :src="require('assets/grids/2.jpg')" title="image-name"/></a>
		                <h3>我是二号棚</h3>
		                <p>
							这里是，是很长的 一号棚介绍。
							以汉服光影人的视角，记录汉服美好瞬间！这里是汉服摄影。
						</p>
		                <a class="button" href="#">查看详情</a>
		            </view>
		            <view class="grid last-grid">
		                <a href="#"><img :src="require('assets/grids/3.png')" title="image-name"/></a>
		                <h3>我是三号棚</h3>
		                <p>
							这里是，是很长的 一号棚介绍。
							以汉服光影人的视角，记录汉服美好瞬间！这里是汉服摄影。
						</p>
		                <a class="button" href="#">查看详情</a>
		            </view>
		            <view class="clear"></view>
		        </view>
		    </view>
		<!-- <view class="app-wrap">
			<u-row gutter="16" justify="space-between">
				<u-col span="12">
					<view class="demo-layout bg-purple">
						
					</view>
				</u-col>
				<u-col span="12">
					<view class="demo-layout bg-purple-light"></view>
				</u-col>
				<u-col span="12">
					<view class="demo-layout bg-purple-light"></view>
				</u-col>
			</u-row>
		</view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				show: true,
				swiper: {
					mode: "none",
					height: 460,
					radius: 0,
					index: 0
				},
				image_list: [
					{
						color: '#9c7f70',
						image: require('assets/slider1.jpg'),
					},
					{
						color: '#790506',
						image: require('assets/slider2.jpg'),
					},
					{
						color: '#650405',
						image: require('assets/slider3.jpg'),
					},
					{
						color: '#450e03',
						image: require('assets/slider4.jpg'),
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			change(index) {
				this.current = index;
			},
			swiper_change(index) {
				this.swiper.index = index
			}
		}
	}
</script>

<style scoped lang="scss">
	.app-wrap {
		padding: 24rpx;
	}

	.u-row {
		margin: 40rpx 0;
	}

	.demo-layout {
		height: 80rpx;
		border-radius: 8rpx;
	}

	.bg-purple {
		background: #d3dce6;
	}

	.bg-purple-light {
		background: #e5e9f2;
	}

	.bg-purple-dark {
		background: #99a9bf;
	}
	
	
	/*-----*/
	
</style>
<style>
	
	.wrap{
		width:95%;
		margin:0 auto;
		transition:all .2s linear;
		-moz-transition:all .2s linear;/* firefox */
		-webkit-transition:all .2s linear; /* safari and chrome */
		-o-transition:all .2s linear; /* opera */
		-ms-transition:all .2s linear;
	}
	/*----start-header-----*/
	.header{
		background:#323A45;
		border-bottom:2px solid #00B895;
	}
	.logo{
		float: left;
		padding:25px 0;
	}
	.top-nav{
		float:right;
	}
	.top-nav ul li{
		display:inline-block;
		float:left;
	}
	.top-nav ul li a{
		font-family: 'Roboto', sans-serif;
		color: #d6d6d6;
		padding: 40px 25px;
		display: block;
		position: relative;
		text-transform: uppercase;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
		font-size: 0.875em;
		position:relative;
	}
	.top-nav li.active a, .top-nav li a:hover {
		color:#FFF;
		background:#00B895;
	}
	/*---start-content----*/
	.content {
	}
	.content_top{
		/*background-image: url("../images/biaotou.jpg");*/
		/*background-size: cover;*/
		/*background-repeat: round;*/
		padding:50px 0;
		/*height: 100%;*/
		text-align: center;
		font-family: 'Roboto', sans-serif;
		position:relative;
	}
	.content_top:after{
		content: '';
		position:relative;
		width: 0;
		height: 0;
		border:20px solid #FFF;
		border-top: 0 solid rgba(0, 0, 0, 0)!important;
		border-right: 15px solid rgba(0, 0, 0, 0)!important;
		border-left: 15px solid rgba(0, 0, 0, 0)!important;
		left:0%;
		top: 30px;
		margin-left: -10px;
	}
	.content_top h1{
		color: #fff;
		font-size:56rpx;
		padding-bottom:14rpx;
	}
	.content_top span a{
		font-family: 'Roboto', sans-serif;
		color:#ffffff;
		background-color:#009175;
		display: inline-block;
		text-transform: uppercase;
		padding: 10px 20px;
		font-size: 28rpx;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
	}
	.content_top span a:hover{
		background:#222;
	}
	.content_top p{
		font-size:30rpx;
		line-height: 1.8em;
		color: #fff;
		margin-bottom: 24rpx;
		margin: 24rpx 0rpx 34rpx 0rpx;
	}
	.content-grids {
		padding:50px 0;
		background:#FFF;
	}
	.grid{
		width: 100%;
		float:none;
		padding:3%;
		margin:25rpx 0;
		background: #fff;
		border: 1px solid #EBEBEB;
		color: #7e7e7e;
		text-align: center;
		margin-right:6%;
		-webkit-box-shadow: 0px 56px 36px -60px #121D12;
		-moz-box-shadow: 0px 56px 36px -60px #121D12;
		-o-box-shadow: 0px 56px 36px -60px #121D12;
	}
	.grid img {
		width: 100%;
	} 
	.grid h3{
		text-transform: uppercase;
		padding: 8px 0;
		margin-bottom: 8px;
		font-size: 1.6em;
		color:#00B895;
		border-bottom: 1px solid #dedede;
		font-family: 'PT Sans Narrow', sans-serif;
	}
	.grid p{
		font-size: 0.875em;
		color: rgba(148, 145, 145, 0.84);
		font-family: Arial, Helvetica, sans-serif;
		padding: 0em 1em 1em 1em;
		line-height: 1.5em;
	}
	.button{
		font-family: 'Roboto', sans-serif;
		color: #ffffff;
		background-color:#00B895;
		display: inline-block;
		text-transform: uppercase;
		padding: 10px 30px;
		font-size: 0.875em;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
	}
	.button:hover{
		background-color: #222;
	}
	.last-grid{
		margin:0px;
	}
	/*-----specials-heading----*/
	.specials{
		background:#EDEAE6;
		padding:50px 0;
		position:relative;
	}
	.specials:after{
		content: '';
		position:absolute;
		width: 0;
		height: 0;
		border:20px solid #FFF;
		border-bottom: 0 solid rgba(0, 0, 0, 0)!important;
		border-right: 15px solid rgba(0, 0, 0, 0)!important;
		border-left: 15px solid rgba(0, 0, 0, 0)!important;
		left:50%;
		top:0px;
		margin-left: -10px;
	}
	.specials-heading h3{
		font-family: 'Roboto', sans-serif;
		font-size: 1.8em;
		color:#6C6C6D;
		text-align: center;
		text-transform: uppercase;
		/* background:url(../images/bg-h2.png) repeat-x center; */
	}
	/*----special-grid------*/
	.special-grid {
		float: left;
		width: 32%;
		margin-right: 2%;
		text-align: center;
	}
	.special-grid img{
		width:100%;
	}
	.special-grid a{
		text-transform: uppercase;
		font-size: 1.2em;
		font-family: 'Roboto', sans-serif;
		color:#5F5F5F;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
		padding: 0.3em 0;
		display: block;
	}
	.special-grid a:hover{
		color: #009175;
	}
	.special-grid p{
		font-size: 0.875em;
		color: rgba(148, 145, 145, 0.84);
		font-family: Arial, Helvetica, sans-serif;
		padding: 0em 1em 1em 1em;
		line-height: 1.5em;
	}
	.spe-grid{
		margin: 0px;
	}
	.specials-grids {
		padding: 50px 0;
	}
	/*----start-testmonial-grid----*/
	.testmonials{
		text-align:center;
		background:#FFF;
		padding:50px 0;
	}
	.testmonial-grid h3{
		font-family: 'Roboto', sans-serif;
		font-size: 2em;
		color:#323A45;
		text-align: center;
		text-transform: uppercase;
		padding: 0.5em 0 0.5em 0;
	}
	.testmonial-grid p{
		font-size: 0.875em;
		color:#8A8A8A;
		font-family: Arial, Helvetica, sans-serif;
		padding:10px 0;
		margin:0 auto;
		width:80%;
		line-height: 1.8em;
	}
	.testmonial-grid a{
		font-size: 0.875em;
		font-size: 1.2em;
		font-family: 'Roboto', sans-serif;
		color:#45B39E;
	}
	/*---start-footer-----*/
	.footer{
		background:#45B39E;
		padding: 50px 0;
		position:relative;
	}
	.footer:after{
		content: '';
		position:absolute;
		width: 0;
		height: 0;
		border:20px solid #45B39E;
		border-top: 0 solid rgba(0, 0, 0, 0)!important;
		border-right: 15px solid rgba(0, 0, 0, 0)!important;
		border-left: 15px solid rgba(0, 0, 0, 0)!important;
		left:50%;
		top:-20px;
		margin-left: -10px;
	}
	.footer-grid{
		float:left;
		width:23%;
		margin-right:2%;
	}
	.footer-grid h3{
		font-size: 1.5em;
		color: #fff;
		text-transform: uppercase;
		font-family: 'Roboto', sans-serif;
		margin-bottom: 20px;
	}
	.footer-grid p{
		font-size: 0.875em;
		color:#FFF;
		font-family: Arial, Helvetica, sans-serif;
		line-height: 1.8em;
	}
	.footer-grid ul li a{
		display:block;
		padding:10px 0px;
		border-bottom: 1px solid #5AC5B1;
		font-size: 0.875em;
		color:#FFF;
		font-family: Arial, Helvetica, sans-serif;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
		text-transform:uppercase;
	}
	.footer-grid ul li a:hover{
		color:#005F4D;
	}
	.footer-lastgrid{
		margin:0;
	}
	.email-link{
		color:#FFF;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
		text-transform:lowercase;
	}
	.email-link:hover{
		color:#FFF;
	}
	/*---start-copy-right-----*/
	.copy-right{
		text-align:center;
		padding:1em;
		background:#323A45;
	}
	.copy-right p{
		font-size: 1em;
		color: #fff;
		text-transform: uppercase;
		font-family: 'Roboto', sans-serif;
	}
	.copy-right p a{
		color: rgba(148, 145, 145, 0.84);
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
	}
	.copy-right p a:hover{
		color:#FFF;
	}
	/*---about-us----*/
	.about-us {
		padding: 50px 0;
	}
	.about-header h5{
		float: left;
		width: 30%;
		height: 1px;
		background: #D1D1D1;
		margin: 24px 0px 0px 0px;
	}
	.about-header h3{
		font-family: 'Roboto', sans-serif;
		font-size: 2em;
		color: #012231;
		text-align: center;
		text-transform: uppercase;
		/* background:url(../images/bg-h2.png) repeat-x center; */
	}
	.about-info a{
		text-transform: uppercase;
		font-size: 1.2em;
		font-family: 'Roboto', sans-serif;
		color:#009175;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
		padding: 1em 0 0.5em 0;
		display: block;
	}
	.about-info p{
		font-size: 0.875em;
		color: rgba(85, 81, 81, 0.84);
		font-family: Arial, Helvetica, sans-serif;
		line-height: 1.8em;
	}
	/*---start-services----*/
	.services {
		padding: 50px 0;
	}
	.services-header h5{
		float: left;
		width: 40%;
		height: 1px;
		background: #D1D1D1;
		margin: 24px 0px 0px 0px;
	}
	.services-header h3{
		font-family: 'Roboto', sans-serif;
		font-size: 2em;
		color: #012231;
		text-align: center;
		text-transform: uppercase;
		padding: 0 0 0.5em 0;
		/* background:url(../images/bg-h2.png) repeat-x center; */
	}
	.section {
		clear: both;
		padding: 0px;
		margin: 0px;
	}
	.group:before,
	.group:after {
	    content:"";
	    display:table;
	}
	.group:after {
	    clear:both;
	}
	.group {
	    zoom:1;
	}
	.listview_1_of_2{
		display: block;
		float:left;
		margin: 0% 0 4% 0%;
	}
	.grid2{
		border-top: 1px solid rgba(192, 192, 192, 0.39);
	}
	.listimg{
		display: block;
		float:left;
	}
	.text{
		display: block;
		float:left;
		margin: 0% 0 0% 3.6%;
	}
	.listview_1_of_2:first-child { margin-left: 0;} 
	
	.images_1_of_2 {
		width: 46.96%;
		padding:1.5%; 
	}
	.listimg_2_of_1 {
		width: 18.2%;
	}
	.list_2_of_1 {
		width: 70.2%;
	}
	.images_1_of_2  img {
		max-width:100%;
		display:block;
		padding-top: 25px;
	}
	.list_2_of_1  h3{
		font-family: 'Roboto', sans-serif;
		font-size:1.6em;
		color: #626262;
		text-transform:uppercase;
		text-align: left;
	}
	.list_2_of_1 h3 span{
		color:#00B895;
	}
	.list_2_of_1  p{
		font-size:0.85em;
		color:#949191;
		line-height:1.8em;
		margin: 0px 0px 16px 0px;
		font-family:Arial, Helvetica, sans-serif;
	}
	.list_2_of_1 h4{
		color:#A8A8A8;
		font-size:1.2em;
		font-family:Arial, Helvetica, sans-serif;
		padding: 5px 0px;
	}
	/*---plans-404page-----*/
	.error-page{
		text-align:center;
	}
	.error-page p{
		font-family: 'Roboto', sans-serif;
		font-size: 4em;
		color: #012231;
		text-shadow: -2px 3px 4px #9B9B9B;
	}
	.error-page h3{
		font-family: 'Roboto', sans-serif;
		font-size: 10em;
		color:#00B895;
		text-shadow: -2px 3px 4px #9B9B9B;
	}
	.error-page {
		padding: 200px 0px 0 0;
		min-height: 450px;
	}
	/*---start-contact----*/
	/*  Contact Form  ============================================================================= */
	.section {
		clear: both;
		padding: 0px;
		margin: 0px;
	}
	.group:before,
	.group:after {
	    content:"";
	    display:table;
	}
	.group:after {
	    clear:both;
	}
	.group {
	    zoom:1;
	}
	.col{
		display: block;
		float:left;
		margin: 1% 0 1% 1.6%;
	}
	.col:first-child{
		margin-left:0;
	}	
	.span_2_of_3 {
		width: 63.1%;
		padding:1.5%; 
	}
	.span_1_of_3 {
		width: 29.2%;
		padding:1.5%; 
	}
	.span_2_of_3  h3,
	.span_1_of_3  h3 {
		font-family: 'Roboto', sans-serif;
		font-size: 1.5em;
		padding: 0.5em 0;
		color: #012231;
		text-transform: uppercase;
	}
	.contact-form{
		position:relative;
		padding-bottom:30px;
	}
	.contact-form div{
		padding:5px 0;
	}
	.contact-form span{
		display:block;
		font-family: 'Roboto', sans-serif;
		font-size: 0.9em;
		padding-bottom:5px;
		color: #012231;
		text-transform: uppercase;
	}
	.contact-form input[type="text"],.contact-form textarea{
			   padding: 8px;
				display: block;
				width: 98%;
				border: none;
				outline: none;
				color: #464646;
				font-size: 0.8125em;
				font-family: Arial, Helvetica, sans-serif;
				border: 1px solid rgba(85, 85, 85, 0.19);
				-webkit-appearance:none;
	}
	.contact-form textarea{
			resize:none;
			height:120px;		
	}
	.mybutton{
		font-family: 'Roboto', sans-serif;
		background: #012231;
		color: #d6d6d6;
		padding: 15px 40px;
		font-size: 0.875em;
		text-transform: uppercase;
		display: block;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
		cursor:pointer;
		border:none;
	}
	.mybutton:hover{
		background: #00B895;
		color: #FFF;
	}
	.company_address{
		padding-top:26px;
	}
	.company_address p{
		font-size: 0.875em;
		color: rgba(85, 81, 81, 0.84);
		font-family: Arial, Helvetica, sans-serif;
		line-height: 1.8em;
	}
	.company_address p span{
		text-decoration:underline;
		color:#012231;
		cursor:pointer;
		transition: 0.5s ease;
		-o-transition: 0.5s ease;
		-webkit-transition: 0.5s ease;
	}
	.company_address p span:hover{
		color:#00B895;
	}
	 


	
	

		.top-nav ul li a{
			padding:41px 5px;
			font-size:0.75em;
		}
		
		.content_top{
			padding:10px 0;
		}
		.content_top:after{
			top:-10px;
		}
		.special-grid{
			float:none;
			width:94%;
			padding:3%;
			margin-right:0;
		}	
		.specials{
			padding:30px 0 0 0;
		}
		.specials-grids{
			padding:10px 0;
		}
		.testmonials{
			padding:0 0 30px 0;
		}
		.footer-grid{
			float:none;
			width:94%;
			padding:3%;
			margin-right:0;
		}
		.services{
			padding:20px 0;
		}
		.images_1_of_2{
			width:94%;
			padding:3%; 
		}
		.span_2_of_3 {
			width:94%;
			padding:3%; 
		}
		.list_2_of_1{
		  width:78.2%;	
		}
		.error-page{
			padding:20px 0;
			min-height:0;
		}
		.col{ 
			margin: 1% 0 1% 0%;
		}
		.span_1_of_3 {
			width:94%;
			padding:3%; 
		}   
	   .contact-form input[type="text"],.contact-form textarea{
			width:97%;
		}
	
	/*  GO FULL WIDTH AT LESS THAN 480 PIXELS */
	
	
</style>