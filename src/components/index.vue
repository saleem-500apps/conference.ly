<template>
  <div>
    <button type="button" class="btn btn-primary mr-2">create Meeting</button>
    <button type="button" class="btn btn-primary">Join a meeting</button>
    <HOST :modal="modal" :type="type"></HOST>
  </div>
</template>

<script>
import Host from "./host.vue";
export default {
  name: "Index",
  components: {
    HOST: Host
  },
  data() {
    return {
      modal: false,
      type: "Login"
    };
  },
  mounted() {
    if (document.cookie.length > 10) {
      var cookie = document.cookie.split(";").find(i => i.includes("token="));
      if (cookie) {
        console.log("in login");
      }
    } else {
      console.log("in login else");
      this.showModal("Login");
    }
  },
  methods: {
    showModal(type) {
      console.log("in modal view");
      this.modal = true;
      this.type = type;
    }
  }
};
</script>

<style></style>
