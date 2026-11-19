# IcomTV + Turma do Bem — Landing de parceria

Landing page de captação de leads da parceria IcomTV + Turma do Bem: parte das vendas da IcomTV é destinada
aos programas da Turma do Bem, e a sala de espera das clínicas passa a mostrar a causa. Sem valores na página.

Publicada em https://senses-turmadobem.netlify.app

Site estático: `index.html`, `styles.css`, `script.js` e `assets/`. Sem build.

## Configuração (topo do `script.js`)

| Campo | O que faz |
|---|---|
| `LEAD_WEBHOOK_URL` | URL que recebe o lead via `POST` (form-urlencoded; campos em `body.*` no n8n) (n8n, Zapier, RD Station, Apps Script…). Vazio = envia direto pro WhatsApp. |
| `WHATSAPP_NUMBER` | Número que recebe a conversa (DDI + DDD, só números). |

Campos enviados: `nome`, `clinica`, `whatsapp`, `email`, `cidade`, `vinculo`, `participacao`, `consentimento`,
`utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `origem`, `pagina`, `enviado_em`.

## Rodar localmente

```bash
npx serve .
```

## Publicar

GitHub Pages: *Settings → Pages → Deploy from branch → `main` / root*.
