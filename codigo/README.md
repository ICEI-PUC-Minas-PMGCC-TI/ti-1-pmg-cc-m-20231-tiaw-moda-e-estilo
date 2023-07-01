# Código do Projeto

// Pagina Principal


    <!DOCTYPE html>
    <html>

    <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TIAW</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-qKXV1j0HvMUeCBQ+QVp7JcfGl760yU08IQ+GpUo5hlbpg51QRiuqHAJz8+BrxE/N"
        crossorigin="anonymous"></script>
    <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
    <script src="https://kit.fontawesome.com/6bd401535f.js" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/dom-to-image/2.6.0/dom-to-image.min.js"></script>
    <script src="js/dom-to-image.min.js"></script>
    </head>

    <body>
    <header>
        <img src="img/logo.png" alt="" class="logo">
        <!--BARRA DE PESQUISA-->
        <form class="search-form">
            <input type="search" placeholder="Search Looks..." class="search-input">
            <button type="submit"> <i class="fa-solid fa-magnifying-glass"></i></button>
        </form>
    </header>

    <!-- MENU -->
    <nav class="menu">
        <div class="expandir"><i class="fa-sharp fa-solid fa-bars"></i></div>
        <ul>
            <li class="item-menu ativo">
                <a href="#">
                    <span class="icon"><i class="fa-solid fa-house"></i></span>
                    <span class="txt">Home</span><!--colocar link-->
                </a>
            </li>
            <li class="item-menu">
                <a href="indexJ.html">
                    <span class="icon"><i class="fa-solid fa-user"></i></span>
                    <span class="txt">Perfil</span><!--colocar link-->
                </a>
            </li>
            <li class="item-menu">
                <a href="indexVM2.html">
                    <span class="icon"><i class="fa-solid fa-bag-shopping"></i></i></span>
                    <span class="txt"> Cadastro de Roupas </span><!--colocar link-->
                </a>
            </li>
            <li class="item-menu">
                <a href="login.html">
                    <span class="icon"><i class="fa-solid fa-right-to-bracket"></i></span>
                    <span class="txt">Login</span><!--colocar link-->
                </a>
            </li>
            <li class="item-menu">
                <a href="indexVM.html">
                    <span class="icon"><i class="fa-solid fa-circle-info"></i></span>
                    <span class="txt">Informação</span> <!--colocar link-->
                </a>
            </li>
        </ul>
    </nav>
    <!-- MENU -->

    <button class="salvar" onclick="salvarImagem()">Save Look</button>
  
    <button class="filtro escuras" onclick="filtrarImagensEscuras()" id="filtro-button-escuras">Escuras(shein)</button>
    <button class="filtro pouca-pele" onclick="filtrarImagensPoucaPele()" id="filtro-button-poucapele">Pouca Revelada(shein)</button>

    <div class="container">
        <div class="area-a" id="area-a">
            <div class="bloco1">
                <!-- Conteúdo do bloco 1 -->
            </div>
            <div class="bloco2">
                <!-- Conteúdo do bloco 2 -->
            </div>
        </div>

        <!-- ROUPAS DE CIMA-->
        <div class="area-b">
            <h1 class="titulos">Peças Superiores</h1>
            <img class="superiorm notpoucapele" src="img/blusaPreta.png" alt="Imagem 1">
            <img class="superiorm " src="img/MangaLonga.png" alt="Imagem 2">
            <img class="superiorm notescuras" src="img/SobretudoBege.png" alt="Imagem 3">
            <img class="superiorm notescuras notpoucapele" src="img/blusaBranca.png" alt="Imagem 4">
            <img class="superiorm notescuras notpoucapele" src="img/blusaAzul.png" alt="Imagem 5">
        </div>
        <!-- ROUPAS DE BAIXO-->
        <div class="area-c">
            <h1 class="titulos">Peças Inferiores</h1>
            <img class="inferiorm notescuras " src="img/calçaJeans.png" alt="Imagem 4">
            <img class="inferiorm " src="img/calçaPreta.png" alt="Imagem 5">
            <img class="inferiorm notescuras " src="img/calçaMarron.png" alt="Imagem 6">
            <img class="inferiorm notpoucapele" src="img/ShortPreto.png" alt="Imagem 7">
        </div>
    </div>

    <script>
        const menuItem = document.querySelectorAll('.item-menu');

        function selectLink() {
            menuItem.forEach((item) => item.classList.remove('ativo'));
            this.classList.add('ativo');
        }

        menuItem.forEach((item) => item.addEventListener('click', selectLink));

        const superiores = document.querySelectorAll('.superiorm');
        const inferiores = document.querySelectorAll('.inferiorm');
        const imagemA = document.getElementById('imagemA');
        const bloco1 = document.querySelector('.bloco1');
        const bloco2 = document.querySelector('.bloco2');
        const filtroButtonEscuras = document.querySelector('#filtro-button-escuras');
        const filtroButtonPoucaPele = document.querySelector('#filtro-button-poucapele');

        function selecionarImagem(event) {
            const imagemSelecionada = event.target.getAttribute('src');
            const imagem = document.createElement('img');
            imagem.setAttribute('src', imagemSelecionada);

            if (event.target.classList.contains('superiorm')) {
                // Imagem superior selecionada
                // Adiciona a imagem ao bloco 1
                bloco1.innerHTML = ''; // Remove as imagens existentes no bloco 1
                bloco1.appendChild(imagem);
            } else if (event.target.classList.contains('inferiorm')) {
                // Imagem inferior selecionada
                // Adiciona a imagem ao bloco 2
                bloco2.innerHTML = ''; // Remove as imagens existentes no bloco 2
                bloco2.appendChild(imagem);
            }

            imagemA.setAttribute('src', imagemSelecionada);
        }

        superiores.forEach((superior) => {
            superior.addEventListener('click', selecionarImagem);
        });

        inferiores.forEach((inferior) => {
            inferior.addEventListener('click', selecionarImagem);
        });

        function salvarImagem() {
            const areaA = document.getElementById('area-a');
            domtoimage.toPng(areaA)
                .then(function (dataUrl) {
                    const link = document.createElement('a');
                    link.href = dataUrl;
                    link.download = 'imagem.png';
                    link.click();
                })
                .catch(function (error) {
                    console.error('Erro ao salvar imagem:', error);
                });
        }

        function filtrarImagensEscuras() {
            const imagensFiltradas = document.querySelectorAll('.notescuras');

            imagensFiltradas.forEach(function (imagem) {
                if (filtroButtonEscuras.classList.contains('ligado')) {
                    imagem.style.display = 'block';
                } else {
                    imagem.style.display = 'none';
                }
            });

            filtroButtonEscuras.classList.toggle('ligado');
        }

        function filtrarImagensPoucaPele() {
            const imagensFiltradas = document.querySelectorAll('.notpoucapele');

            imagensFiltradas.forEach(function (imagem) {
                if (filtroButtonPoucaPele.classList.contains('ligado')) {
                    imagem.style.display = 'block';
                } else {
                    imagem.style.display = 'none';
                }
            });

            filtroButtonPoucaPele.classList.toggle('ligado');
        }
    </script>
    </body>

    </html>

    /* Header */
      header {
    background-color: #25142d;
    border-bottom: 3px solid #d42637;
    display: flex;
    align-items: center;
    }
  
    body {
    background-color: #25142d;
    }



    /* Logo */
    .logo {
    max-width: 5%;
    height: auto;
    }

      /* Search Form */
    .search-form {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 0px;
    height: 60px;
    color: black;
    padding-left: 200px;
    background-color: #25142d;
    }

    .search-input::placeholder {
    color: black;
    }

    input[type="search"] {
    padding: 5px;
    border: 0px solid #d42637;
    border-radius: 4px;
    width: 600px;
    background-color: #d42637;
    color: black;
    }

    button[type="submit"] {
    padding: 5px 10px;
    background-color: #d42637;
    border: none;
    border-radius: 4px;
    margin-left: 5px;
    }

    button[type="submit"] i {
    color: black;
    }

    button[type="submit"]:hover {
    background-color: white;
    }

    /* Menu */


    nav.menu {
    width: 100px;
    height: 200%;
    background-color: #25142d;
    padding: 40px 0px 40px 0px;
    box-shadow: 3px 0px 0 #d42637;
    position: fixed;
    overflow: hidden;
    transition: 0.5s;
    background-color: #25142d;
    }

    nav.menu:hover {
    width: 300px;
    background-color: #25142d;
      }

      .expandir {
    width: 100%;
    padding-left: 45px;
    background-color: #25142d;
    }

    .expandir>i {
    font-size: 20px;
    cursor: pointer;
    color: #d42637;
    margin-bottom: 40px;
    background-color: #25142d;
    }
    
    ul {
    height: 100%;
    list-style-type: none;
    background-color: #25142d;
    }

    ul li.item-menu:hover {
    background: #d42637;
    }

    ul li.item-menu.ativo a {
    color: #25142d;
    transition: 0.5s;
    background-color: #d42637;
    }

    ul li.item-menu {
    transition: 0.5s;
    }

    ul li.item-menu:hover a {
    color: #25142d;
    }

    ul li.item-menu a {
    color: #d42637;
    text-decoration: none;
    font-size: 30px;
    padding: 20px 4%;
    display: flex;
    margin-bottom: 40px;
    line-height: 40px;
    padding-left: 10px;
    }

    ul li.item-menu a .txt {
    margin-left: 30px;
    }
  
    /* Containers */
    .container {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    grid-gap: 40px;
    margin-left: 180px;
    margin-top: 40px;
    margin-right: 100px;
    border-color: 2px  #25142d;
   
    
    
    
    
      }

    .area-a {
    border: 1px solid  black;
    width: 500px;
    height: 700px;
    background-size: cover;
    background-position: center;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr;
    grid-gap: 0px;
  

    }

    .bloco1 {
    grid-row: 1;
    border: 2px black;
    max-height: 90%;
    overflow-y: auto;
    
    }
  
      .bloco2 {
    grid-row: 2;
    overflow-y: auto;
    max-height: 100%;
    margin-top: 0%;
  
      }

    .area-b {
    border: 1px solid  black;
    background-color: #25142d;
    width: 300px;
    height: 600px;
    overflow-y: scroll;
    
    }

    .area-c {
    border: 1px solid  black;
    width: 300px;
    height: 600px;
    overflow-y: scroll;
    background-color: #25142d;
    }
    
    .titulos {
        background-color: #25142d;
        justify-content: center;
        align-items: center;
        display: flex;
        color: #d42637;
        position: absolute;
        width: 300px;
        font-family: Georgia, 'Times New Roman', Times, serif;
        align-items: flex-start;
        font-size: 20px;
        height: 30px;
    }

    /*IMAGENS*/

    .area-a img {
    max-width: 100%;
    max-height: 100%;
    display: block;
    margin: 0 auto;
      }

    .area-b img,
    .superiorm,
    .inferiorm {
      max-width: 100%;
    max-height: 100%;
    display: block;
    margin: 0 auto;
    margin-top: 20px;
    border: #25142d;
  
      }
      .area-c img,
            .superiorm,
    .inferiorm {
      max-width: 100%;
      max-height: 100%;
      display: block;
      margin: 0 auto;
      margin-top: 20px;
      border: #25142d;
      
    }

    .salvar {
    background-color: #25142d;
    color: #d42637;
    outline: none;
    border: none;
    font-weight: bold;
    font-family: Georgia, 'Times New Roman', Times, serif;
    width: 500px;
    margin-left: 288px;
    margin-right: 147px;
    margin-bottom: 10px;
    margin-top: 10px;
    position: static;
    }

    .salvar:hover {
    background-color: #d42637;
    color: #25142d;
    outline: none;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-weight: bold;
    }

    .filtro {
    background-color: #25142d;
    color: #d42637;
    outline: none;
    border: none;
    font-weight: bold;
    font-family: Georgia, 'Times New Roman', Times, serif;
    width: 300px;
    margin-right: 43px;
    
   
    
    
     
      }
              @media screen and (max-width: 1568px)
      {
       .filtro{
  
    width: 200px;
    
         }
      .salvar{
        width: 200px;
      }
 
      }

      .filtro:hover {
    background-color: #d42637;
    color: #25142d;
    outline: none;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-weight: bold;
      }
  
      /* ... Estilos CSS anterior ... */


    
      .filtro.ligado {
      background-color: #d42637;
      color: #25142d;
      /* Estilo para os botões de filtro ligados */
      }



      .filtro.pouca-pele.ligado {
        background-color: #d42637;
      color: #25142d;
      /* Estilo para o botão de filtro 'Pouca pele' ligado */
      }

      /* ... Estilos CSS posterior ... */

      /* Scrollbar */
      ::-webkit-scrollbar {
    width: 8px;
      }
    
    ::-webkit-scrollbar-thumb {
    background-color: #d42637;
    }

    ::-webkit-scrollbar-thumb:hover {
    background-color: #d42637;
    }

      ::-webkit-scrollbar-track {
    background-color: #25142d;
    }

      /* Media Queries */

      @media (max-width: 900px){
    nav.menu {
        display: none;}
    

      }
      @media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
        margin-left: 50px;
        margin-right: 50px;
    }

    .area-a {
        width: 100%;
    }

    .area-b,
    .area-c {
        width: 100%;
        margin-top: 20px;
    }

    .salvar {
        width: 100%;
        margin-left: 0;
        margin-right: 0;
    }
        }

      @media (max-width: 480px) {
    .search-form {
        padding-left: 20px;
        padding-right: 20px;
    }

    input[type="search"] {
        width: 100%;
    }

    nav.menu {
        padding-left: 20px;
        padding-right: 20px;
    }

    .expandir>i {
        margin-bottom: 20px;
    }

    ul li.item-menu a {
        font-size: 20px;
        padding: 15px 4%;
    }
    nav.menu {
        display: none;}

      }

