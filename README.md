# Festivite — Event Invite Form

Projeto de estudo focado em praticar **HTML Forms** e **CSS Grid**. O objetivo foi construir um formulário completo de criação de convite digital para eventos, com múltiplas seções, campos variados e estilização avançada.

## Estrutura do projeto

```
event-invite/
├── index.html
├── assets/
│   ├── Background.png
│   ├── Logo.svg
│   ├── icons/           # SVGs dos ícones (checkbox, radio, upload, etc.)
│   └── images/          # Imagens dos temas de evento (aniversário, casamento, etc.)
└── styles/
    ├── index.css        # Ponto de entrada — importa todos os demais arquivos
    ├── global.css       # Reset, variáveis CSS (cores, tipografia)
    ├── layout.css       # Grid principal (aside + main)
    ├── forms.css        # Estilos do formulário e fieldsets
    └── fields/
        ├── index.css    # Importa todos os arquivos da pasta fields
        ├── grid.css     # Grid do seletor de temas
        ├── input.css    # Inputs de texto, textarea, date
        ├── radio.css    # Botões radio customizados (tipo de evento e cores)
        ├── checkbox.css # Checkboxes customizados
        └── droparea.css # Área de upload de arquivo (foto de capa)
```

## Tecnologias utilizadas

- **HTML5** — estrutura semântica com `<form>`, `<fieldset>`, `<legend>`, `<input>`, `<textarea>`, `<select>`
- **CSS3** — layout, responsividade e estilização completa
- **Google Fonts** — fontes Leckerli One, Baloo 2 e Open Sans

Nenhuma biblioteca ou framework foi utilizado — HTML e CSS puros.

## Conceitos praticados

### HTML Forms
- Tipos de input: `text`, `email`, `tel`, `datetime`, `file`, `radio`, `checkbox`
- Atributos de formulário: `name`, `id`, `placeholder`, `required`, `enctype`
- Agrupamento semântico com `<fieldset>` e `<legend>`
- Upload de arquivo com `<input type="file">` e área de drag-and-drop estilizada

### CSS Grid
- Layout de duas colunas (`aside` + `main`) com `grid-template-columns`
- Grid interno nos `fieldset`s para organizar os campos
- Grid de 4 colunas para o seletor de temas de evento
- Grid de 2 colunas para campos lado a lado (ex.: início/fim, e-mail/telefone)
- Combinação de Grid e Flexbox para alinhamento interno

### Outros conceitos CSS
- Variáveis CSS (`--brand-light`, `--text-heading`, etc.) para design system
- Pseudo-classe `:has()` para estilizar o tema selecionado
- Seletor `input:valid` para exibir/ocultar mensagens de erro
- Componentes customizados de radio e checkbox via CSS puro

## Seções do formulário

1. **Sobre o evento** — título, datas de início/fim, tipo (presencial/online), local e descrição
2. **Personalização** — cor principal (radio de cores), tema do evento (grid de imagens), modo escuro (toggle) e foto de capa
3. **Dados para contato** — nome, e-mail e telefone
4. **Checkboxes** — aceite de termos de uso, e-mail e SMS promocionais
5. **Botão** — "Gerar convite"

## Como rodar

Este projeto é HTML/CSS estático — basta abrir o `index.html` em um servidor local.

**Com o Live Server (VS Code):**
1. Instale a extensão [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) no VS Code
2. Abra a pasta do projeto no VS Code
3. Clique com o botão direito em `index.html` e selecione **"Open with Live Server"**
4. O navegador abrirá automaticamente em `http://127.0.0.1:5500`

> Usar um servidor local (em vez de abrir o arquivo diretamente) garante que as fontes do Google Fonts e os assets sejam carregados corretamente.
