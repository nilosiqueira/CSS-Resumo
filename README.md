# CSS-Resumo
Resumo de CSS Cascading Style Sheets

# Introdução
## O que significar CSS ?

* Cascading Style Sheet
* Código para criar estilos no HTML
* HTML é a estrutura, e o CSS é a beleza
* Não é uma linguagem de programação;
* É uma linguagem style sheet


# Comentários 
 
 * Não irá afetar o seu código
 * Ajuda a lembrar blocos de códigos
 * Deix dicas para leitura
 * Ajuda outros a entenderem
 * Nunca esqueça de fechar um comentário aberto 
 * Você poderá usar para desabilitar partes do seu código

# Anatomia

```css
h1 {
    color: blue;
    font-size: 60px;
    background: gray;
}
```

* Selector
* Declaration
* Properties
* Property Value

# Selectors 

Conecta um elemento HTML com  o CSS

## Tipos 

* Clobal selector `*`
* Element/Type selector `h1, h2, p, div`
* ID Selector `#box, #container`
* Class Selector `.red, .m-4`
*Attribute selector, Pseudo-class, Pseudo-element, e outros

# Caixas (Box Model)

* Você irá perceber que (quase) tudo são caixas do CSS 
* Posicionamentos, tamanhos, espaçamentos, bordas, cores
* Caixa pode ficar ao lado uma da outra, ou acima
* Elementos HTML são caixas

# Valores e unidade de medida

* cada propriedade possui valores `property: valeu`
* estudo constante a fim de entender as propriedades e seus valores

## Prática

* como conhecer e estudadar os valores na documentação
       `  * <color> <length>`
* os termos poder variar. `values` ou `data types`

# Distâncias absolutas <length>

São fixas e não alteram seu valor.
```
Unidade         Nome                        Equivalência
cm              Centímentros                1cm = 96px/2.54
in              Inches (polegadas)          1in = 2.54cm = 96px
px              Pixels                      1px = 1/96th of 1in
```

# Distânciaas realtivas 

São relativas a algum outro valor, pode ser o elemento pai, ou root,
ou o tamanho de tela.

* Benefício: Maior adaptação aos diferentes tipos de tela
```
Unidade             Realtivo a
em                  Tamanho da font do pai.
rem                 Tamanho da font do elemento raiz (root/html)
vw                  1% da viewport width.
vh                  1% da viewport height.
```
# Porcentagens %

* Em muitos casos é tratado da mesma maneira que as distâncias <lenghet>
* Sempre será relativo a algum valor
 
 exemplo: 
 tenho um elemento body e um div e uma lista li dentro deste 
 elemento todos vão ajustar ao elemento pai 

 # Posições 
 <position>

Representa um conjunto de coordenadas 2D:
- top, right, bottom, left e center

* Usado para alguns tipos de propriedades
* Não confundir com a propriedade `position`

exemplo: 

```HTML
<div class="box"></div>
```
```CSS
.box {
  height: 300px;
  width: 400px;
  background-image: 
  url(http://source.unsplash.com/random);
  background-repeat: no-repeat;
  background-position: bottom right;
}
``` 
# Funções 

Em programação, função são reconhecidas por causar um reaproveitamento de código. 

* rgb()
* hsl()
* url()
* calc()

```html
<div class="box"></div>
```
```CSS
body {
    height: 100vh;
    margin: 0;
}
.box {
  height: calc(100% - 40px);
  width: 100px;
  background-image: 
  url(http://source.unsplash.com/random);
  background-repeat: no-repeat;
  background-position: bottom right;
}
```

# Strings e identificadores

* Strings: Texto envolto em aspas
* Identificadores: red, back, gold;

usando um piseudo elemento chamado after

```css
.box::after {
    content: "Aqui vem alguma mensagem";
    color: white;
}
```

# Box Model

- Fundamental para fazer layouts para a web
- Maior facilidade para aplicar o CSS

## O que é ?

Uma caixa retangular. 
Essa Caixa possui propriedades de uma caixa (2D)
```
- Tamanho (largura x altura)        width | height
- Conteúdo                                 content
- Bordas                                      border
- Preenchimento interno                padding
- Espaços fora da caixa                margin
```
* Cada elemnto na sua página , será considerado uma caixa. *

## box-sizing

Como será calculado o tamanho total da caixa?

- content-box | border-box

```css
div {
    width: 100px;
    height: 100px;
    border: 1px solid red;
    margin: 10%;
    padding: 0 20px;
    box-sizing: border-box;
}
```

## display: block vs display: inline

- Como as caixas se comportam em relação às outras caixas 
- Comportamento externo das caixas

|   ** block**                           | ** inline**                        |
|----------------------------------------|------------------------------------|
| Ocupa toda a linha, colocando o        | Elemento ao lado do outro          |
| próximo elemento abaixo desse          |                                    |
|----------------------------------------|------------------------------------|
| width e height são respeitados         | width e height não funcionam       |
|----------------------------------------|------------------------------------|
| padding, margin, border  irão          | somente valores horizontais de     |
| funcionar normalmente.                 | margin, padding e border.          |
|                                        |                                    |

exemplos 
bock: `<p> <div> <section>`, todos os headings ` <h1><h2>`... 
inline: `<a> <strong> <span> <em>`

## margin 

Espaços entre os elementos 

