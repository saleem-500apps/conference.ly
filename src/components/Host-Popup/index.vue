<template>
  <div>
    <h4>Login</h4>
    <form>
      <div class="mt-2">
        <label>Email</label>
        <input type="text" class="form-control">
      </div>
      <div class="mt-2">
        <label>Password</label>
        <input type="password" class="form-control">
      </div>
      <button class="col-12 btn btn-primary mt-3">LOGIN</button>
    </form>
    <div class="float-right mt-2">
      <small>Don't have an account? <a href="">Signup</a></small>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HostPopupIndex'
}
</script>

<style>

</style>
