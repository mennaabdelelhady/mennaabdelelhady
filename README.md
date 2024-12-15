<h1 align="center">Hi 👋, I'm Menna</h1>
<h3 align="center">A Passionate Backend Developer | Fresh Graduate from FCIS Mansoura, Egypt</h3>

<p align="center">
  <img src="https://github.com/mennaabdelelhady/mennaabdelelhady/blob/main/elota.png" alt="Profile Banner" width="70%"/>
</p>

---

<h2 align="left">Connect with Me</h2>
<p align="left">
  <a href="https://www.linkedin.com/in/menna-abd-el-hady-a59313204" target="_blank" style="text-decoration: none;">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="LinkedIn" height="40" width="40" />
  </a>
  <a href="https://codeforces.com/profile/mennatallahmahmoud" target="_blank" style="text-decoration: none;">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/codeforces.svg" alt="Codeforces" height="40" width="40" />
  </a>
</p>

---

<h2 align="left">About Me</h2>
<p align="left">
  I am a highly motivated backend developer with a strong foundation in PHP and Laravel. As a fresh graduate from FCIS Mansoura, I am eager to apply my skills to build scalable, secure, and efficient web applications. I am passionate about problem-solving and continuously improving my technical expertise.
</p>

---

<h2 align="left">Languages & Tools</h2>
<p align="left">
  <a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" width="60" height="60"/>
  </a>
  <a href="https://www.w3schools.com/cs/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="C#" width="60" height="60"/>
  </a>
  <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3" width="60" height="60"/>
  </a>
  <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5" width="60" height="60"/>
  </a>
  <a href="https://www.mysql.com/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" width="60" height="60"/>
  </a>
  <a href="https://www.python.org" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" width="60" height="60"/>
  </a>
</p>

---

<h2 align="left">Snake Game</h2>
<p align="center">
  <canvas id="snakeGame" width="400" height="400" style="border:1px solid #000;"></canvas>
  <script>
    const canvas = document.getElementById('snakeGame');
    const ctx = canvas.getContext('2d');
    const box = 20;
    let snake = [{ x: 9 * box, y: 10 * box }];
    let food = {
      x: Math.floor(Math.random() * 19 + 1) * box,
      y: Math.floor(Math.random() * 19 + 1) * box
    };
    let direction;

    document.addEventListener('keydown', event => {
      if (event.key === 'ArrowUp' && direction !== 'DOWN') direction = 'UP';
      else if (event.key === 'ArrowDown' && direction !== 'UP') direction = 'DOWN';
      else if (event.key === 'ArrowLeft' && direction !== 'RIGHT') direction = 'LEFT';
      else if (event.key === 'ArrowRight' && direction !== 'LEFT') direction = 'RIGHT';
    });

    function drawGame() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      ctx.fillStyle = 'red';
      ctx.fillRect(food.x, food.y, box, box);
      for (let i = 0; i < snake.length; i++) {
        ctx.fillStyle = i === 0 ? 'green' : 'lightgreen';
        ctx.fillRect(snake[i].x, snake[i].y, box, box);
      }

      let snakeX = snake[0].x;
      let snakeY = snake[0].y;

      if (direction === 'UP') snakeY -= box;
      if (direction === 'DOWN') snakeY += box;
      if (direction === 'LEFT') snakeX -= box;
      if (direction === 'RIGHT') snakeX += box;

      if (snakeX === food.x && snakeY === food.y) {
        food = {
          x: Math.floor(Math.random() * 19 + 1) * box,
          y: Math.floor(Math.random() * 19 + 1) * box
        };
      } else {
        snake.pop();
      }

      const newHead = { x: snakeX, y: snakeY };
      if (
        snakeX < 0 ||
        snakeY < 0 ||
        snakeX >= canvas.width ||
        snakeY >= canvas.height ||
        snake.some(segment => segment.x === newHead.x && segment.y === newHead.y)
      ) {
        clearInterval(game);
        alert('Game Over');
      }

      snake.unshift(newHead);
    }

    const game = setInterval(drawGame, 100);
  </script>
</p>

---

<h2 align="left">Featured Media</h2>
<p align="center">
  <video width="70%" controls>
    <source src="https://github.com/mennaabdelelhady/mennaabdelelhady/blob/main/video_2023-02-17_13-26-49.mp4" type="video/mp4">
    <source src="https://github.com/mennaabdelelhady/mennaabdelelhady/blob/main/video_2023-02-17_13-26-49.ogg" type="video/ogg">
    Your browser does not support the video tag.
  </video>
</p>

---

<h2 align="center">Thank You for Visiting My Profile!</h2>