//Pagina de Perfil
           
            
            <!DOCTYPE html>
            <html>

            <head>
  
 
  
  
      <title>Meu Perfil</title>
      <link href="styleJ.css" rel="stylesheet" type="text/css" />
      <script src="script.js"></script>
        <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Poppins">
    <link rel="shortcut icon" href="favicon.ico">
  
    <style>
      body,h1,h2,h3,h4,h5 {font-family: "Poppins", sans-serif}
      body {font-size:16px;}
      .w3-half img{margin-bottom:-6px;margin-top:16px;opacity:0.8;cursor:pointer}
    .w3-half img:hover{opacity:1}
    
    /* Estilo do menu */
    .w3-sidebar {
      background-color: #25142d;
      color: #d42637;
    }
    </style>
      </head>
      
      <body>
      
        <!-- Sidebar/menu -->
          <nav class="w3-sidebar w3-collapse w3-top w3-large w3-padding" style="z-index:3;width:300px;font-weight:bold;" id="mySidebar"><br>
            <a href="javascript:void(0)" onclick="w3_close()" class="w3-button w3-hide-large w3-display-topleft" style="width:100%;font-size:22px">Close Menu</a>
             <div class="w3-container">
              <img src="img/Trendy.jpg" alt="Logo Trendy"style="width: 100%; height: auto;">
            
            </div>
            <div class="w3-bar-block">
              <a href="index.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;">Home</a> 
              <a href="indexJ.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;">Perfil</a> 
              <a href="indexVM2.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;"  >Cadastro de Roupas</a> 
              <a href="indexVM.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;" >Informações</a> 
              <a href="login.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;" >Login</a> 
            </div>
          
          </nav>
          
      
      <!-- Top menu on small screens -->
      <header class="w3-container w3-top w3-hide-large w3-red w3-xlarge w3-padding">
        <a href="javascript:void(0)" class="w3-button w3-red w3-margin-right" onclick="w3_open()">☰</a>
        <span>Trendy - The LookBook</span>
      </header>
      
      <!-- Overlay effect when opening sidebar on small screens -->
      <div class="w3-overlay w3-hide-large" onclick="w3_close()" style="cursor:pointer;" title="close side menu" id="myOverlay"></div>
      
        
        <div class="container" style="margin-top: 100px; margin-left: 450px;">
          <div class="profile">
            <div id="profile-image" class="profile-image"></div>
            <div class="profile-info">
              <h2 id="name-content">Nome</h2>
              <input type="text" id="name-textarea" style="display: none;">
              <button id="name-edit-button" class="edit-button" onclick="toggleEditMode('name')">Editar</button>
              <button id="name-save-button" class="edit-button" style="display: none;" onclick="saveField('name')">Salvar</button>
              <p>Usuário: @usuario</p>
              <p>Email: exemplo@example.com</p>
              <input type="file" accept="image/*" onchange="handleFileSelect(event)">
            </div>
          </div>
      
          <div class="bio">
            <h2>Biografia</h2>
            <div id="bio-content">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam in elit vel tortor commodo convallis vitae
                at tortor. Duis suscipit pulvinar magna, vitae consequat enim mollis eget. Sed a ante pharetra, lobortis nulla
                sit amet, gravida urna.</p>
            </div>
            <textarea id="bio-textarea" style="display: none;"></textarea>
            <button id="bio-edit-button" class="edit-button" onclick="toggleEditMode('bio')">Editar</button>
            <button id="bio-save-button" class="edit-button" style="display: none;" onclick="saveField('bio')">Salvar</button>
          </div>
        </div>
      
      <script>
      // Script to open and close sidebar
      function w3_open() {
        document.getElementById("mySidebar").style.display = "block";
        document.getElementById("myOverlay").style.display = "block";
      }
       
      function w3_close() {
        document.getElementById("mySidebar").style.display = "none";
        document.getElementById("myOverlay").style.display = "none";
      }
      
      // Modal Image Gallery
      function onClick(element) {
        document.getElementById("img01").src = element.src;
        document.getElementById("modal01").style.display = "block";
        var captionText = document.getElementById("caption");
        captionText.innerHTML = element.alt;
      }
      </script>
        
      </body>
      </html>

