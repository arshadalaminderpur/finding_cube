new Vue({
  el: '#app',
  data: {
  	output: ''
  },
  methods: {
      isNumber: function(evt) {
          evt = (evt) ? evt : window.event;
          var charCode = (evt.which) ? evt.which : evt.keyCode;
          if ((charCode > 31 && (charCode < 48 || charCode > 57)) && charCode !== 46) {
            evt.preventDefault();;
          } else {
            return true;
          }
        },
      getFormValues () {
        this.output = Math.pow(this.$refs.my_input.value, 3)
      }
  }
})
