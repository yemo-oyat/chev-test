<template>
            <div class="app-admin-section">
            <div class="app-admin-col-1">
            <Leftbar/>
            </div>
            <div class="app-admin-col-2">
            <div class="admin-top-bar">
        <div class="admin-top-bar-left">
          <div class="settings-icon"></div>
          <div @click = "switchView('transfer')" class="admin-top-barlinks admin-active-top-link">Transfer</div>
          <div @click = "switchView('withdrawal')" class="admin-top-barlinks">Withdrawal</div>
        </div>
        <div class="admin-top-bar-right">
          <div class="admin-topbar-date">{{new Date().toLocaleString() | humanize}}</div>
        </div>
      </div>
        <div v-show="transferView">
        <Transfer/> 
        </div>
            <div v-show="withdrawalView">
           <Withdrawal/>       
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
import Transfer from './transfer'
import Withdrawal from './withdrawal'
export default {
  name: "Home",
  components: {
    Leftbar,
    Rightbar,
    Transfer,
    Withdrawal
  },
  data(){
      return{
        selectedTab: '',
        transferView: true,
        withdrawalView: false,
      }
  },
methods:{
    
    switchView( selected ){
        console.log("HEEIE")

        if(selected == "transfer"){
            console.log('transferView')
         this.transferView = true
         this.withdrawalView = false
        }
        else if(selected == 'withdrawal') {
             this.transferView = false
         this.withdrawalView = true
        }

    },

}
}
</script>

<style src=".././global.css"></style>