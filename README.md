<!DOCTYPE html>
<html>
    <head>
        <title>Teated</title>
        <script>
            function loe (){
                fetch("https://colab.research.google.com/drive/1QsXIzi0SI3e09XUuTyrgUgDdtIZaeCt5").then(d => d.json()).then(kuva);
            }
            function kuva(tekst){
                    console.log(tekst);
                    v1.innerText=tekst;
                    p1.innerText=tekst[0];
                    s1.innerText=tekst[1];
                }
                
        </script>
    </head>
    <body onload="loe(); setInterval(loe, 10000)">
        Teated: <span id="v1">teate koht </span>
        <input type="button" value="Kuva teade" onclick="loe()"/>
        <h1 id="p1">Pealkirja koht</h1>
        <div id="s1">sisu koht</div>
    </body>
</html>
