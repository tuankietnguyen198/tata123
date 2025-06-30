<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Bạn bị troll rồi 😈</title>
  <style>
    body {
      font-family: "Comic Sans MS", cursive, sans-serif;
      text-align: center;
      margin-top: 100px;
      background-color: #f0f0f0;
      transition: background-color 0.5s ease;
    }
    #trollButton {
      padding: 15px 30px;
      font-size: 20px;
      position: absolute;
      background-color: #ff5555;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    #message {
      font-size: 24px;
      color: red;
      display: none;
    }
  </style>
</head>
<body>

  <h1>Bấm nút nếu bạn đủ nhanh 😎</h1>
  <button id="trollButton">Thử Bấm Vào Tao!</button>
  <p id="message">HAHA! Bạn bị troll rồi! 😆</p>

  <audio id="laughSound">
    <source src="https://www.myinstants.com/media/sounds/trollololololol.mp3" type="audio/mpeg">
  </audio>

  <script>
    const button = document.getElementById('trollButton');
    const message = document.getElementById('message');
    const laughSound = document.getElementById('laughSound');

    // Di chuyển nút mỗi khi rê chuột vào
    button.addEventListener('mouseover', () => {
      const x = Math.random() * (window.innerWidth - button.offsetWidth);
      const y = Math.random() * (window.innerHeight - button.offsetHeight);
      button.style.left = `${x}px`;
      button.style.top = `${y}px`;
      document.body.style.backgroundColor = getRandomColor();
    });

    // Khi bấm được nút, hiện thông báo troll + phát âm thanh
    button.addEventListener('click', () => {
      message.style.display = 'block';
      laughSound.play();
      alert("Bạn vừa bị troll! 😝");
    });

    // Hàm tạo màu ngẫu nhiên
    function getRandomColor() {
      const letters = '0123456789ABCDEF';
      let color = '#';
      for (let i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      return color;
    }
  </script>

</body>
</html>
