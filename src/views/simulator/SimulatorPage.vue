<template>
  <div class="Matc">
    <Simulator mode="standalone"/>
  </div>
</template>
<style>
  @import url("../../style/sim.css");
</style>
<script>
import Logger from 'common/Logger'
import Simulator from 'core/Simulator'

export default {
  name: "SimulatorPage",
  mixins: [],
  data: function() {
    return {
      user: {
        id: -1,
        name: "Guest",
        email: "guest@onepersonai.com",
        role: "guest",
        lastlogin: 0,
        lastNotification: 0,
        tos: false,
        paidUntil: 0,
        plan: "Free"
      }
    }
  },
  components: {
    'Simulator': Simulator
  },
  methods: {
  },
  async mounted() {
    this.logger = new Logger('SimulatorPage')
    this.logger.info('mounted', 'exit >> ')
  }
};
</script>