// Pagina de Informações 

      <!DOCTYPE html>
      <html lang="pt-br">
      <head>
      <title>Mais Informações</title>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
      <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Poppins">
      <link rel="shortcut icon" href="img/favicon.ico">
      
      <style>
          body,h1,h2,h3,h4,h5 {font-family: "Poppins", sans-serif}
          body {font-size:16px;}
          .w3-half img{margin-bottom:-6px;margin-top:16px;opacity:0.8;cursor:pointer}
          .w3-half img:hover{opacity:1}
          
          /* Estilo do menu */
          .w3-sidebar {
            background-color: #25142d;
            color: #d42637;
            
          }
        /* Scrollbar */
      ::-webkit-scrollbar {
          width: 8px;
      }
      
      ::-webkit-scrollbar-thumb {
          background-color: #d42637;
      }
      
      ::-webkit-scrollbar-thumb:hover {
          background-color: #d42637;
      }
      
      ::-webkit-scrollbar-track {
          background-color: #25142d;
      }
          </style>
          </head>
          
          <body>
          
          <!-- Sidebar/menu -->
          <nav class="w3-sidebar w3-collapse w3-top w3-large w3-padding" style="z-index:3;width:300px;font-weight:bold;" id="mySidebar"><br>
            <a href="javascript:void(0)" onclick="w3_close()" class="w3-button w3-hide-large w3-display-topleft" style="width:100%;font-size:22px">Close Menu</a>
            <div class="w3-container">
              <img src="img/Trendy.jpg" alt="Logo Trendy"style="width: 100%; height: auto;">
            
            </div>
            <div class="w3-bar-block">
              <a href="index.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;">Home</a> 
              <a href="indexJ.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;">Perfil</a> 
              <a href="indexVM2.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;"  >Cadastro de Roupas</a> 
              <a href="indexVM.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;" >Informações</a> 
              <a href="login.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white" style="margin-bottom:40px; padding-left: 50px;" >Login</a> 
            </div>
          </nav>
          
      
      <!-- Top menu on small screens -->
      <header class="w3-container w3-top w3-hide-large w3-red w3-xlarge w3-padding">
        <a href="javascript:void(0)" class="w3-button w3-red w3-margin-right" onclick="w3_open()">☰</a>
        <span>Trendy - The LookBook</span>
      </header>
      
      <!-- Overlay effect when opening sidebar on small screens -->
      <div class="w3-overlay w3-hide-large" onclick="w3_close()" style="cursor:pointer" title="close side menu" id="myOverlay"></div>
      
      <!-- !PAGE CONTENT! -->
      <div class="w3-main" style="margin-left:340px;margin-right:40px">
      
        <!-- Header -->
        <div class="w3-container" style="margin-top:80px" id="showcase">
          
          <h1 class="w3-jumbo"><b>Mais Informações</b></h1>
          
          
          <!-- Contato -->
        <div class="w3-container" id="contact" style="margin-top:75px">
          <h1 class="w3-xxxlarge w3-text-red"><b>Contato.</b></h1>
          <hr style="width:50px;border:5px solid #25142d" class="w3-round">
          <p>Entre em contato conosco a partir das seguintes Informações:</p>
          <form action="/action_page.php" target="_blank">
            <div class="w3-section">
              <label>Nome Completo</label>
              <input class="w3-input w3-border" type="text" name="Name" required>
            </div>
            <div class="w3-section">
              <label>Email</label>
              <input class="w3-input w3-border" type="text" name="Email" required>
            </div>
            <div class="w3-section">
              <label>Mensagem que deseja enviar</label>
              <input class="w3-input w3-border" type="text" name="Message" required>
            </div>
            <button type="submit" class="w3-button w3-block w3-padding-large w3-#25142d w3-margin-bottom">Send Message</button>
          </form>  
        </div>
          
          
          
          
          
          
          
          
          
          
          <h1 class="w3-xxxlarge w3-text-red"><b>Quem somos?</b></h1>
          <hr style="width:50px;border:5px solid #25142d" class="w3-round">
          <p>Apresentamos com entusiasmo a Trendy, a nova rede social revolucionária para todos os amantes de moda! Se você é apaixonado por roupas e adora se expressar através do seu estilo pessoal, chegou a hora de se juntar a uma comunidade vibrante e compartilhar sua paixão pela moda.
      
              Na Trendy, a moda não é apenas sobre tendências passageiras, mas sim sobre a autenticidade e a expressão individual. Aqui, você encontrará um espaço dedicado para explorar, descobrir e se inspirar em diferentes estilos, desde a moda de rua até os looks mais sofisticados. <br><br>
              
              Nosso objetivo é criar uma plataforma inclusiva e acolhedora, onde todos possam se sentir bem-vindos e valorizados. Conecte-se com outros entusiastas da moda, estilistas talentosos e influenciadores que compartilham sua paixão. Compartilhe fotos dos seus looks favoritos, inspire-se com as criações de outros membros e receba feedback valioso para aprimorar seu próprio estilo.<br><br>
              
              Além disso, na Trendy você encontrará recursos exclusivos para simplificar a sua experiência de compras. Descubra marcas renomadas, promoções imperdíveis e até mesmo uma seção dedicada a pequenos negócios e designers independentes. Encontre exatamente o que você procura e faça compras diretamente pela plataforma, tornando a experiência de moda ainda mais acessível e conveniente.<br><br>
              
              Estamos ansiosos para ver você se juntar à nossa comunidade e compartilhar sua paixão pela moda. Juntos, vamos construir uma rede social onde a criatividade, a expressão pessoal e a moda se encontram. Bem-vindo à Trendy, o seu novo destino para descobrir, inspirar e arrasar com seu estilo único!</p>
        </div>
        
      
      
        <!-- Modal for full size images on click-->
        <div id="modal01" class="w3-modal w3-black" style="padding-top:0" onclick="this.style.display='none'">
          <span class="w3-button w3-black w3-xxlarge w3-display-topright">×</span>
          <div class="w3-modal-content w3-animate-zoom w3-center w3-transparent w3-padding-64">
            <img id="img01" class="w3-image">
            <p id="caption"></p>
          </div>
        </div>
      
        <!-- Lojas Afiliadas -->
        <div class="w3-container" id="services" style="margin-top:75px">
          <h1 class="w3-xxxlarge w3-text-red"><b>Lojas Afiliadas.</b></h1>
          <hr style="width:50px;border:5px solid #25142d" class="w3-round">
          <p>Bem-vindo à seção de Lojas Afiliadas da Trendy, onde você encontrará uma ampla variedade de marcas renomadas e designers independentes, todos em um só lugar! Nosso objetivo é facilitar sua experiência de compra, oferecendo uma seleção cuidadosamente curada de lojas que representam os mais recentes estilos e tendências.</p>
          <p>Dê uma olhada nas opções de marcas que temos para você explorar: </p>
      
          <p>FashionHub: Uma loja online que apresenta uma variedade de marcas internacionais, desde moda casual até luxo. Com uma ampla gama de opções, o FashionHub é perfeito para encontrar peças únicas e exclusivas que se encaixam no seu estilo pessoal.</p> 
              
          <p>StreetStyle Store: Se você é fã de moda de rua, a StreetStyle Store é o lugar certo para você. Descubra roupas urbanas, acessórios descolados e calçados modernos que irão complementar perfeitamente o seu estilo urbano.</p> 
              
          <p>Bella Couture: Se você busca roupas elegantes e sofisticadas para ocasiões especiais, a Bella Couture é a loja ideal. Com uma coleção de vestidos de alta costura, ternos e acessórios luxuosos, você certamente encontrará a peça perfeita para brilhar em qualquer evento.</p>  
              
          <p>FreshTees: Para os amantes de camisetas com estampas criativas e descontraídas, a FreshTees é o destino certo. Com designs únicos e materiais de alta qualidade, eles oferecem uma variedade de opções para expressar sua personalidade e estilo.</p> 
              
          <p>Lembre-se de que, ao fazer compras por meio das lojas afiliadas da Trendy, você estará apoiando tanto a comunidade da moda quanto a própria plataforma. Desfrute da conveniência de encontrar suas marcas favoritas em um único lugar e, ao mesmo tempo, ajude a promover a diversidade e a criatividade no mundo da moda.</p>
          
          <p>Explore nossas lojas afiliadas e encontre as peças perfeitas para complementar seu estilo pessoal. A Trendy está aqui para ajudá-lo a expressar sua paixão pela moda e descobrir novas tendências emocionantes. Boas compras!</p>
        </div>
        
        
      
      <!-- End page content -->
      </div>
      
      <script>
      // Script to open and close sidebar
      function w3_open() {
        document.getElementById("mySidebar").style.display = "block";
        document.getElementById("myOverlay").style.display = "block";
      }
       
      function w3_close() {
        document.getElementById("mySidebar").style.display = "none";
        document.getElementById("myOverlay").style.display = "none";
      }
      
      // Modal Image Gallery
      function onClick(element) {
        document.getElementById("img01").src = element.src;
        document.getElementById("modal01").style.display = "block";
        var captionText = document.getElementById("caption");
        captionText.innerHTML = element.alt;
      }
      </script>
      
      </body>
      </html>

