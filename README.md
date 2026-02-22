<!DOCTYPE html>
<html>
<head>
  <title>Sorry</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      background-color: #ffe6eb;
      margin-top: 120px;
    }
    button {
      font-size: 20px;
      padding: 15px 30px;
      margin: 15px;
      border-radius: 12px;
      border: none;
      cursor: pointer;
    }
    #yes {
      background-color: #ccc;
    }
    #no {
      background-color: #ff4d6d;
      color: white;
      font-size: 20px;
      padding: 15px 30px;
    }
  </style>
</head>
<body>

  <h1 id="message">I'm sorry 😞</h1>
  <div id="buttons">
    <button onclick="nextStep()">Continue</button>
  </div>

  <script>
    let noSize = 20;

    function nextStep() {
      document.getElementById("message").innerHTML = "Are you still mad?";
      document.getElementById("buttons").innerHTML = `
        <button id="yes" onclick="growNo()">Yes</button>
        <button id="no" onclick="finalMessage()">No</button>
      `;
    }

    function growNo() {
      noSize += 10;
      const noButton = document.getElementById("no");
      noButton.style.fontSize = noSize + "px";
      noButton.style.padding = (noSize / 2) + "px " + (noSize) + "px";
    }

    function finalMessage() {
      document.body.innerHTML = "<h1>okay.</h1>";
    }
  </script>

</body>
</html>
