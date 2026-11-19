# Senses + Turma do Bem — Landing de parceria

Landing page de captação de leads da parceria Senses + Turma do Bem: aromatizadores Senses
(comodato + assinatura, garantia eterna e essências MoreSenses recorrentes), com parte de cada mensalidade destinada à Turma do Bem.

Site estático: `index.html`, `styles.css`, `script.js` e `assets/`. Sem build.

## Configuração (topo do `script.js`)

| Campo | O que faz |
|---|---|
| `LEAD_WEBHOOK_URL` | URL que recebe o lead via `POST` (form-urlencoded; campos em `body.*` no n8n) (n8n, Zapier, RD Station, Apps Script…). Vazio = envia direto pro WhatsApp. |
| `WHATSAPP_NUMBER` | Número que recebe a conversa (DDI + DDD, só números). |
| `MODELS` | Os 3 modelos exibidos (nome, cobertura, specs, selo de destaque). |

Campos enviados: `nome`, `clinica`, `whatsapp`, `email`, `cidade`, `area`, `vinculo`, `modelo`, `consentimento`,
`utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `origem`, `pagina`, `enviado_em`.

## Rodar localmente

```bash
npx serve .
```

## Publicar

GitHub Pages: *Settings → Pages → Deploy from branch → `main` / root*.
