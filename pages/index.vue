<template>
  <div>
    <v-btn color="green" dark @click="modalOpened = !modalOpened">
      Add feedback
    </v-btn>
    <glisten-dashboard />
    <glisten-client
      :sheet="modalOpened"
      application-id="GLISTEN"
      user-name="User"
      :custom-tracker="customTracker"
      @close="() => (modalOpened = false)"
    />
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      modalOpened: false,
      customTracker: {
        contextPortal: window.location.href,
        contextPage: '',
      },
    }
  },
}
</script>
