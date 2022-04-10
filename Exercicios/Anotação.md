# HTML5 & CSS3



* Html 
  * Linguagem focada em **Conteúdo**
* Css
  * Linguagem focada em **Design**
* Java Script
  * Linguagem focada em **Interação**

## Estrutura Básica da HTML

```
<!DOCTYPE html>
<html lang="pt-br"
	<head>
		<meta charset="UTF-8">
		<meta name="viewport"
		content="width=device-width, 
		initial-scale=1.0"
		<title>Document</title>
	</head>
	<body>
		<h1>Olá, Mundo!</h1>

	</body>
</html>
```



## Conteúdo em HTML



<h1> Exemplo de titulo </h1>



<p> Exemplo de Parágrafo</p>



<img src="foto.png" alt="Exemplo de Foto">



<hr> Linha Horizontal


&lt;Kaio&gt;



<address> Usado para Endereços</address>



target="_self" <!--Abrir páginas na msm aba -->

### Formatação de Texto

#### Negrito / Destaque



<b>Negrito</b> 

<strong>Termo em destaque</strong>



#### Itálico / Ênfase



<i>Ctrl + Shift + P -> Wrap Abbreviation -> i</i> 	(Sem Semântica)

<em>Ctrl + Shift + P -> Wrap Abbreviation -> i</em> 	(Com Semântica)



#### Texto Marcado



<mark>Marcação</mark>



#### Texto Grande e Pequeno



<big>texto grande</big>

<small>texto pequeno</small>



####  Texto Deletado



<del>um texto como excluido</del>



 #### Texto Inserido



<ins>um texto como inserido</ins> 

<u>sublinhado</u>



#### Texto Sobrescrito



x<sup>20</sup> + 3



#### Texto Subscrito



H<sub>2</sub>O

### Outras Formatações



#### Código Fonte pré-formatado



<code>getElementById('teste')</code><!--Fonte monoespaçada-->

<pre>
        <code>
    num = int(input("Digite um número"))
    if num % 2 == 0;
        print(f' O número {num} é par')
    else
    print('Fim de programa')
        </code>
    </pre>
<!--Indentação de Código-->

#### Citações Simples



<q>o computador é um burro muito rápido</q>



#### Citações Completas



   <blockquote cite="link"> A diferenças entre elementos inline e um bloco de texto é importante, Os elementos html, neste capitulo descrevem os blocos de texto</blockquote>



#### Abreviações



Estou estudando <abbr title="HyperText Markup Lnaguage">html</abbr> e <abbr title="Cascading Style Sheets">css</abbr>



#### Texto Invertido



<bdo dir="rtl">Estou aprendendo a criar coisas em html.</bdo>



### Trabalhando com Listas



#### Listas Ordenadas



<ol type="1" start="1"> <li>Acordar</li><li>Ligar para o joao</li><li>Tomar café</li><li>Escovar os Dentes</li><li>Ir para a faculdade</li> </ol>

<!--1, A, a, I, i-->

​    

#### Listas não Ordenadas



<ul type="square"><li>Acordar</li><li>Ligar para o joao</li><li>Tomar café</li>  <li>Escovar os Dentes</li><li>Ir para a faculdade</li>  </ul>

<!--disc, circle e square-->

#### Lista de Definições



```
<dt>HTML</dt> <!--Termo--> 

<dd>Linguagem de marcação para a criação de um conteúdo para um site.</dd> <!--Definição-->

```

### Trabalhando com Downloads



<li><a href="/Exercicios/ex-010/livro/guia-markdown.pdf" download="guia-markdown.pdf" type="application/pdf">Baixar livro em PDF</a></li>

<li><a href="/Exercicios/ex-010/livro/guia-markdown.pdf" download="guia-markdown.zip" type="application/zip">Livro compactado em zip</a></li>



### Trabalhando com Imagens, Áudios e Vídeos

#### Imagens Dinâmica


```  
<picture>

  <source media="(max-width: 750px)"     	   		   srcset="imagens/foto-p.png" type="image/png">

  <source media="(max-width: 1050px)" 				   srcset="imagens/foto-m.png" type="image/png">

  <img src="imagens/foto-g.png" alt="Imagem       	   flexivel">

  </picture>
```

<!--Tem que seguir uma ordem do maior para o menor ou do menor para o maior-->

<!--Nessen Exemplo carrega primeiro a imagem Grande, caso o tamanho máximo for 1050 pixel carrega tamanho médio e assim sucessivamente-->



#### Reproduzindo Áudio

 <!--Um pouco mais limitada-->

<audio src="midia/North-Oakland.mp3" autoplay controls></audio>
    <!--MP3 WAV OGG -->



<!--Recomendado -->

<audio preload="metadata" autoplay controls loop>
        <source src="midia/North-Oakland.mp3" type="audio/mpeg">
        <source src="midia/North-Oakland.ogg" type="audio/ogg">
        <source src="midia/North-Oakland.wav" type="audio/wav">
        <p>Infelizmente seu navegador não consegue reproduzir áudio. <a href="midia/North-Oakland.mp3">Clique aqui para baixar o arquivo mp3</a></p>
    </audio>  

<!--Preoload = Auto, Metadada, none-->

<!--WAV pesadissimo-->



#### Inserindo vídeos hospedados localmente



<video src="midia/meu-video.ogv" width="500" controls></video>



