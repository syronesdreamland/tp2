<template>
  <div>
    <!-- 1. HTML yang berbeda -->
    <h1 style="font-family:Verdana, Geneva, Tahoma, sans-serif">Halo!</h1>

    <!-- 2. Elemen input teks -->
    <input v-model="inputText" placeholder="Ketik disini" />

    <!-- 3. Penggunaan class bindings dan style bindings -->
    <div :class="{ 'active': isActive }" :style="{ color: textColor }">
      <br><h2>{{ statusText }}</h2>
      <p>{{ emoticon }}</p>
    </div>
    <br>

    <!-- 4. Interaksi dinamis dengan event listener -->
    <br><button @click="toggleActive">Ubah Teks</button>
    <p>{{ dynamicText }}</p>

     
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isActive: false,
    };
  },
  methods: {
    toggleActive() {
      
      this.isActive = !this.isActive;
      if (this.isActive) {
            this.textColor = 'white';
            this.emoticon = '😊';
            this.statusText = 'Aktif';
          } else {
            this.textColor = 'red';
            this.emoticon = '';
            this.statusText = 'Teks Belum Aktif Ya';
        }
      }
    }
  }
</script>

<style scoped>
.active {
  background-color: lightblue;
}

.h1 {
  margin-bottom: 10%;
}
 .active {
  margin-top: 20%;

 }

</style>