# README - Classes e IDs em HTML e CSS

## Introdução
Este documento explica o uso de classes e IDs em HTML e CSS, utilizando como base o exemplo de código fornecido.

## Estrutura do Código HTML
O código HTML apresentado contém elementos como `<h1>` e `<p>`, sendo estilizados por seletores CSS.

### Exemplo de Estrutura:
```html
<h1>Estilo Css (Cascading Style Sheet)</h1>
<p>
    Em linguística, a noção de texto é ampla e ainda aberta a uma definição mais precisa.
</p>
<p class="azul">
    Este parágrafo possui uma classe chamada "azul".
</p>
```

## Estilização com CSS
No CSS, foram usados seletores para estilizar os elementos:

```css
p {
    color: red;
}

h1 {
    color: blue;
}

.azul {
    color: blue;
}
```

### Explicação dos Seletores
1. `p { color: red; }` - Todos os parágrafos (`<p>`) terão a cor vermelha.
2. `h1 { color: blue; }` - Todos os títulos `<h1>` terão a cor azul.
3. `.azul { color: blue; }` - Qualquer elemento com a classe `azul` terá a cor azul, sobrescrevendo a cor padrão do seletor `p`.

## Diferença entre Classes e IDs
- **Classe (`class`)**: Pode ser usada em múltiplos elementos e permite a reutilização de estilos.
- **ID (`id`)**: Deve ser único dentro da página e normalmente é usado para elementos específicos.

Exemplo de um ID (não presente no código fornecido):
```html
<p id="unico">Este parágrafo tem um ID único.</p>
```
```css
#unico {
    font-weight: bold;
}
```

## Conclusão
Neste exemplo, vimos como as classes podem ser utilizadas para aplicar estilos específicos sem alterar todos os elementos do mesmo tipo. O uso adequado de classes e IDs é essencial para uma boa prática de estilização com CSS.

# Estilos em Linha (Inline Styles) no HTML  

No seu código, você utilizou **estilos em linha** para definir a cor do texto nos parágrafos (`<p>`).  

## O que é um estilo em linha?  
O **estilo em linha** (ou **inline style**) é uma forma de aplicar CSS diretamente dentro da tag do elemento, usando o atributo `style`.  

## Como funciona no seu código?  
```html
<p style="color: red;">
```
Aqui, o `style="color: red;"` define que o texto do parágrafo (`<p>`) terá a cor vermelha.  

Isso significa que **somente esse parágrafo** receberá essa cor, pois o estilo foi aplicado diretamente a ele.  

## Desvantagens do estilo em linha  
- **Dificulta a manutenção** – Se quiser mudar a cor do texto de vários elementos, precisará modificar um por um.  
- **Não reaproveita código** – Diferente de um arquivo CSS externo ou de um `<style>` no `<head>`, o estilo em linha precisa ser repetido em cada elemento.  
- **Menor organização** – Para projetos maiores, misturar HTML com estilos torna o código menos limpo.  

## Alternativa melhor: CSS interno ou externo  
Se quiser aplicar a mesma cor para todos os `<p>`, uma opção melhor seria usar CSS interno:  

```html
<head>
    <style>
        p {
            color: red;
        }
    </style>
</head>
```
Ou CSS externo (em um arquivo separado, como `style.css`):  

```css
p {
    color: red;
}
```
E no HTML, referenciar esse arquivo externo:  

```html
<link rel="stylesheet" href="style.css">
```
Isso torna o código mais **limpo** e **fácil de modificar** depois.  
 

# Estilos Internos (Internal Styles) no HTML  

No seu código, você utilizou **estilos internos** para definir a cor do texto nos parágrafos (`<p>`) e títulos (`<h1>`).  

## O que é um estilo interno?  
O **estilo interno** (ou **internal style**) é uma forma de aplicar CSS dentro do próprio documento HTML, dentro da tag `<style>` no `<head>`.  

## Como funciona no seu código?  
```html
<style type="text/css">
    p {
        color: red;
    }
    h1 {
        color: blue;
    }
</style>
```
Aqui, você definiu que:
- Todos os elementos `<p>` terão a cor vermelha (`color: red;`).
- Todos os elementos `<h1>` terão a cor azul (`color: blue;`).  

## Vantagens do estilo interno  
- **Mais organizado que o estilo em linha** – Permite definir regras para vários elementos sem precisar repetir `style` em cada um.  
- **Fácil de modificar** – Basta alterar as regras dentro da tag `<style>`.  
- **Bom para projetos pequenos** – Para projetos simples ou páginas individuais, o CSS interno é uma boa opção.  

## Desvantagens do estilo interno  
- **Menos reutilizável** – Não pode ser usado em múltiplas páginas sem copiar o código.  
- **Menos eficiente que CSS externo** – Para projetos grandes, é melhor usar um arquivo CSS separado.  

## Alternativa melhor: CSS externo  
Para melhor organização e reutilização, você pode usar CSS externo. Basta criar um arquivo `style.css` e colocar:  

```css
p {
    color: red;
}
h1 {
    color: blue;
}
```
E no HTML, referenciar esse arquivo externo:  

```html
<link rel="stylesheet" href="style.css">
```
Isso torna o código mais **limpo**, **modular** e **reutilizável**.  
  
