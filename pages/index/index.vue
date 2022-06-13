<template>
	<view>
		<u-navbar bgColor="#f3f4f6" height="90">
			<view slot="center" class="nav-center">微信</view>
			<view slot="left">
				<view class="nav-left">
					<image src="@/static/1.jpg" mode="widthFix"></image>

				</view>
			</view>
			<view slot="right">
				<view class="nav-right">
					<u-icon name="search" size="60" bold></u-icon>
					<u-icon name="man-add" size="60" bold></u-icon>
				</view>
			</view>
		</u-navbar>
		<view class="content">
			<view class="friend-list">
				<view class="friend-item">
					<view class="friend-item__avatar">
						<image src="@/static/2.jpg" mode="widthFix"></image>
						<u-badge max="99" :value="1" absolute :offset="[-13,10]"></u-badge>
					</view>
					<view class="friend-item__content">
						<view class="friend-item__info">
							<text class="friend-item__info__title">
								蔡夏柠
							</text>
							<text class="friend-item__info__newdate">
								12:38
							</text>
						</view>
						<view class="friend-item__news">
							饭吃了吗？
						</view>
					</view>
				</view>

				<view class="friend-item">
					<view class="friend-item__avatar">
						<image src="@/static/5.jpg" mode="widthFix"></image>
						<u-badge max="99" :value="100" absolute :offset="[-13,10]"></u-badge>
					</view>
					<view class="friend-item__content">
						<view class="friend-item__info">
							<text class="friend-item__info__title">
								张江航
							</text>
							<text class="friend-item__info__newdate">
								晚上 6:20
							</text>
						</view>
						<view class="friend-item__news">
							吃了
						</view>
					</view>


				</view>


			</view>
		</view>
	</view>
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
		emthods: {

		}
	}
</script>

<style lang="scss">
	.nav {
		&-left {
			line-height: 20rpx;

			image {
				width: 70rpx;
				height: 70rpx;
				border-radius: $uni-border-radius-base;
			}
		}

		&-right {
			width: 140rpx;
			display: flex;
			justify-content: space-between;

		}

		&-center {
			font-weight: 700;
		}
	}

	.content {
		margin-top: 90rpx;
		background-color: rgba($uni-color-primary, .2);
		height: calc(100vh - 90rpx);

		.friend {
			&-list {
				display: flex;
				flex-direction: column;
			}

			&-item {
				flex-basis: 140rpx;
				overflow: hidden;
				display: flex;
				justify-content: space-between;
				align-items: center;
				padding: 0 $uni-spacing-row-base;
				background: rgba($uni-bg-color-grey, .6);
				border-bottom: 2rpx solid $uni-color-primary;

				&__avatar {
					position: relative;
					flex-basis: 120rpx;
					display: flex;
					align-items: center;

					image {
						width: 90rpx;
						line-height: 90rpx;
						border-radius: $uni-border-radius-base;
					}
				}

				&__content {
					flex: 1;
					padding-right: 10rpx;
				}

				&__info {
					display: flex;
					justify-content: space-between;

					&__newdate {
						font-size: $uni-font-size-sm;
						color: $uni-text-color-placeholder;
					}

					&__title {
						font-size: $uni-font-size-lg;
					}
				}

				&__news {
					font-size: $uni-font-size-base;
					color: $uni-text-color-placeholder;
				}

			}
		}
	}
</style>