// Pagina de Cadastro de Roupas 


      <!DOCTYPE html>
      <html lang="pt-br">
      
      <head>
        <title>Cadastro de roupas</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
        <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Poppins">
        <link rel="shortcut icon" href="img/favicon.ico">
      
        <style>
          body,
          h1,
          h2,
          h3,
          h4,
          h5 {
            font-family: "Poppins", sans-serif
          }
      
          body {
            font-size: 16px;
          }
      
          .w3-half img {
            margin-bottom: -6px;
            margin-top: 16px;
            opacity: 0.8;
            cursor: pointer
          }
      
          .w3-half img:hover {
            opacity: 1
          }
      
          /* Estilo do menu */
          .w3-sidebar {
            background-color: #25142d;
            color: #d42637;
          }
          /* Scrollbar */
      ::-webkit-scrollbar {
          width: 8px;
      }
      
      ::-webkit-scrollbar-thumb {
          background-color: #d42637;
      }
      
      ::-webkit-scrollbar-thumb:hover {
          background-color: #d42637;
      }
      
      ::-webkit-scrollbar-track {
          background-color: #25142d;
      }
        </style>
      </head>
      
      <body>
      
        <!-- Sidebar/menu -->
        <nav class="w3-sidebar w3-collapse w3-top w3-large w3-padding" style="z-index:3;width:300px;font-weight:bold;"
          id="mySidebar"><br>
          <a href="javascript:void(0)" onclick="w3_close()" class="w3-button w3-hide-large w3-display-topleft"
            style="width:100%;font-size:22px">Close Menu</a>
          <div class="w3-container">
            <img src="img/Trendy.jpg" alt="Logo Trendy" style="width: 100%; height: auto;">
      
          </div>
          <div class="w3-bar-block">
            <a href="index.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white"
              style="margin-bottom:40px; padding-left: 50px;">Home</a>
            <a href="indexJ.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white"
              style="margin-bottom:40px; padding-left: 50px;">Perfil</a>
            <a href="indexVM2.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white"
              style="margin-bottom:40px; padding-left: 50px;">Cadastro de Roupas</a>
            <a href="indexVM.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white"
              style="margin-bottom:40px; padding-left: 50px;">Informações</a>
            <a href="login.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white"
              style="margin-bottom:40px; padding-left: 50px;">Login</a>
          </div>
        </nav>
      
      
        <!-- Top menu on small screens -->
        <header class="w3-container w3-top w3-hide-large w3-red w3-xlarge w3-padding">
          <a href="javascript:void(0)" class="w3-button w3-red w3-margin-right" onclick="w3_open()">☰</a>
          <span>Trendy - The LookBook</span>
        </header>
      
        <!-- Overlay effect when opening sidebar on small screens -->
        <div class="w3-overlay w3-hide-large" onclick="w3_close()" style="cursor:pointer" title="close side menu"
          id="myOverlay"></div>
      
        <!-- !PAGE CONTENT! -->
        <div class="w3-main" style="margin-left:340px;margin-right:40px">
      
          <!-- Header -->
          <div class="w3-container" style="margin-top:80px" id="showcase">
      
            <h1 class="w3-jumbo"><b>Cadastra</b></h1>
      
      
            <div id="container">
              <h1 class=tittleCadastro>Cadastro de Roupas</h1>
              <button id="btnAbrirFormulario">Nova Roupa</button>
              <div id="formulario" style="display: none;">
                <h2>Formulário de Cadastro</h2>
                <form id="roupaForm">
                  <label for="imagem">Imagem:</label>
                  <input type="file" id="imagem" name="imagem" accept="image/*" required><br><br>
      
                  <label for="estilo">Estilo:</label><br>
                  <input type="text" id="estilo" name="estilo" required><br><br>
      
                  <label for="peca">Tipo de Peça:</label>
                  <select id="peca" name="peca" required>
                    <option value="calçado">Calçado</option>
                    <option value="shorts">Shorts</option>
                    <option value="blusa">Blusa</option>
                    <option value="vestido">Vestido</option>
                    <option value="outro">Outro</option>
                  </select><br><br>
      
                  <label for="ocasiao">Ocasião de Uso:</label>
                  <input type="text" id="ocasiao" name="ocasiao" required><br><br>
      
                  <input type="submit" value="Cadastrar">
                </form>
              </div>
            </div>
      
      
      
            <!-- Modal for full size images on click-->
            <div id="modal01" class="w3-modal w3-black" style="padding-top:0" onclick="this.style.display='none'">
              <span class="w3-button w3-black w3-xxlarge w3-display-topright">×</span>
              <div class="w3-modal-content w3-animate-zoom w3-center w3-transparent w3-padding-64">
                <img id="img01" class="w3-image">
                <p id="caption"></p>
              </div>
            </div>
      
            <script>
              // Script to open and close sidebar
              function w3_open() {
                document.getElementById("mySidebar").style.display = "block";
                document.getElementById("myOverlay").style.display = "block";
              }
      
              function w3_close() {
                document.getElementById("mySidebar").style.display = "none";
                document.getElementById("myOverlay").style.display = "none";
              }
      
              // Modal Image Gallery
              function onClick(element) {
                document.getElementById("img01").src = element.src;
                document.getElementById("modal01").style.display = "block";
                var captionText = document.getElementById("caption");
                captionText.innerHTML = element.alt;
              }
            </script>
            <script src="script.js"></script>
      
      </body>
      
      </html>

