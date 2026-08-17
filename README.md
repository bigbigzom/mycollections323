# bigbigzom.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>我的服务与商品</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <!-- 顶部导航 -->
  <header class="navbar">
    <div class="container nav-inner">
      <div class="logo">我的服务站</div>
      <nav>
        <a href="#services">服务</a>
        <a href="#about">关于</a>
        <a href="#contact">联系</a>
      </nav>
    </div>
  </header>

  <!-- Hero 区域 -->
  <section class="hero">
    <div class="container">
      <h1>专业服务，一键获取</h1>
      <p class="subtitle">扫码付款，自动发货，安全便捷</p>
    </div>
  </section>

  <!-- 服务/商品列表 -->
  <section id="services" class="services">
    <div class="container">
      <h2>服务与商品</h2>
      <div id="product-grid" class="product-grid">
        <!-- 商品卡片由 JS 动态渲染 -->
      </div>
    </div>
  </section>

  <!-- 关于 -->
  <section id="about" class="about">
    <div class="container">
      <h2>关于我</h2>
      <p>在这里介绍你的背景、专业领域和服务理念。</p>
    </div>
  </section>

  <!-- 联系 -->
  <section id="contact" class="contact">
    <div class="container">
      <h2>联系方式</h2>
      <p>邮箱：your@email.com</p>
    </div>
  </section>

  <footer class="footer">
    <div class="container">
      <p>&copy; 2026 我的服务站. All rights reserved.</p>
    </div>
  </footer>

  <!-- 付款二维码弹窗 -->
  <div id="payment-modal" class="modal-overlay" style="display:none;">
    <div class="modal">
      <button class="modal-close" onclick="closePaymentModal()">&times;</button>
      <h3 id="modal-product-name">商品名称</h3>
      <p id="modal-product-price" class="price">¥0.00</p>

      <div id="qr-container" class="qr-container">
        <div class="loading">正在生成付款码...</div>
      </div>

      <p class="qr-tip">请使用微信/支付宝扫码支付</p>

      <div id="payment-status" class="payment-status">
        <span class="status-dot"></span>
        <span id="status-text">等待付款...</span>
      </div>

      <div id="download-section" style="display:none;">
        <p class="success-text">付款成功！</p>
        <a id="download-link" class="download-btn" href="#" target="_blank">获取商品/服务</a>
      </div>

      <button class="cancel-btn" onclick="closePaymentModal()">取消</button>
    </div>
  </div>

  <script src="js/config.js"></script>
  <script src="js/app.js"></script>
</body>
</html>
