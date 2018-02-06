# Tools to Style for front-end

**Tools to Style** é um conjunto de estilos css para acelerar o desenvolvimento front-end de sites. 
Ele foi feito utilizando o pré-procesador Sass que permite ter automatizar e modificar os estilos de acordo com a necessidade do projeto.
O **Tools to Style** procura deixar o HTML mais limpo possivel, usando os include e mixins do SASS permitindo com seu CSS seja facilmente customizado.

##Usando o Settings.sass
Se você quer deixar seu estilo css totalmente customizado, recomendamos o uso de um arquivo de configuração, nele você pode criar variaveis que armazenam as informações do seu estilo como por exemplo nome da fonte que vai usada, a paleta de cores, tamanho da fonte, espaçamento de caraceres e inumeras outras configurações. A ideia por traz desse arquivo de configuração é que se você ter todo as propriedades do seu estilo em arquivo configuração, sua manutenção será bem mais facil, pois em vez de ter que ficar procurando no arquivo sass ou css todos os lugares onde você utilizou uma determinada propriedade, que precisa alterar, você simplesmente vai no settings.sass e procura a variavel que contém a propriedade e a modifica, assim quando vc recompilar os arquivos sass o seu estilo será automaticamente alterado

Veja um modelo de configuração que você pode usar:
``` scss
/* settings.scss */
/* se você for usar a extensão .sass remova os ; no final dos das variaveis abaixo. */

/* Font style */
$font-size-default: 14px;

/* Palette Colors */
$white: #fff;
$black: #000;
$gray: #999;


```

##Começando a usar o Tools for Style
Para começar a usar é necessário primeiramente importar o settings.sass no seu arquivo de estilo principal, que aqui para iremos chamar de main.sass.

*Note: O arquivo settings.sass contém a configuração do seu estilo(typografia, paleta de cores, alinhamentos entre outras configurações)*

##Alinhamento de Textos
```scss
//Style in SASS
@import ../settings/settings

//Configurando o tamanho da fonte
@mixin font-size($size)
  font-size: $size

//Configurando a cor da fonte
@mixin font-color($color)
  color: $color

//Configurando a fonte que será usado (o nome da fonte)
@mixin font-family($font-name)
  font-family: $font-name

//Configurando o espaçamento entre as linhas
@mixin line-height($line-height)
  line-height: $line-height

//Configurando o espaçamento entre as letras
@mixin letter-spacing($letter-spacing)
  letter-spacing: $letter-spacing

//Configurando a intensidade da fonte
@mixin font-weight($font-weight)
  font-weight: $font-weight

//Transformações para os texto (UpperCase, lowerCase,
@mixin text-transform($text-transform)
  text-transform: $text-transform

//Configurando o Estilo do Texto (normal, italic, oblique)
@mixin font-style($style)
  font-style: $style

//Configurando as variações da Fonte (normal, small-caps)
@mixin font-variant($variant)
    font-variant: $variant
```
