<template>
  <div>
    <teleport to="#modal">
      <Modal />
    </teleport>
  </div>
</template>

<script>
import Modal from "@/components/Modal.vue";
export default {
  components: {
    Modal,
  },
};
</script>
