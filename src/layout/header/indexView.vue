<template>
    <div class="header-wrapper row m-0">
           <div class="header-logo-wrapper col-auto p-0">
               <sidebar/>
           </div>
            <div class="left-header col horizontal-wrapper ps-0">
              
           </div>
            <div class="nav-right col-6 pull-right right-header p-0">
            <ul class="nav-menus">
                <li> 
               <searchView/>
              </li>
              <li class="serchinput">
                <searchInput/>
              </li>
               <li>
                <modeView/>
              </li>
              <li class="maximize">
                    <maximizeView/>
                </li>
            </ul>
            </div>
    </div>
</template>
<script>
import searchInput from "./searchInput.vue"
import sidebar from "./sidebarView.vue"
import searchView from "./searchView.vue"
import modeView from "./modeView.vue"
import maximizeView from "./maximizeView.vue"

export default {
    components:{
        sidebar,
        searchView,
        modeView,
        maximizeView,
        searchInput
    },
     data () {
      return {
        filtered: false,
      };
    },
      methods: {
     collapseFilter() {
        this.filtered = !this.filtered;
      },
      }
}
</script>