<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
<html lang="en">
  <div id ="card" class = "card">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="styles.css">
<title>Card Example</title>
</head>
<body>
<div class = "card">
<img src="https://www.mydomaine.com/thmb/CaWdFGvTH4-h1VvG6tukpKuU2lM=/3409x0/filters:no_upscale():strip_icc()/binary-4--583f06853df78c6f6a9e0b7a.jpeg"> 
      
<div class="card-content"> 
          <h4><b>Two Pod Real Estate Agency</b></h4>
<p id = 'description'> Real Estate Company Focused on delivering the best properties for college students at Penn State University in State College, PA</p> 
      <button class="details-button" id="detailsBtn">Details</button>
      </div>
      </div> 
</body> 
  </div>
  <button id ="btn">Duplicate</button>
  <button id="colorBtn">BGColorChanger</button>
  <button id="Headingbtn">HeadingChanger</button>
  <button id ="dltbtn">DeleteCard</button>
  <script>
   document.querySelector('#btn').addEventListener('click', function(e){
const clone = document.querySelector('#card').cloneNode('card');
document.body.appendChild(clone);
     const cardCline = cardToClone.cloneNode(true);
})
</script> 
   <script>
        var numbers = ["1", "2", "3", "4", "5", "6", "7", "8", "9"];
        var letters = ["A", "B", "C", "D", "E", "F"];
        function randomColor() {
            var color = "";
            for (var i = 0; i < 3; i++) {
                var index = Math.floor(Math.random() * (numbers.length + letters.length));
                color += (index < numbers.length) ? numbers[index] : letters[index - numbers.length];
            }
            return color;
        }
       document.querySelector('#colorBtn').addEventListener('click', function (e) {
            const card = document.querySelector('.card');
   
            const currentColor = card.style.backgroundColor;
             card.style.backgroundColor = '#' + randomColor();
        });
    </script>
  <script>
   document.querySelector('#Headingbtn').addEventListener('click', function(e){
      const title = document.querySelector('h4');
      title.innerText = "Super Pod 2 Realty";
    })
  </script>
  <script>
    //card delete
    document.querySelector('#dltbtn').addEventListener('click', function(e){
      const cards = document.querySelectorAll('.card');
      
    if (cards.length > 2) {
        const lastCard = cards[cards.length - 1];
        lastCard.parentNode.removeChild(lastCard);
    }
    })
  </script>
  <script>
    
    var original= document.querySelector('#description').innerText;
document.querySelector('#detailsBtn').addEventListener('click', function(e) {
    const description = document.querySelector('#description');
    
    if (description.innerText === 'none' || description.innerText=== '') {
        description.innerText = original; 
    } else {
        description.innerText = ''; 
    }
});
  </script>
</html> 
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
