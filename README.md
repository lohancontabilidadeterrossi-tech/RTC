# Simulador da Reforma Tributária | Terrossi Contabilidade

Ferramenta web que simula o impacto da Reforma Tributária do consumo (IBS, CBS e Imposto Seletivo) em empresas de todo o Brasil, ano a ano, de 2026 a 2033.

A empresa informa segmento, regime tributário, faturamento, crédito de fornecedores e nicho de atividade, e recebe um relatório com a carga atual, a carga estimada em 2033, a linha do tempo da transição, a base legal aplicada e recomendações. O relatório pode ser baixado em PDF.

## Base legal

- Emenda Constitucional 132/2023
- Lei Complementar 214/2025
- Lei Complementar 227/2026
- Comitê Gestor do IBS

## Estrutura

```
index.html   página única com HTML, CSS e JavaScript (logo embutida)
vercel.json  configuração mínima de site estático
README.md    este arquivo
```

Não há build, dependências para instalar nem backend. As bibliotecas html2canvas e jsPDF (geração do PDF) são carregadas por CDN.

## Rodar localmente

Abra o `index.html` no navegador, ou use um servidor simples:

```
npx serve .
```

## Publicar na Vercel pelo GitHub

1. Suba este repositório no GitHub.
2. Em vercel.com/new, escolha "Import Git Repository" e selecione o repositório.
3. Em Framework Preset, deixe "Other". Não preencha build command nem output directory.
4. Clique em Deploy.

Cada novo commit na branch principal gera um novo deploy automaticamente.

## Personalização rápida

- Botão de WhatsApp: a função `enviarLead()` no final do `index.html` monta o link `https://wa.me/`. Para enviar direto ao número da empresa, use `https://wa.me/55DDDNUMERO?text=...`.
- Cores: variáveis no bloco `:root` do CSS (preto, branco e dourado).

## Aviso

A simulação é uma estimativa simplificada, com fins educativos e de prospecção comercial. As alíquotas de referência dependem de Resolução do Senado e de regulamentação do Comitê Gestor do IBS. Não substitui um estudo tributário formal.
