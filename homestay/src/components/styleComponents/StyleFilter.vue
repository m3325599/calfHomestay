<template>
	<div class="stylefilter">
     <FilterNav />
		 <FilterContent @toParent="sent"/>
	</div>
</template>

<script>
import FilterNav from "./filter/FilterNav";
import FilterContent from "./filter/FilterContent";
export default {
  name: "StyleFilter",
  components: {
    FilterNav,
    FilterContent
  },
  data() {
    return {};
  },
  methods:{
    sent(data){
      this.$emit("toParent",data);
    }
  }
};
</script>

<style scoped>
.stylefilter {
  width: 100%;
  height: 160px;
  padding-bottom: 30px;
  background-color: #fff;
  border-bottom: 2px solid #eee;
}
</style>