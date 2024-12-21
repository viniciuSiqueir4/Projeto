<!DOCTYPE html>
<html lang="br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="estilo.css">
    <title>Login de pagina</title>

</head>
<body id="body">
<div class="header" id="header">



    <div class="logo_header">
        <img src="ee6128f9a6738399d8bdeac97daa7a3d.jfif" alt="Logo Ficticio" class="img_logo_header">
    </div>
    <div class="login">

        <h1>Login</h1>
        <input type="text" placeholder="Nome">
        <br><br>
        <input type="password" placeholder="Senha">
        <br><br>
        <button>Enviar</button>
    </div>
    <div class="navigation_header" id="navigation_header">



        <div class="color_link">
            <a href="index.html" class="active"> Funcionario</a>

        </div>
    </div>
</div>
<div tabindex="0" class="content" onfocus="closeSidebar()" id="content">
    <h2>Cadastro de Cliente</h2>
</div>

</body>
</html>

CSS

:root{
    --color-white: #fff;
    --color-dark1: rgb(39, 39, 39);
    --color-dark2: #2d2d2d;
    --color-dark3: #414141;
    --color-dark4: #1c1c1c;
    --color-dark5: #343434;

}
*{
    margin: 0;
    padding: 0;
}
body{
    font-family: "Arial";
    background-image: linear-gradient(45deg, cyan, blue);
    color: var(--color-white);
}
.img_logo_header{
    width: 45px;
}
.header,
.navigation_header{
    display: flex;
    flex-direction: row;
    align-items: center;
}
.header{
    background-color: black;
    justify-content: space-between;
    padding: 0 10%;
    height: 3.5em;
    box-shadow: 1px 1px 4px var(--color-dark4);
}
.navigation_header{
    gap: 3em;
    z-index: 2;
}
.content{
    padding-top: 5em;
    text-align: center;
    height: 100vh;
    transition: 1s;
}
.navigation_header a{
    text-decoration: none;
    background-image: linear-gradient(45deg, cyan , blue);
    transition: 500ms;
    font-weight: bold;
}
.navigation_header a:hover{
    color: var(--color-white);
}
.active{

    padding: 10px;
    border-radius: 10px;
}
.login{
    background-color: rgba(0, 0, 0, 0.9);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    padding: 80px;
    border-radius: 15px;
    color: #fff;
}
input{
    padding: 15px;
    border: none;
    outline: none;
    font-size: 15px;
}
button {
    background-color: dodgerblue;
    border: none;
    padding: 15px;
    width: 100%;
    border-radius: 10px;
    color: white;
    font-size: 15px;
}

button:hover{
    background-color: deepskyblue;
    cursor: pointer;
}

.btn_icon_header{
    background: transparent;
    border: none;
    color: var(--color-white);
    cursor: pointer;
    display: none;
}
@media screen and (max-width: 768px) {
    .navigation_header{
        position: absolute;
        flex-direction: column !important;
        top: 0;
        background: var(--color-dark5);
        height: 100%;
        width: 35vw;
        padding: 1em;
        animation-duration: 1s;
        margin-left: -100vw;
    }
    .btn_icon_header{
        display: block;
    }
}
@keyframes showSidebar {
    from {margin-left: -100vw;}
    to {margin-left: -10vw;}
}

.color_link{
    color: black;
    font-weight: bold;
}

h2{
    color: black;
    font-family: "Arial"
}

