<template>
  <div class="modal-mask">
    <div class="modal-wrapper">
      <div class="modal-container">

        <div class="modal-header d-flex justify-content-between">
          <slot name="header">
            default header
          </slot>
          <button class="modal-default-button" @click="$emit('close')">
            <IconClose />
          </button>
        </div>

        <div class="modal-body">
          <slot name="body">
            default body
          </slot>
        </div>

      </div>
    </div>
  </div>

</template>

<script>
import IconClose from './icons/IconClose.vue';


export default {
  components: {
    IconClose
  }
}
</script>


<style scoped>
.modal-default-button {
  padding: 16px;
  box-shadow: none;
  background-color: black;
  border: none;
}

.modal-default-button svg {
  fill: #ffffff;
}

.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  position: relative;
  overflow: scroll;
  width: 600px;
  height: auto;
  margin: 0 auto;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  max-height: 600px;
}

.modal-header {
  margin: 0;
  color: white;
  background-color: black;
}

.modal-header p {
  margin-bottom: 0;
}
.modal-body {
  margin: 16px;
}




.modal-enter-from, .modal-leave-to {
  opacity: 0;
}

.modal-enter-active .modal-container,
.modal-leave-active .modal-container {
  transform: scale(1.1);
}

</style>
