<template>
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-section">
            <h3>Tentang Kami</h3>
            <p>Kami menyediakan layanan rental PlayStation terbaik dengan koleksi game terbaru dan terlengkap.</p>
          </div>
          <div class="footer-section">
            <h3>Kontak</h3>
            <p><strong>Alamat:</strong> Jl. Gamer No.1, Jakarta</p>
            <p><strong>Email:</strong> info@rentalps.com</p>
            <p><strong>Telepon:</strong> (021) 1234567</p>
          </div>
          <div class="footer-section">
            <h3>Ikuti Kami</h3>
            <p>Temukan kami di sosial media:</p>
            <ul class="socials">
              <li><a href="#">Facebook</a></li>
              <li><a href="#">Twitter</a></li>
              <li><a href="#">Instagram</a></li>
            </ul>
          </div>
        </div>
        <div class="footer-bottom">
          <p>© 2024 Rental PlayStation. Hak cipta dilindungi.</p>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'FooterComponent'
  }
  </script>
  
  <style scoped>
.footer {
  background-color: #222;
  color: white;
  padding: 20px 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
}

.footer-section {
  flex: 1;
  min-width: 200px;
  margin-right: 20px;
}

.footer-section h3 {
  margin-bottom: 10px;
}

.footer-section p,
.footer-section ul {
  margin-bottom: 10px;
}

.footer-section ul {
  list-style: none;
  padding: 0;
}

.footer-section ul li a {
  color: white;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-section ul li a:hover {
  color: #ffcc00;
}

.footer-bottom {
  text-align: center;
  margin-top: 20px;
  border-top: 1px solid #444;
  padding-top: 20px;
}

.socials {
  display: flex;
}

.socials li {
  margin-right: 10px;
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
  }

  .footer-section {
    margin-bottom: 20px;
  }

  .footer-bottom {
    text-align: center;
  }
}

  </style>
  