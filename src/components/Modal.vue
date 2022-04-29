<template>
  <button @click="modalOpen = true">Show Modal</button>
  <div v-if="modalOpen" class="modal-overlay">
    <div class="modal">
      <div class="modal-header">This is a modal</div>
      <div class="modal-body">
        lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec euismod,
      </div>
      <div class="modal-footer">
        <button @click="modalOpen = false">Close</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      modalOpen: false,
    };
  },
};
</script>

<style>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
}
.modal {
  background: white;
  border: 1px solid #eee;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.modal-header {
  border-bottom: 1px solid #eee;
}

.modal-body,
.modal-footer,
.modal-header {
  padding: 10px;
}

.modal-footer {
  border-top: 1px solid #eee;
}
</style>
