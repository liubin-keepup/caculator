<template>
  <div id="calcul">
    <div class="calc_methods">
      <div class="front">
        <el-input v-model="resault" class="show_res" number></el-input>
      </div>
      <div>
        <div class="calc_num">
          <span v-for="(n,i) in nums" :key="i" @click="getRes(n)">{{n}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Calculator",
  data() {
    return {
      nums: ["清空", "+", "-", "×", 1, 2, 3, "÷", 4, 5, 6, '删除',7, 8, 9, 0, "="],
      join_nums:[],
      
      way:'',
      resault: "",
    };
  },
  methods: {
    getRes(n) {
        let type =typeof(n)
        
        if(type="number"){
            this.resault+=n
        }else if(n=='string'){
            this.resault.indexOf()
        }
    }
  },
  components: {},
};
</script>

<style scoped>
#calcul {
  width: 400px;
  height: 400px;
  border: 1px solid blue;
  margin: 0 auto;
  padding: 20px;
}
.show_res .el-input__inner {
  text-align: end;
}
.calc_num span {
  display: inline-block;
  width: 12%;
  border: 1px solid;
  padding: 5px;
  margin: 15px;
  border-radius: 14%;
}
</style>
