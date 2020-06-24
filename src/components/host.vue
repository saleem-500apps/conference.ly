<template>
  <div>
    <b-modal id="modal" hide-header hide-footer>
      <button type="button" aria-label="Close" class="close" @click="hide()">×</button>
      <LOGIN v-if="type == 'Login'"></LOGIN>
      <INVITE v-else-if="type == 'Invite'"></INVITE>
      <PUBLIC v-else-if="type == 'Public'"></PUBLIC>
      <PRIVATE v-else-if="type == 'Private'"></PRIVATE>
    </b-modal>
  </div>
</template>

<script>
import Login from './Host-Popup/index.vue'
import Invite from './Host-Popup/invite.vue'
import Public from './Host-Popup/public.vue'
import Private from './Host-Popup/private.vue'
export default {
  name: 'Host',
  props: {
    modal: Boolean,
    type: String
  },
  components: {
    'LOGIN': Login,
    'INVITE': Invite,
    'PUBLIC': Public,
    'PRIVATE': Private
  },
  methods: {
    show () {
      this.$bvModal.show('modal')
    },
    hide () {
      this.$bvModal.hide('modal')
    }
  },
  watch: {
    modal: function (val) {
      if (val) this.show()
      else this.hide()
    }
  }
}
</script>

<style>
</style>
