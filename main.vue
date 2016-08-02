<template>
  <input type="submit" name="{{ name }}" value="{{ value }}" v-on:click="confirmFromUser">
</template>

<script>
export default Vue.extend({
  props: ['name', 'value', 'confirm'],
  methods: {
    confirmFromUser(event){
      event.preventDefault();
      let form = event.target.form;
      let buttontype = document.createElement("input");
      buttontype.setAttribute("type", "hidden");
      buttontype.setAttribute("name", this.name);
      buttontype.setAttribute("value", this.value);

      if(this.confirm !== undefined) {
        if (confirm(this.confirm)) {
          form.appendChild(buttontype);
          form.submit();
        }
      }else {
        form.appendChild(buttontype);
        form.submit();
      }
    }
  }
});
</script>