<!--Melhor recomendação -->

<video width="500" height="500"
    poster="#" controls>
        <source src="midia/meu-video.m4v" type="video/m4v">
        <source src="midia/meu-video.webm" type="video/webm">
        <source src="midia/meu-video.ogv" type="video/ogv">
        <source src="midia/meu-video.mp4" type="video/mp4">
        <p>Seu navegador não tem compatibilidade com reprodução de videos.</p>
    </video>



<!--Poster =  Capa do video-->



#### Inserindo vídeos hospedados externamente

##### Youtube

<iframe width="560" height="315" src="https://www.youtube.com/embed/eF9Qoc6p_4Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



##### Vimeo

 <iframe src="https://player.vimeo.com/video/197093965?h=7fbc516b5a&color=ff9933&portrait=0" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>




## Estrutura Básica da CSS


```
h1{ Seletor
		
	|declaração
	|------------------
​	font-family: Arial;
	font-size: 20 pt;
	-----  ----
	|color: |blue; -> Valor
	|Propriedade
}
```

### Estilos em Linha



<p>São estilos dentro de cada semântica do html</p>

<!--Evitar usar ao máximo-->

<!--Primeiro na ordem de utilização-->



### Estilos Internos



<p>São estilos que ficam fora do corpo do html e dentro da cabeça</p>

<!--Segundo na ordem de utilização-->

### Estilos Externos



<p>São estilos que ficam fora do arquivo html chamado style.css</p>

<!--Terceiro na ordem de utilização-->

### Cores

---------------

### Fontes

#### Sintaxe

<!--Fontes com mais de 1 nome se usa aspas-->

```
font-family: 'Times New Roman';
font-size: 1em;<!--Tamanho-->
font-weight: normal;
font-style: italic;
text-decoration: underline; <!--Sublinhado-->

Lighter(leve), Normal, Bold(negrito), Bolder(ousado) 

Weight(Peso), Width(Largura), Height(Altura)
```



#### Uso de Fontes Internas

<!--DaFont-->

```
@font-face {
font-family:'Love';
src: url('fonts/love story.ttf') format(opentype);
font-weight: normal;
font-style: normal;
}

/*
Tipos de format();
-opentype(otf)
-truetype(ttf)
-embedded-opentype
-truetype-aat(Apple Advanced Typography)
- svg
*/


h1{
font-family: 'Love', Times, serif;
font-size: 3em;
font-weight: normal;
}
```



#### Uso de Fontes Externas

<!--Google fonts-->

```
@import url('https://fonts.googleapis.com/css2?family=Kaushan+Script&display=swap');

h1 {

​font-family: 'Kaushan Script',sans-serif;

​font-size: 3em;

​ }
```

#### Medidas

##### Medidas Absolutas

<ul>
    <li>cm</li>
    <li>mm</li>
    <li>in(polegadas)</li>
    <li>px</li>
    <li>pt</li>
    <li>pc</li>
</ul>


##### Medidas Relativas



<ul>
    <li>em</li>
    <li>ex</li>
    <li>rem</li>
    <li>vw</li>
    <li>vh</li>
    <li>%</li>
</ul>


<!--Recomendação é utilizar 'px' e 'em'-->

#### Shorthand Font



```
font-family:'Work Sans', sans-serif;
font-weight: bolder;
font-size: 3em;
font-style: italic;
```

<!--font-style -> font-weight -> font-size -> font-family-->

```
font: italic bolder 3em 'Work Sans', Sans-serif;
```

#### Alinhamento

<!--Center, Justify, left e right-->

```
text-align: Center;
text-indent: 30px;<!--Distanciamento do paragrafo-->
```

### Seletores Personalizados

```
# = id
. = classe
> = children (filho) 
: = pseudo-class
:: = pseudo-element
```

#### ID (#)

h1*#principal*{

  text-align:center;

}

ou

#principal{ <!--Menos usual-->

​	 text-align:center;

}

#### Class (.)

*.especial*{

​     background-color:rgb(255, 110, 110) 

 }

ou

a.especial{ <!--Menos usual-->

​	background-color:rgb(255, 110, 110) 

}



#### Pseudo-Class (:) 

<!--Seletores que especifica um estado especial do elemento-->



a*:visited*{  <!--Depois do clique-->

​	color: darkred; 

}

a*:hover*{ <!--Movimentação do mouse-->

​     text-decoration:underline;

​    color: black;

 }

a*:active*{<!--Quando clicar-->

​	color: yellow;

 }

#### Pseudo-Element (::)

<!--Seletor que permite que você estilize uma parte especifica do elemento-->



 a*::after*{ <!--Depois do elemento-->

​      content: '[Link]';

​      text-decoration:none;

​     font-weight:normal;

​     color: darkgray; 

​    }

#### Children (>)

 div > p{ <!--Paragrafo que esta dentro da Div-->

​      display: none;

​    }

div*:**hover* > p{

​      display: block; 

​      color:white;

​      background-color:red;

​      width:300px;

}

### Modelos de caixas 


## Símbolos



 &reg;

  &copy;

  &trade;

  &euro;

  &pound;

  &cent;

  &Delta;



## Emoji



 &#x1F596;

 &#x1F913;



## Teclas de Atalho



Shift + Tab 	<!-- Volta com o código -->

Ctrl + Shift + P 	<!-- Envelopamento -->









