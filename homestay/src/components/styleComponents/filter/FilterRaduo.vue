<template>
	<div class="filterradio">
		<div class="radiotitle">{{radioli.name}}</div>
        <el-radio-group v-model="radio" class="radiolist">
            <el-radio v-for="item in radioli.choose" :key="item.index" :label="item"></el-radio>
        </el-radio-group>
	</div>
</template>

<script>
	export default {
        name: 'FilterRadio',
		props:["radioli","info","p"],
		components:{

		},
		data() {
			return {
                radio:'全部',
			}
		},
		watch:{
			radio(val){
				if(val=='全部'){
					this.info[this.p]="";
					return;
				}
				this.info[this.p]=val;
			}
		}
	}
</script>

<style scoped>
.filterradio {
	position: relative;
	left: 30px;
}
.radiotitle {
	font-size: 14px;
	font-weight: 700;
	position: relative;
	left: 20px;
	top: 20px;
}
.radiolist {
	text-align: left;
	position: relative;
	left: 80px;
}
</style>