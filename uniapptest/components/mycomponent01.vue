<template>
	<view>
		<h1 v-on:click="click_inner01" >{{title}}</h1>
		<div>{{content}}</div>
	</view>
</template>

<script>
	
	export default {
		data() {
			return {				
			};
		},onLoad() {			
		},
		props:{
			title:{
				type: String,
				default:"Title01",
			},
			content:{
				type: String,
				default:"Content001",
			},
		},
		methods:{	
			click_inner01: function(){
				console.log( this.title);
				this.$emit("click_out",this.title);
			}
		},
		components:{
		}
	}
</script>

<style>

</style>
