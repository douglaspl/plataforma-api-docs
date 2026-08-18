# Integração SSO — Especificação Técnica

Documentação técnica pública da integração de Single Sign-On (SSO) da **Plataforma Semente**, destinada a parceiros integradores (escolas e sistemas de gestão escolar).

Descreve o fluxo de autenticação via JWT assinado com HMAC-SHA256 (HS256): pré-requisitos, especificação das claims do token, o endpoint de integração e exemplos de geração do JWT em C#, Python, Java, Node.js e PHP.

## Conteúdo

Tudo está em um único arquivo autocontido — [`index.html`](index.html) — sem dependências além de fontes e syntax highlighting carregados via CDN (Google Fonts e highlight.js). Não há build, framework ou etapa de compilação.

## Publicando com GitHub Pages

1. No GitHub, vá em **Settings → Pages**.
2. Em **Source**, selecione a branch `main` e a pasta `/ (root)`.
3. Salve. O site ficará disponível em `https://<usuario-ou-org>.github.io/<nome-do-repositorio>/`.

Qualquer alteração enviada (`git push`) para a branch configurada é publicada automaticamente em alguns minutos.

## Desenvolvimento local

Como é um HTML estático, basta abrir `index.html` diretamente no navegador, ou servir a pasta com qualquer servidor HTTP simples, por exemplo:

```bash
python -m http.server 8000
```

e acessar `http://localhost:8000`.
