- 👋 Hi, I’m @Robin-qwerty
- 👀 And I’m interested in coding
- 🌱 I’m currently learning to make apps using xamarin in C# and making websites in HTML, CSS & PHP and laravel
- 🌱 And I would like to learn python, javascript or typescript

<!---
Robin-qwerty/Robin-qwerty is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<div class="header">
  <div class="title">
    <h1 id="title" data-value="ROBIN-QWERTY">ROBIN-QWERTY</h1>
  </div>
</div>

<script>
  const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  let interval = null;

  function animateTitle(title) {
    let iteration = 0;
    clearInterval(interval);
    interval = setInterval(() => {
      title.innerText = title.dataset.value
        .split("")
        .map((letter, index) => {
          if (index < iteration) {
            return letter;
          }
          return letters[Math.floor(Math.random() * 26)];
        })
        .join("");
      if (iteration >= title.dataset.value.length) {
        clearInterval(interval);
      }
      iteration += 1 / 3;
    }, 70);
  }

  const title = document.querySelector("#title");

  if (performance.navigation.type == performance.navigation.TYPE_RELOAD) {
    animateTitle(title);
  }

  title.addEventListener("mouseover", () => {
    animateTitle(title);
  });

</script>
<style>
  .header {
    background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
    padding: 5px;
    text-align: center;
    font-family: 'Sofia';
    font-size: 35px;
  }

  .title {
    display: grid;
    place-items: center;
  }

  .title h1 {
    -webkit-user-select: none; /* Safari */
    -ms-user-select: none; /* IE 10 and IE 11 */
    user-select: none; /* Standard syntax */
    font-family: "Space Mono", monospace;
    font-weight: bold;
    font-size: 65px;
    margin: 25px 0;
    max-width: 100%;
    max-height: 200px;
    padding: 5px;
    background: transparent;
    border: 25px solid rgba(0,0,0,0.9);
    border-radius: 25px;
    box-shadow: 0 8px 40px 0 rgba(0,0,0,1);
    background-image: url(https://robin.humilis.net/media/giphy.gif);
    background-size: cover;
    -webkit-background-clip: text;
    color: transparent;

    animation: fadename 1.5s ease-in;
  }
</style>
