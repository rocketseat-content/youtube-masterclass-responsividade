# Responsividade 

Fala Dev! 💜

Responsividade é um assunto muito importante para que nosso layout seja flexível, conforme o dispositivo que o está acessando, seja ele smartphone, tablet ou desktop. (E até mesmo, a impressora sabia?)

Na Masterclass de hoje, vamos usar estratégias de CSS Units para que tanto o nosso Layout, quanto os nossos textos, fiquem fluidos. 

Utilizaremos também CSS Media Queries para adicionar CSS customizados conforme o breakpoint definido, para que nosso layout fique adaptado ao viewport do dispositivo. 

Além do mais, veremos atributos e tags HTML especiais, para que possamos obter sucesso ao tornar nosso layout responsivo.

Se você ainda não sabe muito bem como fazer layouts responsivos, está começando nesse assunto, está um pouco inseguro, fique tranquilo, vem comigo que eu vou tirar suas dúvidas!

Espero que faça sentido pra você. 🥰

Bora codar? 🚀 

## CSS Units

Unidades de medidas do CSS

Layout Fixo
`px` - Pixels

Layout Fluido
`%` - Porcentagem
`auto` - Automática
`vh` - Viewport Height
`vw` - Viewport Width

Textos fixos
`1px` = 0.75pt
`16px` = 12pt

Texto fluidos
`em` - multiplicado pelo pai 
`rem` - multiplicado pelo root

## CSS Media Queries 

No HTMl eu coloco a seguinte tag meta

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

No CSS eu uso da seguinte forma

```css
@media (max-width: 320px) {
  #form h3 {
    font-size: 2rem;
  }
}
```

## HTML Media Attrib.

Posso utilizar o atribuito `media` no link do meu HTML, ao importar um arquivo css, usando as propriedades da mesma forma que usaria na regra `@media` do css.

```html
<link 
    rel="stylesheet"
    href="responsive.css" 
    media="screen and (max-width: 768px)"
/>

<link rel="stylesheet" href="print.css" media="print">
```

## Imagens

Usamos a tag `<picture>` para que as imagens sejam responsivas.

```html
<picture class="image" alt="Imagem">
    <source media="(min-width: 768px)" 
        srcset="https://i.ytimg.com/vi/GykTLqODQuU/maxresdefault.jpg">
    <source media="(min-width: 320px)" 
        srcset="https://i.ytimg.com/vi/GykTLqODQuU/hqdefault.jpg">
    <source media="(min-width: 10px)" 
        srcset="https://i.ytimg.com/vi/GykTLqODQuU/mqdefault.jpg">

    <img 
        src="https://i.ytimg.com/vi/GykTLqODQuU/hqdefault.jpg" 
        alt="Imagem" />
</picture>
```

Sempre que possível, usar SVG ao invés de JPG, PNG
