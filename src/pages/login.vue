<template>
  <div class="semantic-component">
    <!-- <div class="ui selection dropdown semanticDropDown">
      <input type="hidden" name="gender" v-model="selected">
      <i class="dropdown icon"></i>
      <div class="default text">Gender</div>
      <div class="menu">
        <div class="item" :data-value="item.Value"
             v-for="item in items"
             @click="changeSelection(item)">
          {{ item.Gender }}
        </div>
      </div>
    </div>
    <pre>{{ JSON.stringify(selectedItem) }}</pre> -->
        <div class="ui grid center aligned">
            <div class="row">
                <div class="sixteen wide tablet six wide computer column">
                    <div class="ui left aligned segment">
                        <div id="form1" class="ui form">
                            <h1 id="login-head" class="ui header center aligned">Login</h1>
                            <div class="field">
                                <label>Email or Username:</label>
                                <div class="ui fluid icon input">
                                    <input name="user_name" id="u_name" type="email" autocomplete="off" style="width:100%!important;min-width:100%;width:100%;">
                                    <i class="icon mail outline"></i>
                                </div>
                            </div>
                            <div class="field">
                                <label>Password:</label>
                                <div class="ui fluid icon input">
                                    <input name="password" id="u_pass" type="password" autocomplete="off" style="width:100%!important;min-width:100%;width:100%;">
                                    <i class="icon key"></i>
                                </div>
                            </div>
                            <div class="field">
                                <a class="ui teal basic right labeled icon button" href="#" >
                                    Login<i class="icon sign in"></i>
                                </a>
                                <a class="ui blue basic right labeled icon button" href="#" style="float:right;">
                                    Sign Up<i class="icon spy"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {Gender: 'Male', Value: 1},
          {Gender: 'Female', Value: 0}
        ],
        selected: '',
        selecteditem: {}
      }
    },
    methods: {
      changeSelection (item) {
        this.selectedItem = item
        this.selected = item.Value
      }
    },
    mounted () {
      this.selecteditem = {}
      $('.semanticDropDown').dropdown()
    }
  }
</script>

<style>
#login-head{
  background: #86aedd;
  color: #fff;
  font-size: 20px;
  padding: 10px;
}
.ui.labeled.icon.button>.icon{
  background: none;

}
</style>
