<template>

  <div style='margin:auto;height:44px;width:90%;background-color:#616986;border-top-left-radius:10px;border-top-right-radius:10px;'>
  <p style='float:left;padding-left:20px;color:white;padding-bottom:10px;'>Immunization Details</p>
  <i class='el-icon-close' style='float:right;color:white;padding-top:14px;padding-right:15px;'></i>
      <el-collapse v-model='activeNames' @change='handleChange' style='width:100%;margin:auto;padding-top:43px;border-bottom-left-radius:10px;border-bottom-right-radius:10px;'>
              <el-collapse-item title='Willis, Ben    |    14 Months, Male    |    DOB 09/15/2018'>
                <div style='border-top:0.05px solid #D7DFE0;border-bottom:0.05px solid #D7DFE0;height:550px;width:25%;background-color:white;float:left;'>
                  <!-- left element -->
                  <el-input
                    placeholder="Type something"
                    prefix-icon="el-icon-search"
                    v-model="input2">
                  </el-input>
                </div>
                <div style='border-top:0.05px solid #D7DFE0;border-bottom:0.05px solid #D7DFE0;height:550px;width:25%;background-color:white;float:right;'>
                  <!-- right element -->
                  <p>Assessment(s)</p>
                  <el-checkbox v-model="checked" style='padding-left:10px;'>Select all</el-checkbox>
                  <el-checkbox v-model="checked" style='padding-left:10px;'>A48.51 Infant Botulism disease</el-checkbox>
                  <el-checkbox v-model="checked" style='padding-left:10px;'>G93.7 Reye's syndrome</el-checkbox>
                  <el-checkbox v-model="checked" style='padding-left:10px;'>R68.1 Excessive crying of infant</el-checkbox>
                </div> 
                <div style='border-top:0.05px solid #D7DFE0;border-bottom:0.05px solid #D7DFE0;height:550px;width:75%;width:100%;background-color:#F0FCFF;'>
                  <!-- center element -->
                  <p style='float:left;padding-left:25px;font-size:17px;'>Details</p>
                  <pre>

                  </pre>
                    <span class="date" style='padding-left:25px;'>Visit Date</span>
                    <el-date-picker
                      v-model="value1"
                      type="date"
                      placeholder="Pick a day">
                    </el-date-picker>
                    <span class="date" style='padding-left:25px;'>Exp. date</span>
                    <el-date-picker
                      v-model="value2"
                      type="date"
                      placeholder="Pick a day">
                    </el-date-picker>
                    <el-divider></el-divider>
                    <span class="date" style='padding-left:25px;'>Status</span>
                    <el-dropdown>
                      <el-button type="primary" style='background-color:white;'>
                        Pending<i class="el-icon-arrow-down el-icon--right"></i>
                      </el-button>
                      <el-dropdown-menu slot="dropdown">
                        <el-dropdown-item>Pending</el-dropdown-item>
                        <el-dropdown-item>Completed</el-dropdown-item>
                      </el-dropdown-menu>
                    </el-dropdown>
                    <span class="date" style='padding-left:25px;'>Reason</span>
                    <el-input style='background-color:white;height:10px;width:150px;padding-top:5px;' placeholder="Enter reason" v-model="input"></el-input>
                    <pre>

                    </pre>
                    <ele-divider></ele-divider>
                    <span class="date" style='padding-left:25px;'>Dose Number</span>
                    <el-input style='background-color:white;height:10px;width:150px;padding-top:5px;' placeholder="Dose number" v-model="input2"></el-input>
                    <span class="date" style='padding-left:25px;'>Dose</span>
                    <el-input-number v-model="num" @change="handleChange" :min="1" :max="10"></el-input-number>
                    <p style='padding-left:25px;'>Route</p>
                    <el-radio v-model="radio" label="1" style='padding-left:25px;'>Injectible</el-radio>
                    <el-radio v-model="radio" label="2" style='padding-left:25px;'>Oral</el-radio>
                    <el-radio v-model="radio" label="2" style='padding-left:25px;'>Intravenous</el-radio>
                    <pre>

                    </pre>
                    <div style='float:left;'>
                    <p>Given Date</p>
                    <el-date-picker placeholder="pick a day">
                    </el-date-picker>
                    </div>
                    <div style='float:right;'>
                    <p>Given By</p>
                    <el-input
                    placeholder=""
                    prefix-icon="el-icon-search"
                    v-model="input3">
                    </el-input>
                    </div>
                </div>
              </el-collapse-item>
      </el-collapse>
  </div>
  
</template>


<script>
export default {
  data(){
    return{
      activeNames:['top'],
      input:'',
      num: 1
    };
  },
  methods: {
    handleChange(val){
      console.log(val);
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
