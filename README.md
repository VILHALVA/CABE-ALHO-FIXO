# CABEÇALHO FIXO
☑️Um cabeçalho fixo é útil para manter o cabeçalho visível na parte superior da página enquanto o usuário rola o conteúdo.

[![GitHub Repo stars](https://img.shields.io/badge/VILHALVA-GITHUB-03A9F4?logo=github)](https://github.com/VILHALVA)
[![GitHub Repo stars](https://img.shields.io/badge/MEUS-CURSOS-03A9F4?logo=github)](https://github.com/VILHALVA?tab=repositories&q=CURSO&type=public&language=&sort=) <br>

<img src="https://4.bp.blogspot.com/-OBKyVVpLzmI/TrJ87Q5iLcI/AAAAAAAAGN8/zCbypNALX-A/s1600/power.png" align="center" width="280"> <br>

## Pré-requisitos
- Um editor de código (como Visual Studio Code, Sublime Text, etc.).
- Conhecimento básico de HTML, CSS e JavaScript.

## Passos
1. **Estrutura HTML**

   Comece com uma estrutura HTML básica que inclui um cabeçalho, o conteúdo da página e os links de navegação. O cabeçalho deve ter uma classe que usaremos para aplicar estilos CSS.

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <link rel="stylesheet" href="styles.css">
       <title>Header Fixo</title>
   </head>
   <body>
       <header class="header">
           <nav>
               <ul>
                   <li><a href="#">Página Inicial</a></li>
                   <li><a href="#">Sobre</a></li>
                   <li><a href="#">Contato</a></li>
               </ul>
           </nav>
       </header>
       <div id="content">
           <!-- Conteúdo da página aqui -->
       </div>
   </body>
   </html>
   ```

2. **Estilos CSS**

   Crie um arquivo CSS (por exemplo, `styles.css`) para estilizar o cabeçalho e adicionar um espaço de margem superior ao conteúdo para evitar sobreposição.

   ```css
   /* Estilo do cabeçalho */
   .header {
       position: fixed;
       top: 0;
       left: 0;
       width: 100%;
       background-color: #333;
       color: #fff;
       padding: 10px 0;
   }

   /* Estilo da navegação no cabeçalho */
   .header nav {
       text-align: center;
   }

   .header ul {
       list-style: none;
       margin: 0;
       padding: 0;
   }

   .header li {
       display: inline;
       margin-right: 20px;
   }

   .header a {
       text-decoration: none;
       color: #fff;
   }

   /* Adicione estilos de margem superior ao conteúdo */
   body {
       margin-top: 60px; /* Ajuste conforme necessário para a altura do cabeçalho */
   }
   ```

3. **JavaScript (Opcional)**

   Você pode adicionar JavaScript para criar um efeito de rolagem suave ao clicar nos links de navegação. Isso é opcional, mas pode melhorar a experiência do usuário.

   ```javascript
   document.querySelectorAll('a').forEach(anchor => {
       anchor.addEventListener('click', function(e) {
           e.preventDefault();

           const targetId = this.getAttribute('href').substring(1);
           const targetElement = document.getElementById(targetId);

           if (targetElement) {
               window.scrollTo({
                   top: targetElement.offsetTop - 60, // Ajuste para a altura do cabeçalho
                   behavior: 'smooth'
               });
           }
       });
   });
   ```

4. **Personalize conforme necessário**

   Personalize o HTML, CSS e JavaScript de acordo com as necessidades do seu site e os estilos específicos do seu cabeçalho.

## Testando
Após seguir os passos acima, você pode criar uma página HTML com um cabeçalho fixo e conteúdo longo para testar o cabeçalho fixo enquanto rola a página.

Isso é um guia básico para criar um cabeçalho fixo em uma página HTML. Você pode adicionar mais elementos e estilos conforme necessário para atender aos requisitos do seu projeto.