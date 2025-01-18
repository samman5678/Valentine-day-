<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Valentine's Day Proposal</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f8c6d8;
      color: #333;
      margin: 0;
      padding: 0;
    }
    .container {
      margin-top: 20%;
    }
    button {
      background-color: #ff5c5c;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 18px;
      cursor: pointer;
      border-radius: 5px;
      margin: 10px;
    }
    button:hover {
      background-color: #ff1c1c;
    }
    .heart {
      display: none;
      font-size: 100px;
      color: red;
      animation: pop 1s infinite alternate;
    }
    .crackers {
      display: none;
      margin: 20px auto;
      width: 200px;
      height: 200px;
      background: url('https://i.gifer.com/origin/93/939f646f0d8fdc4d4f6c9477c1f465cd.gif') center/contain no-repeat;
    }
    @keyframes pop {
      from { transform: scale(1); }
      to { transform: scale(1.2); }
    }
  </style>
</head>
<body>
  <div class="container" id="questionPage">
    <h1>Do you love me?</h1>
    <button onclick="yesOption()">Yes</button>
    <button onclick="noOption()">No</button>
  </div>

  <div class="container" id="repeatQuestionPage" style="display: none;">
    <h1>Do you love me?</h1>
    <button onclick="loveYouToo()">I love you too</button>
    <button onclick="hateYou()">I hate you</button>
  </div>

  <div class="container" id="finalPage" style="display: none;">
    <h1>I love you too! ❤️😘</h1>
    <button onclick="loveYouToo()">Click Me</button>
  </div>

  <div class="container" id="heartDisplay" style="display: none;">
    <div class="heart">❤️</div>
    <div class="crackers"></div>
    <h1>I Love You! Happy Valentine's Day! 💕</h1>
  </div>

  <script>
    function yesOption() {
      document.getElementById('questionPage').style.display = 'none';
      document.getElementById('heartDisplay').style.display = 'block';
      document.querySelector('.heart').style.display = 'block';
      document.querySelector('.crackers').style.display = 'block';
    }

    function noOption() {
      document.getElementById('questionPage').style.display = 'none';
      document.getElementById('repeatQuestionPage').style.display = 'block';
    }

    function loveYouToo() {
      document.getElementById('repeatQuestionPage').style.display = 'none';
      document.getElementById('finalPage').style.display = 'none';
      document.getElementById('heartDisplay').style.display = 'block';
      document.querySelector('.heart').style.display = 'block';
      document.querySelector('.crackers').style.display = 'block';
    }

    function hateYou() {
      document.getElementById('repeatQuestionPage').style.display = 'none';
      document.getElementById('finalPage').style.display = 'block';
    }
  </script>
</body>
</html>
