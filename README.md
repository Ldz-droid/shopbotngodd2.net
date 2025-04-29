<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Hericium Yam Corn Paste - Thực Phẩm Dinh Dưỡng Cao Cấp</title>
  <meta name="description" content="Bột ngô khoai mỡ nấm đầu khỉ - Thơm ngon, bổ dưỡng, dễ chế biến. Phù hợp cho người ăn kiêng, tiểu đường, người già, phụ nữ mang thai và trẻ nhỏ." />
  <meta name="keywords" content="bột ngô, khoai mỡ, nấm đầu khỉ, sản phẩm dinh dưỡng, thực phẩm tốt cho sức khỏe, giảm cân, tiểu đường" />
  <meta name="author" content="Hericium Corn Co." />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: linear-gradient(135deg, #fff8e1 0%, #ffcc80 50%, #ff8a65 100%);
      color: #4e342e;
      line-height: 1.6;
      overflow-x: hidden;
      position: relative;
    }

    #loader {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #ff7043;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 10001;
      animation: fadeOut 1s ease forwards 1s;
    }

    #loader::before {
      content: '';
      width: 50px;
      height: 50px;
      border: 5px solid #fff;
      border-top: 5px solid #ffca28;
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }

    @keyframes fadeOut {
      to { opacity: 0; visibility: hidden; }
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    #particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      pointer-events: none;
    }

    .promo-popup {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) scale(0);
      background: #fff;
      padding: 1.5rem;
      border-radius: 15px;
      box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
      z-index: 10000;
      text-align: center;
      width: 90%;
      max-width: 350px;
      display: none;
    }

    .promo-popup.active {
      transform: translate(-50%, -50%) scale(1);
      display: block;
      animation: popupIn 0.5s ease forwards;
    }

    @keyframes popupIn {
      0% { transform: translate(-50%, -50%) scale(0); opacity: 0; }
      70% { transform: translate(-50%, -50%) scale(1.05); opacity: 1; }
      100% { transform: translate(-50%, -50%) scale(1); opacity: 1; }
    }

    .promo-popup h2 {
      font-size: 1.8rem;
      color: #ff7043;
      margin-bottom: 1rem;
    }

    .promo-popup p {
      font-size: 1rem;
      margin-bottom: 1rem;
    }

    .promo-popup button {
      background: #ffca28;
      color: #4e342e;
      border: none;
      padding: 0.8rem 2rem;
      font-size: 1.1rem;
      font-weight: bold;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .promo-popup button:hover {
      background: #ffb300;
      transform: scale(1.1);
    }

    .promo-close {
      position: absolute;
      top: 10px;
      right: 10px;
      background: #ef5350;
      color: white;
      border: none;
      width: 30px;
      height: 30px;
      border-radius: 50%;
      cursor: pointer;
      font-size: 1.2rem;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s ease;
    }

    .promo-close:hover {
      background: #d32f2f;
      transform: scale(1.2);
    }

    .hericium-toggle {
      position: fixed;
      top: 10px;
      right: 10px;
      background: #ff7043;
      color: white;
      border: none;
      padding: 0.6rem 1rem;
      font-size: 1rem;
      font-weight: bold;
      border-radius: 50px;
      cursor: pointer;
      z-index: 1000;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(255, 112, 67, 0.5);
    }

    .hericium-toggle:hover {
      background: #ef5350;
      transform: scale(1.1);
    }

    .hericium-panel {
      position: fixed;
      top: 50px;
      right: 10px;
      background: #ff7043;
      color: white;
      padding: 1rem;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
      z-index: 999;
      display: none;
      width: 200px;
      text-align: center;
      animation: slideIn 0.3s ease-out;
    }

    .hericium-panel.active {
      display: block;
    }

    @keyframes slideIn {
      from { transform: translateX(100%); }
      to { transform: translateX(0); }
    }

    .hericium-panel ul li a {
      color: #ffca28;
      text-decoration: none;
      font-weight: bold;
      padding: 0.5rem;
      display: block;
      transition: all 0.3s ease;
    }

    .hericium-panel ul li a:hover {
      color: #ffb300;
      transform: translateX(5px);
    }

    .flash-sale-banner {
      background: linear-gradient(90deg, #ef5350, #ff7043);
      padding: 1rem;
      text-align: center;
      color: white;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }

    .flash-sale-text {
      font-size: 1.5rem;
      font-weight: bold;
      text-transform: uppercase;
      animation: pulse 1.5s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    .flash-sale-button {
      background: #ffca28;
      color: #4e342e;
      border: none;
      padding: 0.6rem 1.5rem;
      font-size: 1.2rem;
      font-weight: bold;
      border-radius: 50px;
      cursor: pointer;
      margin-top: 0.5rem;
      transition: all 0.3s ease;
      box-shadow: 0 4px 10px rgba(255, 202, 40, 0.5);
    }

    .flash-sale-button:hover {
      background: #ffb300;
      transform: scale(1.05);
    }

    .pricing-countdown {
      background: rgba(255, 255, 255, 0.95);
      margin: 1rem auto;
      padding: 1rem;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
      border: 2px solid #ffca28;
      max-width: 500px;
    }

    .promo-price {
      color: #ef5350;
      font-size: 1.5rem;
      font-weight: bold;
    }

    .original-price {
      color: #ef5350;
      text-decoration: line-through;
      font-size: 1rem;
    }

    .countdown-label {
      font-size: 1rem;
      margin: 0.5rem 0;
    }

    .countdown-timer {
      display: flex;
      justify-content: center;
      gap: 0.5rem;
      margin: 0.5rem 0;
    }

    .timer-box {
      background: #ff7043;
      color: white;
      font-size: 1.2rem;
      padding: 0.5rem;
      border-radius: 8px;
      width: 40px;
      text-align: center;
    }

    .remaining-products {
      font-size: 1rem;
      color: #ef5350;
      animation: blink 2s infinite;
    }

    @keyframes blink {
      50% { opacity: 0.5; }
    }

    .gallery {
      max-width: 500px;
      margin: 1rem auto;
      position: relative;
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
      overflow: hidden;
    }

    .main-image {
      width: 100%;
      height: 250px;
      object-fit: cover;
      border-radius: 15px;
      transition: opacity 0.5s ease;
    }

    .main-image.fade {
      opacity: 0;
    }

    .nav-button {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: #ff7043;
      color: white;
      border: none;
      padding: 0.6rem;
      cursor: pointer;
      font-size: 1.2rem;
      border-radius: 50%;
      transition: all 0.3s ease;
    }

    .nav-button.left { left: 10px; }
    .nav-button.right { right: 10px; }

    .nav-button:hover {
      background: #ef5350;
      transform: translateY(-50%) scale(1.1);
    }

    .thumbnails {
      display: flex;
      justify-content: center;
      gap: 10px;
      margin-top: 10px;
      padding: 0 10px;
    }

    .thumbnail {
      width: 50px;
      height: 50px;
      object-fit: cover;
      border-radius: 8px;
      cursor: pointer;
      border: 2px solid #ddd;
      transition: all 0.3s ease;
    }

    .thumbnail:hover,
    .thumbnail.active {
      border: 2px solid #ffca28;
      transform: scale(1.1);
    }

    .top-button {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      margin: 1rem 0;
    }

    .button {
      padding: 0.8rem 1.5rem;
      background: #ff7043;
      color: white;
      border: none;
      border-radius: 50px;
      font-size: 1.2rem;
      font-weight: bold;
      text-decoration: none;
      transition: all 0.3s ease;
      box-shadow: 0 4px 10px rgba(255, 112, 67, 0.5);
      width: 80%;
      text-align: center;
    }

    .button:hover {
      background: #ef5350;
      transform: scale(1.05);
    }

    .section {
      padding: 2rem 1rem;
      margin: 1rem auto;
      background: rgba(255, 255, 255, 0.95);
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
      text-align: center;
      max-width: 800px;
    }

    .section h2 {
      background: #ff7043;
      color: white;
      padding: 0.8rem 1.5rem;
      border-radius: 10px;
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 1rem;
      box-shadow: 0 4px 10px rgba(255, 112, 67, 0.5);
    }

    .features h3 {
      font-size: 1.2rem;
      margin-bottom: 0.5rem;
      font-weight: bold;
    }

    .features h3 i {
      color: #ffca28;
      margin-right: 0.5rem;
    }

    .products {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin: 1rem 0;
    }

    .product {
      border: 2px solid #ffca28;
      border-radius: 10px;
      padding: 1rem;
      background: #fff;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      transition: all 0.3s ease;
    }

    .product:hover {
      border-color: #ef5350;
      transform: scale(1.02);
      box-shadow: 0 4px 15px rgba(255, 112, 67, 0.5);
    }

    .product input[type="checkbox"] {
      transform: scale(1.5);
      accent-color: #ff7043;
    }

    .product.selected {
      animation: shake 0.3s ease;
    }

    @keyframes shake {
      0% { transform: translateX(0); }
      25% { transform: translateX(-5px); }
      50% { transform: translateX(5px); }
      75% { transform: translateX(-5px); }
      100% { transform: translateX(0); }
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-top: 1rem;
    }

    input, textarea {
      padding: 0.8rem;
      border: 2px solid #ffca28;
      border-radius: 8px;
      font-size: 1rem;
      transition: all 0.3s ease;
    }

    input:focus, textarea:focus {
      border-color: #ef5350;
      outline: none;
    }

    .submit-btn {
      background: #ffca28;
      color: #4e342e;
      border: none;
      padding: 1rem;
      font-size: 1.2rem;
      font-weight: bold;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 10px rgba(255, 202, 40, 0.5);
      align-self: center;
    }

    .submit-btn:hover {
      background: #ffb300;
      transform: scale(1.05);
    }

    .selected-products {
      margin-top: 1rem;
      color: #ff7043;
      font-weight: bold;
      font-size: 1.1rem;
    }

    .testimonial-grid {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-top: 1rem;
    }

    .testimonial {
      background: #fff;
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      transition: all 0.3s ease;
    }

    .testimonial:hover {
      transform: scale(1.02);
    }

    footer {
      background: #ff7043;
      text-align: center;
      padding: 1.5rem;
      color: white;
      box-shadow: 0 -4px 10px rgba(0, 0, 0, 0.2);
    }

    footer a {
      color: #ffca28;
      text-decoration: none;
      font-weight: bold;
    }

    footer a:hover {
      color: #ffb300;
    }

    /* CSS cho thông báo tùy chỉnh */
    .notification {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #ef5350;
      color: white;
      padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
      z-index: 10001;
      display: none;
      max-width: 300px;
      font-size: 1rem;
      animation: slideInNotification 0.3s ease forwards;
    }

    .notification.active {
      display: block;
    }

    @keyframes slideInNotification {
      from { transform: translateX(100%); opacity: 0; }
      to { transform: translateX(0); opacity: 1; }
    }

    .notification-close {
      position: absolute;
      top: 5px;
      right: 5px;
      background: #d32f2f;
      color: white;
      border: none;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      cursor: pointer;
      font-size: 0.8rem;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s ease;
    }

    .notification-close:hover {
      background: #b71c1c;
      transform: scale(1.1);
    }

    @media (min-width: 600px) {
      .hericium-toggle { padding: 0.8rem 1.2rem; font-size: 1.2rem; }
      .hericium-panel { width: 250px; padding: 1.5rem; }
      .flash-sale-text { font-size: 2rem; }
      .flash-sale-button { padding: 0.8rem 2rem; font-size: 1.4rem; }
      .promo-price { font-size: 1.8rem; }
      .timer-box { font-size: 1.4rem; width: 50px; }
      .main-image { height: 350px; }
      .thumbnail { width: 70px; height: 70px; }
      .top-button { flex-direction: row; justify-content: center; gap: 1.5rem; }
      .button { width: auto; padding: 0.8rem 2rem; font-size: 1.4rem; }
      .section h2 { font-size: 2rem; padding: 0.8rem 2rem; }
      .features h3 { font-size: 1.5rem; }
      .products { flex-direction: row; flex-wrap: wrap; justify-content: center; }
      .product { width: 45%; }
      .submit-btn { font-size: 1.4rem; max-width: 300px; }
      .testimonial-grid { flex-direction: row; flex-wrap: wrap; justify-content: center; }
      .testimonial { width: 45%; }
    }

    @media (min-width: 900px) {
      .product { width: 22%; }
      .testimonial { width: 30%; }
    }
  </style>
</head>
<body>
  <div id="loader"></div>
  <canvas id="particles"></canvas>

  <!-- Thêm phần tử cho thông báo tùy chỉnh -->
  <div class="notification" id="notification">
    <button class="notification-close" onclick="closeNotification()">✕</button>
    <span id="notificationMessage"></span>
  </div>

  <div class="promo-popup" id="promoPopup">
    <button class="promo-close" onclick="closePromo()">✕</button>
    <h2>Ưu Đãi Đặc Biệt!</h2>
    <p>Mua ngay hôm nay để nhận <strong>giảm giá 30%</strong> và miễn phí vận chuyển cho đơn từ 3 gói!</p>
    <button onclick="scrollToSection(event, 'order', true)">Nhận Ngay</button>
  </div>

  <button class="hericium-toggle" id="hericiumToggle" onclick="toggleHericiumPanel()">Menu</button>
  <div class="hericium-panel" id="hericiumPanel">
    <h2>Hericium</h2>
    <ul>
      <li><a href="#advantages" onclick="scrollToSection(event, 'advantages')">Ưu điểm</a></li>
      <li><a href="#usage" onclick="scrollToSection(event, 'usage')">Cách dùng</a></li>
      <li><a href="#order" onclick="scrollToSection(event, 'order')">Đặt mua</a></li>
      <li><a href="#testimonials" onclick="scrollToSection(event, 'testimonials')">Đánh giá</a></li>
    </ul>
  </div>

  <div class="flash-sale-banner">
    <span class="flash-sale-text">Flash Sale - Giảm Sốc 30%</span>
    <button class="flash-sale-button" onclick="scrollToSection(event, 'order')">MUA NGAY</button>
  </div>

  <div class="pricing-countdown">
    <div class="pricing">
      Giá KM: <span class="promo-price">89.000 đ</span> 
      <br>Giá Gốc: <span class="original-price">128.000 đ</span>
    </div>
    <div class="countdown-label">Khuyến mãi kết thúc sau</div>
    <div class="countdown-timer">
      <span class="timer-box" id="hours">00</span>
      <span class="timer-box" id="minutes">00</span>
      <span class="timer-box" id="seconds">00</span>
    </div>
    <div class="remaining-products">Chỉ còn 89 sản phẩm trong kho!</div>
  </div>

  <div class="gallery">
    <img src="https://i.postimg.cc/66jSHhNf/a.jpg" alt="Main Product Image" class="main-image" id="mainImage">
    <button class="nav-button left" onclick="changeImage(-1)">❮</button>
    <button class="nav-button right" onclick="changeImage(1)">❯</button>
    <div class="thumbnails">
      <img src="https://i.postimg.cc/66jSHhNf/a.jpg" alt="Thumbnail 1" class="thumbnail active" onclick="setImage(0)">
      <img src="https://i.postimg.cc/zDnqL6mP/b.jpg" alt="Thumbnail 2" class="thumbnail" onclick="setImage(1)">
      <img src="https://i.postimg.cc/J0RvHTJ9/c.jpg" alt="Thumbnail 3" class="thumbnail" onclick="setImage(2)">
      <img src="https://i.postimg.cc/c1DXc4NK/d.jpg" alt="Thumbnail 4" class="thumbnail" onclick="setImage(3)">
      <img src="https://i.postimg.cc/sDQ99Yc8/e.jpg" alt="Thumbnail 5" class="thumbnail" onclick="setImage(4)">
    </div>
  </div>

  <div class="top-button">
    <a href="#advantages" class="button" onclick="scrollToSection(event, 'advantages')">Ưu điểm</a>
    <a href="#usage" class="button" onclick="scrollToSection(event, 'usage')">Cách dùng</a>
    <a href="#order" class="button" onclick="scrollToSection(event, 'order')">Đặt hàng</a>
  </div>

  <div class="section" id="advantages">
    <h2>ƯU ĐIỂM</h2>
    <div class="features">
      <h3><i class="fas fa-check-circle"></i> Nguyên liệu tự nhiên</h3>
      <p>Bắp ngô non, khoai mỡ tươi, nấm đầu khỉ – sạch, an toàn.</p>
      <h3><i class="fas fa-leaf"></i> Dinh dưỡng vượt trội</h3>
      <p>Thay bữa chính, hỗ trợ giảm cân, tăng miễn dịch.</p>
      <h3><i class="fas fa-heart"></i> Phù hợp mọi đối tượng</h3>
      <p>Người ăn kiêng, tiểu đường, người già, trẻ nhỏ.</p>
      <h3><i class="fas fa-clock"></i> Nhanh chóng, tiện lợi</h3>
      <p>Chỉ 3 phút pha chế, phù hợp người bận rộn.</p>
      <h3><i class="fas fa-globe"></i> Xuất xứ uy tín</h3>
      <p>Sản xuất tại Đài Loan, đạt chuẩn quốc tế.</p>
    </div>
  </div>

  <div class="section" id="usage">
    <h2>CÁCH DÙNG</h2>
    <div class="features">
      <h3><i class="fas fa-utensils"></i> Ăn kiêng</h3>
      <p>Pha 1 gói với 200ml nước sôi.</p>
      <h3><i class="fas fa-candy-cane"></i> Trẻ em</h3>
      <p>Thêm sữa hoặc đường cho bé.</p>
      <h3><i class="fas fa-pepper-hot"></i> Món mặn</h3>
      <p>Kết hợp rau củ, thịt băm.</p>
      <h3><i class="fas fa-snowflake"></i> Giải nhiệt</h3>
      <p>Pha với sữa đặc và đá lạnh.</p>
    </div>
  </div>

  <div class="section" id="order">
    <h2>ĐẶT MUA</h2>
    <div class="products" id="products">
      <label class="product">
        <input type="checkbox" name="products[]" value="Gói 400g" onchange="updateSelectedProducts()"> 1 Gói 400g - 89.000đ + 30k ship
      </label>
      <label class="product">
        <input type="checkbox" name="products[]" value="Combo 2 gói" onchange="updateSelectedProducts()"> Combo 2 gói - 170.000đ + 30k ship
      </label>
      <label class="product">
        <input type="checkbox" name="products[]" value="Combo 3 gói" onchange="updateSelectedProducts()"> Combo 3 gói - 250.000đ + miễn ship
      </label>
      <label class="product">
        <input type="checkbox" name="products[]" value="Combo 5 gói" onchange="updateSelectedProducts()"> Combo 5 gói - 400.000đ + miễn ship
      </label>
    </div>
    <div class="selected-products">
      Sản phẩm đã chọn: <span id="selectedProductsList">Chưa chọn sản phẩm</span>
    </div>
    <form id="orderForm" method="POST" action="https://script.google.com/macros/s/AKfycbxj2cR9N7qbHFUMD2ZK_WDuf7mlkICZdx9onUkIMtTBUbj9tRs7AM7lln0YegmntLGUqw/exec" target="_blank" onsubmit="return validateAndSubmit()">
      <input type="hidden" name="timestamp" id="timestamp">
      <input type="hidden" name="products" id="productsHidden">
      <label for="name">Họ và Tên</label>
      <input type="text" id="name" name="name" required placeholder="Nhập họ tên">
      <label for="phone">Số điện thoại</label>
      <input type="tel" id="phone" name="phone" required placeholder="Nhập số điện thoại" pattern="[0-9]{10}" title="Vui lòng nhập đúng 10 chữ số">
      <label for="address">Địa chỉ</label>
      <textarea id="address" name="address" rows="3" required placeholder="Nhập địa chỉ"></textarea>
      <input type="hidden" name="ip" id="ip">
      <button type="submit" class="submit-btn">XÁC NHẬN</button>
    </form>
    <div id="successMessage" style="display: none; color: #2e7d32; font-size: 1.2rem; margin-top: 1rem;">
      Đơn hàng đã gửi thành công! Chúng tôi sẽ liên hệ sớm.
    </div>
  </div>

  <div class="section" id="testimonials">
    <h2>ĐÁNH GIÁ</h2>
    <div class="testimonial-grid">
      <div class="testimonial">
        <p>"Giảm 3kg sau 2 tuần, vị ngon!"</p>
        <span>- Chị Lan, 32 tuổi</span>
      </div>
      <div class="testimonial">
        <p>"Bé thích lắm, tiêu hóa tốt."</p>
        <span>- Mẹ Hạnh, 28 tuổi</span>
      </div>
      <div class="testimonial">
        <p>"Tiện lợi, đủ chất trong 3 phút."</p>
        <span>- Anh Minh, 35 tuổi</span>
      </div>
    </div>
  </div>

  <footer>
    <p>© 2025 Hericium Corn Co. | Hotline: <a href="tel:123-456-789">123-456-789</a> | Email: <a href="mailto:support@hericiumcorn.com">support@hericiumcorn.com</a></p>
  </footer>

  <script>
    const canvas = document.getElementById('particles');
    const ctx = canvas.getContext('2d');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    const particlesArray = [];
    const numberOfParticles = 50;

    class Particle {
      constructor() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * canvas.height;
        this.size = Math.random() * 5 + 1;
        this.speedX = Math.random() * 1 - 0.5;
        this.speedY = Math.random() * 1 - 0.5;
      }
      update() {
        this.x += this.speedX;
        this.y += this.speedY;
        if (this.size > 0.2) this.size -= 0.01;
      }
      draw() {
        ctx.fillStyle = 'rgba(255, 202, 40, 0.5)';
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fill();
      }
    }

    function initParticles() {
      for (let i = 0; i < numberOfParticles; i++) {
        particlesArray.push(new Particle());
      }
    }

    function animateParticles() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      for (let i = 0; i < particlesArray.length; i++) {
        particlesArray[i].update();
        particlesArray[i].draw();
        if (particlesArray[i].size <= 0.2) {
          particlesArray.splice(i, 1);
          i--;
          particlesArray.push(new Particle());
        }
      }
      requestAnimationFrame(animateParticles);
    }

    initParticles();
    animateParticles();

    window.addEventListener('resize', () => {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    });

    function closePromo() {
      const popup = document.getElementById('promoPopup');
      popup.classList.remove('active');
      setTimeout(() => { popup.style.display = 'none'; }, 300);
    }

    document.addEventListener('DOMContentLoaded', () => {
      const promoPopup = document.getElementById('promoPopup');
      promoPopup.style.display = 'none';
      setTimeout(() => {
        promoPopup.style.display = 'block';
        promoPopup.classList.add('active');
      }, 2000);
    });

    function toggleHericiumPanel() {
      document.getElementById('hericiumPanel').classList.toggle('active');
    }

    function scrollToSection(e, sectionId, closePopup = false) {
      e.preventDefault();
      const section = document.getElementById(sectionId);
      section.scrollIntoView({ behavior: 'smooth' });
      if (closePopup) {
        closePromo();
      }
    }

    const images = [
      "https://i.postimg.cc/66jSHhNf/a.jpg",
      "https://i.postimg.cc/zDnqL6mP/b.jpg",
      "https://i.postimg.cc/J0RvHTJ9/c.jpg",
      "https://i.postimg.cc/c1DXc4NK/d.jpg",
      "https://i.postimg.cc/sDQ99Yc8/e.jpg"
    ];
    let currentIndex = 0;
    let isAnimating = false;

    function changeImage(direction) {
      if (isAnimating) return;
      isAnimating = true;
      const mainImage = document.getElementById("mainImage");
      mainImage.classList.add("fade");
      setTimeout(() => {
        currentIndex = (currentIndex + direction + images.length) % images.length;
        mainImage.src = images[currentIndex];
        mainImage.classList.remove("fade");
        updateThumbnails();
        isAnimating = false;
      }, 500);
    }

    function setImage(index) {
      if (isAnimating || index === currentIndex) return;
      isAnimating = true;
      const mainImage = document.getElementById("mainImage");
      mainImage.classList.add("fade");
      setTimeout(() => {
        currentIndex = index;
        mainImage.src = images[currentIndex];
        mainImage.classList.remove("fade");
        updateThumbnails();
        isAnimating = false;
      }, 500);
    }

    function updateThumbnails() {
      document.querySelectorAll(".thumbnail").forEach((thumb, index) => {
        thumb.classList.toggle("active", index === currentIndex);
      });
    }

    let countdownDuration = 3600 * 1000;
    let endTime = Date.now() + countdownDuration;

    function updateCountdown() {
      const now = Date.now();
      const timeLeft = endTime - now;
      if (timeLeft <= 0) {
        endTime = Date.now() + countdownDuration;
      }
      const hours = Math.floor(timeLeft / (1000 * 60 * 60));
      const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
      document.getElementById("hours").textContent = String(hours).padStart(2, "0");
      document.getElementById("minutes").textContent = String(minutes).padStart(2, "0");
      document.getElementById("seconds").textContent = String(seconds).padStart(2, "0");
    }

    setInterval(updateCountdown, 1000);
    updateCountdown();

    function updateSelectedProducts() {
      const selectedProducts = Array.from(document.querySelectorAll('.product input[type="checkbox"]:checked'))
        .map(checkbox => checkbox.value)
        .join(', ') || 'Chưa chọn sản phẩm';
      document.getElementById('selectedProductsList').textContent = selectedProducts;
      document.getElementById('productsHidden').value = selectedProducts;
      const productLabels = document.querySelectorAll('.product');
      productLabels.forEach(label => {
        const checkbox = label.querySelector('input[type="checkbox"]');
        label.classList.toggle('selected', checkbox.checked);
      });
    }

    async function getIP() {
      const ipApis = [
        'https://api.ipify.org?format=json',
        'https://api.ipgeolocation.io/getIp',
        'https://ipapi.co/json/'
      ];

      for (const api of ipApis) {
        try {
          const response = await fetch(api, { method: 'GET', mode: 'cors' });
          if (!response.ok) throw new Error(`HTTP error! Status: ${response.status}`);
          const data = await response.json();
          return data.ip || 'Không xác định';
        } catch (error) {
          console.error(`Lỗi khi lấy IP từ ${api}:`, error.message);
          continue;
        }
      }
      return 'Không xác định';
    }

    // Hàm hiển thị thông báo tùy chỉnh
    function showNotification(message) {
      const notification = document.getElementById('notification');
      const notificationMessage = document.getElementById('notificationMessage');
      notificationMessage.textContent = message;
      notification.classList.add('active');

      // Tự động đóng sau 3 giây
      setTimeout(() => {
        notification.classList.remove('active');
      }, 3000);
    }

    // Hàm đóng thông báo
    function closeNotification() {
      const notification = document.getElementById('notification');
      notification.classList.remove('active');
    }

    async function validateAndSubmit() {
      const name = document.getElementById("name").value.trim();
      const phone = document.getElementById("phone").value.trim();
      const address = document.getElementById("address").value.trim();
      const selectedProducts = Array.from(document.querySelectorAll('.product input[type="checkbox"]:checked'))
        .map(checkbox => checkbox.value)
        .join(', ') || 'Chưa chọn sản phẩm';

      if (!name) {
        showNotification('Vui lòng nhập họ và tên!');
        document.getElementById("name").focus();
        return false;
      }

      if (!phone) {
        showNotification('Vui lòng nhập số điện thoại!');
        document.getElementById("phone").focus();
        return false;
      }

      if (!/^[0-9]{10}$/.test(phone)) {
        showNotification('Số điện thoại phải có đúng 10 chữ số!');
        document.getElementById("phone").focus();
        return false;
      }

      if (!address) {
        showNotification('Vui lòng nhập địa chỉ!');
        document.getElementById("address").focus();
        return false;
      }

      if (selectedProducts === 'Chưa chọn sản phẩm') {
        showNotification('Vui lòng chọn ít nhất một sản phẩm!');
        return false;
      }

      const timestamp = new Date().toLocaleString('vi-VN');
      const ip = await getIP();

      document.getElementById("timestamp").value = timestamp;
      document.getElementById("productsHidden").value = selectedProducts;
      document.getElementById("ip").value = ip;

      console.log("Dữ liệu gửi đi:", {
        timestamp: timestamp,
        name: name,
        phone: phone,
        address: address,
        ip: ip,
        products: selectedProducts
      });

      const form = document.getElementById("orderForm");
      const successMessage = document.getElementById("successMessage");
      form.style.display = "none";
      successMessage.style.display = "block";
      setTimeout(() => {
        form.style.display = "block";
        successMessage.style.display = "none";
        form.reset();
        document.querySelectorAll('.product input[type="checkbox"]').forEach(cb => {
          cb.checked = false;
          cb.parentElement.classList.remove('selected');
        });
        document.getElementById('selectedProductsList').textContent = 'Chưa chọn sản phẩm';
        document.getElementById('productsHidden').value = '';
      }, 3000);

      return true;
    }
  </script>
</body>
</html>
