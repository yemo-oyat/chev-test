<template>
            <div class="app-admin-section">
            <div class="app-admin-col-1">
            <Leftbar/>
            </div>
            <div class="app-admin-col-2">
            <div class="admin-top-bar">
        <div class="admin-top-bar-left">
          <div class="settings-icon"></div>
          <div @click = "switchView('cashAddition')" class="admin-top-barlinks admin-active-top-link">Cash Addition</div>
          <div @click = "switchView('IncreaseDecrease')" class="admin-top-barlinks">Increase/Decrease Savings</div>
        </div>
        <div class="admin-top-bar-right">
          <div class="admin-topbar-date">{{new Date().toLocaleString() | humanize}}</div>
        </div>
      </div>
        <div v-show="cashAddition">
        <CashAddition/> 
        </div>
            <div v-show="IncreaseDecrease">
           <IncreaseDecrease/>       
            </div>
    </div>
      <div class="app-admin-col-3">
              <Rightbar />
            </div>
</div>
</template>


<script>
import Leftbar from '../../components/leftbar/leftbar'
import Rightbar from '../../components/rightbar/rightbar'
import CashAddition from './cashAddition.vue'
import IncreaseDecrease from './IncreaseDecrease.vue'
export default {
  name: "Home",
  components: {
    Leftbar,
    Rightbar,
    CashAddition,
    IncreaseDecrease
  },
  data(){
      return{
        selectedTab: '',
        cashAddition: true,
        IncreaseDecrease: false,
      }
  },
methods:{
    
    switchView( selected ){
        if(selected == "cashAddition"){
      
         this.cashAddition = true
         this.IncreaseDecrease = false
        }
        else if(selected == 'IncreaseDecrease') {
             this.cashAddition = false
         this.IncreaseDecrease = true
        }

    },

}
}
</script>

<style src=".././global.css"></style>