- margin-top | margin-right | margin-bottom | margin-left
- values: `<length>` | `<percentage>` | auto

```css
div {
      margin: 12px 16px 10px 4px;
      margin: 12px 16px 0;
      margin: 8px 16px;
      margin: 8px;
}
```

  * Cuidado com margin collapsing (top se ajusta ao bottom)

## padding

Espaços entre os elementos 

- padding-top | padding-right | padding-bottom | padding-left
- values: `<length>` | `<percentage>` | auto

```css
div {
      padding: 12px 16px 10px 4px;
      padding: 12px 16px 0;
      padding: 8px 16px;
      padding: 8px;
}
```

  * Padding poderá causar diferença na largura de um elemento.

## border (e outline )

As bordas da caixa

- value: `<border-style>` | `<border-width>` | `<border-color>` 

      - style:    solid | dotted    |   dashed | double  |   groove | ridge     | inset | outset
      - width: `<length>`
      - color: `<color>`

 ```CSS
 div {
   /*shorthand*/ 
      border-top: solid 2px; /* top | right  | bottom |  left * /

      /* style */
      border: solid;

      /* width <lengtt> | style */
      border: 2px dotted;

      /* style | color */
      border: outset #f33;

      /* width | style | color */
      border: medium dashed green;
 }
 ```

 ##  E outline?

 - difere em 4 sentidos: 
        - Não modifica o tamanho da caixa, pois não é parte do box model
        - Poderá ser difrente de retangular
        - Não permite ajuste individuais
        - Mais usado pelo user agent para acessibilidade


Veja mais informações [MDN border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)


# Tipos de combinadores

1. Seletor de descendente
2. Seletor filho (>)
3. Seletor de irmão adjacente (+)
4. Seletor geral de irmãos (~)

## Seletor de descendente

O seletor descendente corresponte a todos os elementos descendentes de um elemento especificado.

Exemplo a seguir seleciona todos os elementos `<p>`
dentro dos elementos  `<div>`

```css
div p {
  background-color: yellow;
}
```

## Seletor filho (>)

O seletor filho seleciona todos os elementos que são filhos de um elemento especificado.

O exemplo a seguir seleciona todos os elementos `<p>` que são filhos de um elemento `<div>`

```css
div > p {
    background-color: yellow;
}
```

## Seletor de irmão adjacente (+)

O seletor irmão adjacente é usado para selecionar um elemento que está diretamente após outro elemento específico.

O exemplo a seguir seleciona o primeiro elemento `<p>` que é colocado imediatamente após 
os elementos `<div>`

```css
div + p {
    background-color: yellow;
}
```
### Exemplo (irmão djacente +)

```css
div + p {
  background-color: yellow;
}
```
```html
<div>
    <p>PARÁRGRAFO 1 NA DIV.</p>
    <p>PARÁRGRAFO 2 NA DIV.</p>
</div>
      <p>PARÁRGRAFO 3.</p>
      <p>PARÁRGRAFO 4.</p>
```

```html
RESULTADO

PARÁGRAFO 1 NA DIV.
PARÁGRAFO 2 NA DIV.
**PARÁGRAFO 3 .**
PARÁGRAFO 4.
```

O exemplo a seguir seleciona todos os elementos `<p>`
são irmãos próximos dos elementos `<div>`

```css
div ~ p {
    background-color: yellow;
}
```

### Exemplo (geral de irmãos ~)

```css
div ~ p {
  background-color: yellow;
}
```
```html
<p>Algum parágrafo qualquer</p>
<p>Parágrafo 1.</p>

<div>
    <p>Parágrafo 2 na div.
</div>
<p>Parágrafo 3.</p>
<p>Parágrafo 4.</p>
```
```html
Algum parágrafo qualquer 
Parágrafo 1.
Parágrafo 2 na div.
**Parágrafo 3.**
**Parágrafo 4.**
```

# Cores 

Usamos CSS para alterar cores do nosso documento.

## Tipos 
* background-color (para caixas)
* Color (para textos)
* border-color (para-caixas)
* outros...

## Valores

Podemos definir os valores por 

* palavra-chave (blue, transparent)
* hexadecimal (#009900aa)
* funções: rgb, rgba, hsl, hsla

```css
element {
  /* keyword values */
    color: currentcolor;

    /* <named-color> values */
    color: red;
    color: orange;
    color: tan;
    color: rebeccapurple;

    /* <hex-color> values 0-F */
    color: #090; /* RED GREEN BLUE*/
    color: #009900;
    color: #090a;
    color: #009900aa;

    /* <rgb()> values */
    color: rgb(34, 12, 64, 0.6); /* 0-255 */
    color: rgba(34, 12, 64, 0.6);
    color: rgb(34 12 64 / 0.6);
    color: rgb( 34.0 12 64 / 60%);
    color: rgba(34.6 12 64 / 30%);

    /* <hsl()> values */
    color: hsl(30, 100%, 50%, 0.6); /* Hue - Saturation - Lumiance */
    color: hsla(30, 100%, 50%, 0.6);
    color: hsl(30 100% 50% / 0.6);
    color: hsla(30 100% 50% / 0.6);
    color: hsl(30.0 100% 50% / 60%);
    color: hsla(30.2 100% 50% / 60%);

    /* Global values */
    color: inherit;
    color: initial;
    color: unset;
}
```
## Referência

Veja mais informações [MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/color_value)