<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>موقعي الشخصي - أدواتي الصحية</title>
  <style>
    body {
      font-family: 'Tahoma', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
    }
    header {
      background-color: #007bff;
      color: white;
      padding: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .site-name {
      font-weight: bold;
      font-size: 20px;
    }
    .language-switch {
      background-color: white;
      color: #007bff;
      border: none;
      padding: 5px 10px;
      cursor: pointer;
      border-radius: 4px;
    }
    nav ul {
      list-style: none;
      padding: 0;
      margin: 0;
      display: flex;
      justify-content: center;
      background-color: #0056b3;
      flex-wrap: wrap;
    }
    nav ul li {
      padding: 15px 20px;
    }
    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      cursor: pointer;
    }
    nav ul li a:hover {
      text-decoration: underline;
    }
    main {
      padding: 30px;
      text-align: center;
    }
    .message-box {
      background-color: white;
      margin: 30px auto;
      padding: 25px;
      max-width: 750px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      display: none;
      transition: all 0.4s ease-in-out;
    }
    .message-box p {
      font-size: 18px;
      line-height: 2;
      margin: 0;
    }
    .service-list {
      text-align: right;
      margin-top: 15px;
    }
    .service-list li {
      margin-bottom: 10px;
      font-size: 17px;
    }
    footer {
      background-color: #222;
      color: white;
      text-align: center;
      padding: 15px;
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>

  <header>
    <div class="site-name">أدواتي الصحية</div>
    <button class="language-switch" onclick="toggleLanguage()">English</button>
  </header>

  <nav>
    <ul>
      <li><a onclick="toggleAbout()"><span class="ar">من نحن</span><span class="en hidden">About Us</span></a></li>
      <li><a onclick="toggleServices()"><span class="ar">الخدمات</span><span class="en hidden">Services</span></a></li>
      <li>
        <a href="https://www.instagram.com/mohamedahmed0591?igsh=bHQ5b2pzdG1ydjV3" target="_blank">
          <span class="ar">معرض الصور</span>
          <span class="en hidden">Gallery</span>
        </a>
      </li>
      <li><a onclick="toggleContact()"><span class="ar">تواصل معنا</span><span class="en hidden">Contact</span></a></li>
    </ul>
  </nav>

  <main>
    <p class="ar">مرحباً بك في موقعي الشخصي!</p>
    <p class="en hidden">Welcome to my personal website!</p>

    <!-- من نحن -->
    <div id="about-message" class="message-box">
      <p class="ar">
        🌊 <strong>نحن نبتكر الخلاطات المائية</strong> بحب وإتقان، نبدأ من نقطة الصفر وننتهي عند ابتسامة عميل راضٍ.<br>
        💙 رؤيتنا ليست فقط منتجات تصل إليكم، بل <strong>علاقات تدوم</strong> وثقة تنمو مع كل قطرة.
      </p>
      <p class="en hidden">
        🌊 <strong>We craft water blends</strong> with care and precision — from scratch to satisfaction.<br>
        💙 Our vision is not just delivering a product, but <strong>building trust and lasting relationships</strong> with every drop.
      </p>
    </div>

    <!-- الخدمات -->
    <div id="services-message" class="message-box">
      <p class="ar"><strong>🛠 خدماتنا:</strong></p>
      <ul class="ar service-list">
        <li>تحضير الخلطات المائية حسب المواصفات المطلوبة.</li>
        <li>توصيل سريع وآمن للعملاء في جميع أنحاء القاهرة.</li>
        <li>خدمة عملاء متميزة ومتابعة بعد التسليم.</li>
      </ul>

      <p class="en hidden"><strong>🛠 Our Services:</strong></p>
      <ul class="en hidden service-list">
        <li>Custom preparation of water-based mixtures to your specifications.</li>
        <li>Fast and secure delivery across Cairo.</li>
        <li>Excellent customer service and post-delivery follow-up.</li>
      </ul>
    </div>

    <!-- تواصل معنا -->
    <div id="contact-message" class="message-box">
      <p class="ar"><strong>📞 رقم الهاتف:</strong> 01145587547</p>
      <p class="ar"><strong>📍 العنوان:</strong> إمبابة - القومية</p>
      <p class="ar"><strong>📸 إنستجرام:</strong>
        <a href="https://www.instagram.com/mohamedahmed0591?igsh=bHQ5b2pzdG1ydjV3" target="_blank" style="color: #007bff; text-decoration: none;">
          @mohamedahmed0591
        </a>
      </p>

      <p class="en hidden"><strong>📞 Phone:</strong> 01145587547</p>
      <p class="en hidden"><strong>📍 Address:</strong> Imbaba - El Qawmeya</p>
      <p class="en hidden"><strong>📸 Instagram:</strong>
        <a href="https://www.instagram.com/mohamedahmed0591?igsh=bHQ5b2pzdG1ydjV3" target="_blank" style="color: #007bff; text-decoration: none;">
          @mohamedahmed0591
        </a>
      </p>
    </div>
  </main>

  <footer>
    <p class="ar">جميع الحقوق محفوظة © 2025</p>
    <p class="en hidden">All rights reserved © 2025</p>
  </footer>

  <script>
    let currentLang = 'ar';

    function toggleLanguage() {
      const arElements = document.querySelectorAll('.ar');
      const enElements = document.querySelectorAll('.en');
      const html = document.documentElement;
      const button = document.querySelector('.language-switch');

      if (currentLang === 'ar') {
        arElements.forEach(el => el.classList.add('hidden'));
        enElements.forEach(el => el.classList.remove('hidden'));
        html.lang = 'en';
        html.dir = 'ltr';
        button.textContent = 'العربية';
        currentLang = 'en';
      } else {
        enElements.forEach(el => el.classList.add('hidden'));
        arElements.forEach(el => el.classList.remove('hidden'));
        html.lang = 'ar';
        html.dir = 'rtl';
        button.textContent = 'English';
        currentLang = 'ar';
      }
    }

    function toggleAbout() {
      showOnly('about-message');
    }

    function toggleServices() {
      showOnly('services-message');
    }

    function toggleContact() {
      showOnly('contact-message');
    }

    function showOnly(idToShow) {
      const allSections = ['about-message', 'services-message', 'contact-message'];
      allSections.forEach(id => {
        const el = document.getElementById(id);
        if (el) el.style.display = (id === idToShow && el.style.display !== 'block') ? 'block' : 'none';
      });
      const target = document.getElementById(idToShow);
      if (target && target.style.display === 'block') {
        target.scrollIntoView({ behavior: 'smooth' });
      }
    }

    window.onload = () => {
      document.querySelectorAll('.ar').forEach(el => el.classList.remove('hidden'));
      document.querySelectorAll('.en').forEach(el => el.classList.add('hidden'));
    };
  </script>

</body>
</html>
