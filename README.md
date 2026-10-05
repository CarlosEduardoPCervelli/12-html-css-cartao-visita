# Cartão de Visita Digital

Página simples de perfil pessoal: foto, nome, cargo/área, bio curta e links
de redes sociais.

## Prática de variáveis CSS

Todas as cores e o espaçamento-base ficam centralizados em `:root`:

```css
:root {
  --cor-principal: #6246ea;
  --cor-texto: #2b2c34;
  --cor-texto-claro: #6b7280;
  --cor-fundo: #fffffe;
  --espacamento: 16px;
}
```

Isso significa que pra trocar a cor principal do cartão inteiro (borda da
foto, cargo, bordas dos links, hover), basta mudar o valor de
`--cor-principal` uma vez. O espaçamento interno também usa a variável
`--espacamento`, inclusive combinada com `calc()`.

## Hover nos links

Os links de redes sociais começam como "contorno" (`border`) e, no hover,
preenchem com a cor principal:

```css
.links a:hover {
  background-color: var(--cor-principal);
  color: #fff;
}
```

A transição (`transition: background-color 0.2s ease, color 0.2s ease`)
deixa a troca de cor suave em vez de instantânea.

## Como personalizar

- Troque `src` da `<img>` por uma foto real (ou mantenha o placeholder).
- Edite nome, cargo, bio e os `href` dos links em `index.html`.
- Troque `--cor-principal` em `style.css` pra mudar a cor do cartão inteiro.

## Como ver

Basta abrir `index.html` direto no navegador.

## Possíveis melhorias futuras
- Adicionar ícones (SVG) ao lado de cada link em vez de só texto.
- Adicionar um modo escuro usando outra variável CSS.
