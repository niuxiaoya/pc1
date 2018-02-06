<template>
  <div>
    <ul>
      <li v-for="(item,index) in dataList">
        {{item}}
      </li>
    </ul>
<!--:class="{'active':navNum==key+1}" @click="navClick(item,key+1)"-->
  </div>
</template>
<script type="javascript">
  export default {
    data () {
      return {
        dataList:[1,2,3],
        num:0
      }
    }
  }
</script>
<style type="text/less" scoped lang="less">
  ul {
    padding: 10px 15px;
    display: flex;
    justify-content: space-between;
    li {
      position: relative;
        &:before{
          cursor: pointer;
          width: 20px;
          height: 3px;
          background: #333;
          content: "";
          position: absolute;
          bottom: 0;
          left: calc(~'50% - 10px');
        }
    }
  }
</style>
