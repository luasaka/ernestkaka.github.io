<!DOCTYPE html>
<html>
  <head>
    <title>Die Abenteuer von Ernest</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        text-align: center;
      }
      
      h1 {
        font-size: 36px;
        margin-bottom: 20px;
      }
      
      p {
        font-size: 18px;
        margin-bottom: 20px;
      }
      
      button {
        font-size: 18px;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        background-color: lightblue;
        color: white;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <h1>Die Abenteuer von Ernest</h1>
    <p>Ernest war ein aufgeweckter Junge, der immer auf der Suche nach Abenteuern war.</p>
    <p>Eines Tages beschloss er, in den Wald zu gehen, um ein neues Abenteuer zu erleben.</p>
    <p>Wohin soll Ernest gehen?</p>
    <button id="left">Zum Fluss</button>
    <button id="right">Zur Höhle</button>
    
    <script>
      const leftBtn = document.querySelector('#left');
      const rightBtn = document.querySelector('#right');
      
      leftBtn.addEventListener('click', function() {
        document.querySelector('p:last-of-type').innerHTML = 'Ernest besucht den Fluss und trifft auf eine Gruppe von Ottern, die ihm bei seiner Entdeckungsreise helfen.';
        leftBtn.style.display = 'none';
        rightBtn.style.display = 'none';
        const nextBtn = document.createElement('button');
        nextBtn.innerHTML = 'Weiter';
        nextBtn.addEventListener('click', function() {
          alert('Mit den Ottern erkundet Ernest den Fluss und entdeckt eine verborgene Bucht, die er nun als sein geheimes Versteck nutzen kann.');
        });
        document.body.appendChild(nextBtn);
      });
      
      rightBtn.addEventListener('click', function() {
        document.querySelector('p:last-of-type').innerHTML = 'Ernest besucht die Höhle und findet dort eine Schatzkarte, die ihn auf eine spannende Schatzsuche führt.';
        leftBtn.style.display = 'none';
        rightBtn.style.display = 'none';
        const nextBtn = document.createElement('button');
        nextBtn.innerHTML = 'Weiter';
            nextBtn.addEventListener('click', function() {
          alert('Mit der Schatzkarte erkundet Ernest die Gegend und findet schließlich einen großen Schatz, den er mit nach Hause nimmt.');
        });
        document.body.appendChild(nextBtn);
      });
    </script>
  </body>
</html>
