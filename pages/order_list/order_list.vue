<template>
	<view>
		<view class="order-list" v-for="one in monthList">
			<view class="month">
				<text>{{ one.month }}</text>
				<image src="../../static/order_list/calendar-icon.png" mode="widthFix"></image>
			</view>
			<view class="order" v-for="order in one.orders" @tap="viewOrderHandle(order.id)">
				<view class="top">
					<view class="date">{{ order.acceptTime }}</view>
					<view class="amount-status">
						<text class="amount" v-if="order.hasOwnProperty('realFee')">￥{{ order.realFee }}</text>
						<text :class="order.style">{{ order.status }}</text>
					</view>
				</view>
				<view class="content">
					<view class="from">
						<text>{{ order.startPlace }}</text>
					</view>
					<view class="to">
						<text>{{ order.endPlace }}</text>
					</view>
					<view class="desc">
						<text>订单编号：{{ order.id }}</text>
						<view class="rate"><u-rate :count="5" v-model="order.rate" active-color="#FFBD66" :disabled="true"></u-rate></view>
					</view>
				</view>
			</view>
		</view>
		<u-top-tips ref="uTips"></u-top-tips>
	</view>
</template>

<script>
let dayjs = require('dayjs');
export default {
	data() {
		return {
			
		};
	},
	methods: {
		
	},
	onLoad: function() {
		
	},
	onReachBottom: function() {
		
	},

	onShow: function() {
		
	},
	onHide: function() {
		
	}
};
</script>

<style lang="less">
@import url('order_list.less');
</style>
