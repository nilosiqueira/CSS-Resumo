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

Unidade         Nome                        Equivalência
cm                  Centímentros            1cm = 96px/2.54
in                     Inches (polegadas)   1in = 2.54cm = 96px
px                    Pixels                       1px = 1/96th of 1in

# Distânciaas realtivas 

São relativas a algum outro valor, pode ser o elemento pai, ou root,
ou o tamanho de tela.

* Benefício: Maior adaptação aos diferentes tipos de tela

Unidade             Realtivo a
em                      Tamanho da font do pai.
rem                     Tamanho da font do elemento raiz (root/html)
vw                       1% da viewport width.
vh                        1% da viewport height.