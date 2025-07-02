
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>دَفْتُرُكَ صَدَقَتُكَ</title>
  <style>
    body {
      font-family: 'Amiri', 'Segoe UI', Tahoma, sans-serif;
      background: #f3f8f4;
      margin: 0;
      padding: 0;
      color: #274d27;
      line-height: 1.6;
      direction: rtl;
      text-align: right;
    }

    @import url('https://fonts.googleapis.com/css2?family=Amiri&display=swap');

    header {
      background: linear-gradient(to right, #4caf50, #2e7d32);
      color: white;
      padding: 25px 15px;
      text-align: center;
      border-bottom: 5px solid #c8e6c9;
      font-weight: bold;
      font-size: 1.8em;
      letter-spacing: 0.08em;
    }

    header p {
      font-size: 1.1em;
      font-weight: normal;
      margin-top: 8px;
      font-style: italic;
    }

    .container {
      max-width: 700px;
      margin: 30px auto;
      background: #ffffff;
      padding: 25px 30px;
      border-radius: 18px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.12);
      border: 2px solid #a5d6a7;
    }

    .message h2 {
      font-size: 1.6em;
      margin-bottom: 10px;
      color: #2e7d32;
      text-decoration: underline wavy #388e3c;
      text-underline-offset: 6px;
    }

    .message p {
      font-size: 1.15em;
      text-align: justify;
      text-justify: inter-word;
      margin-bottom: 20px;
      word-spacing: 0.15em;
    }

    form h3 {
      font-size: 1.4em;
      margin-bottom: 15px;
      color: #2e7d32;
      font-weight: bold;
      letter-spacing: 0.05em;
    }

    input, textarea {
      width: 100%;
      padding: 14px 15px;
      margin-top: 12px;
      border: 2px solid #9ccc65;
      border-radius: 10px;
      font-size: 1.1em;
      font-family: 'Amiri', serif;
      transition: border-color 0.3s ease;
      outline: none;
      resize: none;
      box-sizing: border-box;
    }

    input:focus, textarea:focus {
      border-color: #4caf50;
      box-shadow: 0 0 8px #81c784;
    }

    button {
      width: 100%;
      background-color: #4caf50;
      color: white;
      border: none;
      padding: 16px;
      margin-top: 25px;
      border-radius: 12px;
      font-size: 1.25em;
      cursor: pointer;
      font-weight: bold;
      transition: background-color 0.3s ease;
      letter-spacing: 0.05em;
    }

    button:hover {
      background-color: #388e3c;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #e8f5e9;
      margin-top: 50px;
      font-size: 1em;
      color: #555;
      font-family: 'Amiri', serif;
      letter-spacing: 0.03em;
    }
  </style>
</head>
<body>

<header>
  دَفْتُرُكَ صَدَقَتُكَ
  <p>شَارِكِ الْعِلْمَ وَابْدَأْ صَدَقَتَكَ الْجَارِيَةَ بِدَفْتَرٍ!</p>
</header>

<div class="container">
  <div class="message">
    <h2>فِكْرَةُ اَلَصَدَقَهـ</h2>
    <p>
      بَدَلَ أَنْ تَرْمِيَ دَفَاتِرَكَ الْقَدِيمَةَ، تَبَرَّعْ بِهَا لِمَنْ يَحْتَاجُهَا. هُنَاكَ طُلاَّبٌ لَا يَمْلِكُونَ الْقُدْرَةَ عَلَى شِرَاءِ الْأَدَوَاتِ الْمَدْرَسِيَّةِ.
      سَاهِمْ فِي نَشْرِ الْعِلْمِ وَكُنْ سَبَبًا فِي رَسْمِ ابْتِسَامَةِ طَالِبٍ!
    </p>
  </div>

  <form id="donationForm">
    <h3>هَلْ تَرْغَبُ بِالتَّبَرُّعِ؟ اِمْلَأِ الْبَيَانَاتِ:</h3>
    <input type="text" id="name" placeholder="الاسْمُ الْكاملُ" required />
    <input type="text" id="city" placeholder="الْمَدِينَةُ / الْمِنْطَقَةُ" required />
    <textarea rows="4" id="details" placeholder="عَدَدُ الدَّفَاتِرِ وَنَوْعُهَا" required></textarea>
    <button type="submit">أَرْسِلِ التَّبَرُّعَ عَبْرَ وَاتْسَاب</button>
  </form>
</div>

<footer>
  تَمَّ التَّنْفِيذُ بِوَاسِطَةِ مُتَطَوِّعِينَ – صَدَقَةٌ جَارِيَةٌ ❤️
</footer>

<script>
  document.getElementById("donationForm").addEventListener("submit", function (e) {
    e.preventDefault();

    const name = document.getElementById("name").value;
    const city = document.getElementById("city").value;
    const details = document.getElementById("details").value;

    const message = `السلام عليكم،\nأرغب بالتبرع بدفاتر.\nالاسم: ${name}\nالمنطقة: ${city}\nالتفاصيل: ${details}`;
    const phone = "967780277099"; // مفتاح اليمن + الرقم
    const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;

    window.open(url, "_blank");
  });
</script>

</body>
</html>![Uploading 4a3be679-8e5c-4b8a-8ac0-4f4e70aaabf0_0_watermark.jpeg…]()
