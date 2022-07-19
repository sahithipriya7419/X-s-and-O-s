<template>
    <div>
        <i class="fa fa-circle fa-4x text-primary zoomIn"  v-if="iconname === 'circle'"></i>
         <i class="fa fa-times fa-4x text-warning zoomIn"  v-else-if="iconname === 'cross'"></i>
         <img src="../assets/logo.png" alt="" class="img-fluid zoomIn" v-else-if="iconname=== 'empty'"/>
    </div>
</template>

<script>
export default {
    props:{
        iconname:{
            type: String,
            required: true
        }
    }
}
</script>

<style>
img {
  width: 80px;
}

@keyframes zoomIn {
  from {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }

  50% {
    opacity: 1;
  }
}

.zoomIn {
  animation-name: zoomIn;
  animation-duration: 1s;
}
</style>