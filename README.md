<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Holograma</title>

<style>
html,body{
    margin:0;
    width:100%;
    height:100%;
    background:black;
    overflow:hidden;
}

#inicio{
    position:fixed;
    width:100%;
    height:100%;
    background:black;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    color:white;
    text-align:center;
    z-index:10;
}

button{
    padding:15px 30px;
    font-size:18px;
    margin-top:20px;
}

iframe{
    width:100vw;
    height:100vh;
    border:none;
    display:none;
}
</style>

</head>
<body>

<div id="inicio">

<h2>Experiencia Holográfica</h2>

<p>
Gire el teléfono horizontalmente y presione iniciar.
</p>

<button onclick="iniciar()">
Iniciar experiencia
</button>

</div>

<iframe
id="video"
allow="autoplay; fullscreen"
allowfullscreen>
</iframe>

<script>

function iniciar(){

    document.getElementById("inicio")
    .style.display = "none";

    const iframe =
    document.getElementById("video");

    iframe.style.display = "block";

    iframe.src =
    "https://www.youtube.com/embed/NCXKdQSWzRY?autoplay=1&mute=1&loop=1&playlist=NCXKdQSWzRY&controls=0&rel=0&modestbranding=1&playsinline=1";

    if(document.documentElement.requestFullscreen){

        document.documentElement
        .requestFullscreen();

    }

}

</script>

</body>
</html>
