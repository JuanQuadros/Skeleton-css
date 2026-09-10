# Skeleton 2.0.4 — Guia Rápido (cheatsheet)

Framework de CSS leve (grid 12 colunas + tipografia + componentes básicos).

- CDN: `https://cdnjs.cloudflare.com/ajax/libs/skeleton/2.0.4/skeleton.min.css`
- Normalize (recomendado, antes do Skeleton): `https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css`

## HTML base

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="...normalize.min.css">
  <link rel="stylesheet" href="...skeleton.min.css">
</head>
<body>...</body>
</html>
```

## Grid (12 colunas)

| Classe | Função |
|---|---|
| `.container` | Limita a 960px e centraliza |
| `.row` | Linha; limpa os floats entre colunas |
| `.columns` / `.column` | É uma coluna do grid |
| `.one.columns` … `.twelve.columns` | Largura da coluna (soma = 12) |
| `.offset-by-one` … `.offset-by-eleven` | Espaço vazio à esquerda |

Exemplo: linha com 3 colunas iguais = `four + four + four`.

> Em telas < 550px as colunas empilham automaticamente (mobile-first).

## Tipografia

- `h1`–`h6`, `p`, `a`, `strong`, `em`, `u` — já estilizados.
- `ul`, `ol` e listas aninhadas — já estilizadas.
- `blockquote` — citação com borda esquerda.
- `code` — código inline; `pre > code` — bloco de código.

## Botões (todas equivalentes)

- `<button>`, `<input type="submit|reset|button">`, `<a class="button">`.
- Versão destaque: `.button-primary`.
- Desabilitar: atributo `disabled`.

## Formulários

- Sempre `label for="idDoInput"` ligado ao campo.
- Campos: `input[type=text|email|password|number]`, `textarea`, `select`.
- `.u-full-width` deixa o campo com 100% da largura da coluna.
- Foco em azul: nativo (basta clicar no campo).
- `fieldset + legend` agrupa campos com borda própria.

## Tabelas

- Tag `table` já estilizada (bordas, espaçamento, alinhamento).
- Use `thead`/`tbody` e opcionalmente `caption`.
- `.u-full-width` para ocupar toda a largura.

## Utilitários (apenas estes!)

- `.u-full-width` — 100% da largura.
- `.u-max-full-width` — nunca passa do contêiner (imagems responsivas).
- `.u-pull-right` — flutua à direita.
- `.u-pull-left` — flutua à esquerda.
- `.u-cf` — clearfix; ponha no **pai** de elementos flutuantes.

## Não existe no Skeleton

Sem `.u-text-center`, navbar, cards, modais, tema dark, container-full,
grid customizado ou espaço fixo (gutter) ajustável. Para isso, crie suas
próprias classes num CSS personalizado carregado **depois** do Skeleton.

## Personalizar

```css
/* seu-css.css — carregar depois do skeleton.min.css */
h1 { color: #2c3e50; }
.button-primary { background-color: #27ae60; border-color: #27ae60; }
```

## Documentação
https://github.com/dhg/Skeleton/blob/master/README.md