// Pagina de Login
      
      <!DOCTYPE html>
      <html lang="en">
      
      <head>
      	<meta charset="UTF-8">
      	<meta name="viewport" content="width=device-width, initial-scale=1.0">
      	<title>Login/Cadastro</title>
      	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm"
      	 crossorigin="anonymous">
      </head>
      
      <body style="background-color:#25142d ; background-size: cover; background-repeat: no-repeat;height: 500px">
        
      	<div id="login">
      		<div class="container">
      			<div id="login-row" class="row justify-content-center align-items-center">
      				<div id="login-column" class="col-md-6">
      					<div id="login-box" class="col-md-12">
      						<form id="login-form" class="form" method="post" onsubmit="loginUser (this)">
      							<img src="img/logo.png"style="width: 120px; height: 120px; margin=top: 20px; margin-bottom: 10px; margin-left: 35%">
                    <h3 style="text-align: center; color: #d42637; font-family: 'Times New Roman', Times, serif; font-size: 30px; margin-bottom: 30px; margin-top: 30px">Entre na sua conta</h3>
      							<div class="form-group" >
      								<label for="username" style="color:#d42637">Usuário</label><br>
                                      <input type="text" name="username" id="username" class="form-control">
                                  </div>
                                  <div class="form-group">
                                      <label for="password" style="color: #4b001e">Senha</label><br>
                                      <input type="text" name="password" id="password" class="form-control">
                                  </div>
                                  <div class="form-group text-right">                                
                                      <input type="submit" name="submit" style="background-color: #4b001e; color: #ffffff; padding: 10px 20px; border: none; border-radius: 4px; cursor: pointer; margin-bottom: 3px" value="Entrar">
                                  </div>
                              </form>
                          </div>
      
      
                          <button type="button" style="background-color: #4b001e; color: #ffffff; padding: 10px 20px; border: none; border-radius: 5px;cursor: pointer; margin-left: 35%" data-toggle="modal" data-target="#loginModal">Novo Usuário</button>
                      </div>
                  </div>
              </div>
          </div>    
      
        <div class="modal fade" id="loginModal" tabindex="-1" role="dialog" aria-labelledby="loginModalLabel" aria-hidden="true" >
          <div class="modal-dialog" role="document">
            <div class="modal-content" style="background-color: #c0c0c0">
              <div class="modal-header">
                <h5 style="color: #4b001e; font-family: 'Times New Roman', Times, serif; font-size: 30px" id="loginModalLabel">Crie usuário para Login</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                  <span aria-hidden="true">&times;</span>
                </button>
              </div>
              <div class="modal-body">
                  <div id="login-box" class="col-md-12">
                      <form id="login-form" class="form" method="post" onsubmit="loginUser (this)">
                          <h3 style="align-text: center; color #4b001e; font-family: 'Times New Roman', Times, serif; font-size: 25px">Novo usuário</h3>
                          <div class="form-group">
                              <label for="login" style=" color: #4b001e;">Usuário</label><br>
                              <input type="text" name="txt_login" id="txt_login" class="form-control">
                          </div>
                          <div class="form-group">
                              <label for="nome" style=" color: #4b001e;">Nome</label><br>
                              <input type="text" name="txt_nome" id="txt_nome" class="form-control">
                          </div>
                          <div class="form-group">
                              <label for="email" style=" color: #4b001e;">Email</label><br>
                              <input type="text" name="txt_email" id="txt_email" class="form-control">
                          </div>
                          <div class="form-group">
                              <label for="senha" style=" color: #4b001e;">Senha</label><br>
                              <input type="password" name="txt_senha" id="txt_senha" class="form-control">
                          </div>
                          <div class="form-group">
                              <label for="senha2" style=" color: #4b001e;">Confirme sua Senha</label><br>
                              <input type="password" name="txt_senha2" id="txt_senha2" class="form-control">
                          </div>
                      </form>
                  </div>
              </div>
              <div class="modal-footer">
                <button type="button" style="background-color: #151716; color: #ffffff; padding: 10px 20px; border: none; border-radius: 5px;cursor: pointer;" data-dismiss="modal">Cancelar</button>
                <button type="button" id="btn_salvar" style="background-color: #4b001e; color: #ffffff; padding: 10px 20px; border: none; border-radius: 5px;cursor: pointer;">Salvar Informações</button>
              </div>
            </div>
          </div>
        </div>
      
          <script src="loginecadastro.js"></script>
          <script>
              
              
              function processaFormLogin (event) {                
                      
                      event.preventDefault ();
      
                      
                      var username = document.getElementById('username').value;
                      var password = document.getElementById('password').value;
      
                      
                      resultadoLogin = loginUser (username, password);
                      if (resultadoLogin) {
                          window.location.href = 'index.html';
                      }
                      else { 
                          alert ('Usuário ou senha incorretos');
                      }
              }
      
              function salvaLogin (event) {
                  
                  event.preventDefault ();
      
                  
                  let login  = document.getElementById('txt_login').value;
                  let nome   = document.getElementById('txt_nome').value;
                  let email  = document.getElementById('txt_email').value;
                  let senha  = document.getElementById('txt_senha').value;
                  let senha2 = document.getElementById('txt_senha2').value;
                  if (senha != senha2) {
                      alert ('As senhas informadas devem ser iguais!');
                      return
                  }
      
                  
                  addUser (nome, login, senha, email);
                  alert ('Seu usuário agora foi criado, agora proceda com o login para ');
      
                  
                  $('#loginModal').modal('hide');
              }
      
              
              document.getElementById ('login-form').addEventListener ('submit', processaFormLogin);
      
      
              
              document.getElementById ('btn_salvar').addEventListener ('click', salvaLogin);        
          </script>
      
          <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
          <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
          <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>    
      </body>
      </html>

      
      
      





