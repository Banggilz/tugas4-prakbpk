<template>
    <div class="container">
      <h1 class="title">Sistem Rental PlayStation</h1>
      <form @submit.prevent="hitungSewa" class="form">
        <div class="input-group">
          <label for="nama">Nama:</label>
          <input type="text" id="nama" v-model="namaPeminjam" class="input">
        </div>
        <div class="input-group">
          <label for="durasi">Durasi Sewa (jam):</label>
          <input type="number" id="durasi" v-model.number="durasiSewa" class="input">
        </div>
        <button type="submit" class="button">Hitung Biaya Sewa</button>
      </form>
  
      <div v-if="biayaSewa > 0" class="result">
        <h2>Hasil Sewa</h2>
        <p><strong>Nama:</strong> {{ namaPeminjam }}</p>
        <p><strong>Durasi Sewa:</strong> {{ durasiSewa }} jam</p>
        <p><strong>Biaya Sewa:</strong> Rp {{ biayaSewa }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        namaPeminjam: '',
        durasiSewa: 0,
        biayaSewa: 0
      }
    },
    methods: {
      hitungSewa() {
        this.biayaSewa = this.durasiSewa * 5000;
      }
    }
  }
  </script>
  
  <style>
.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  color: black; /* Menambahkan warna teks hitam */
}
  
.title {
  text-align: center;
  color: black; /* Mengubah warna judul menjadi hitam */
  margin-bottom: 20px;
}
  
  .form {
    display: flex;
    flex-direction: column;
  }
  
  .input-group {
    margin-bottom: 10px;
  }
  
  .label {
    margin-bottom: 5px;
    color: #666;
  }
  
  .input {
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  
  .button {
    padding: 10px 15px;
    background-color: #5cb85c;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    margin-top: 10px;
  }
  
  .button:hover {
    background-color: #4cae4c;
  }
  
  .result {
  margin-top: 20px;
  padding: 15px;
  background-color: #dff0d8;
  border: 1px solid #d6e9c6;
  border-radius: 4px;
  color: black; /* Mengubah warna teks hasil menjadi hitam */
}
  
  .result h2 {
    color: #3c763d;
  }
  </style>
  