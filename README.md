# Documentação de Integrações — Plataforma Semente

Portal de documentação técnica pública das integrações da **Plataforma Semente**, destinado a parceiros integradores (escolas e sistemas de gestão escolar).

`index.html` é a página inicial (vitrine), que lista as integrações disponíveis e futuras. Cada integração tem sua própria página em [`docs/`](docs).

## Estrutura

```
/
├─ index.html          → hub: lista todas as integrações
├─ docs/
│  └─ sso.html          → Integração SSO (JWT / HMAC-SHA256)
└─ README.md
```

Conforme novas integrações forem documentadas (cadastro de usuários, cadastro de escolas, endpoints de consulta como matrículas e status de conclusão, etc.), cada uma ganha um novo arquivo em `docs/` e um card correspondente em `index.html`.

Cada página é um HTML autocontido (CSS e JS inline), sem build, framework ou etapa de compilação — só fontes e syntax highlighting carregados via CDN (Google Fonts e highlight.js).

## Identidade visual

As páginas seguem o Manual de Identidade Visual da Plataforma Semente (tipografia, cores e o símbolo da marca):

- **Tipografia:** Poppins (única fonte web — a fonte principal da marca, Conigen, está disponível só via Adobe Fonts e não é usada aqui; o próprio manual indica Poppins como a variação para plataformas digitais).
- **Cores institucionais:** verde `#8AB925` (predominante) e `#55782C` (escuro, usado no topbar e headings), azul-marinho `#1A2E3D`, amarelo `#F4BB2F`, vermelho `#E61D47`, cinza-escuro `#333233`, creme `#F2EFE9`, além dos secundários azul-claro `#3FA5C3` e roxo `#765AA3`.
- **Símbolo:** o ícone de 5 partes é usado no topbar de cada página e como favicon (`favicon.svg`), sempre nas cores oficiais completas — a variação de símbolo em cor única (ligada às competências socioemocionais) exige validação do time de Marketing e não deve ser usada aqui.

## Publicando com GitHub Pages

1. No GitHub, vá em **Settings → Pages**.
2. Em **Source**, selecione a branch `main` e a pasta `/ (root)`.
3. Salve. O site ficará disponível em `https://<usuario-ou-org>.github.io/<nome-do-repositorio>/`.

Qualquer alteração enviada (`git push`) para a branch configurada é publicada automaticamente em alguns minutos.

## Desenvolvimento local

Como é HTML estático, basta abrir `index.html` diretamente no navegador, ou servir a pasta com qualquer servidor HTTP simples, por exemplo:

```bash
python -m http.server 8000
```

e acessar `http://localhost:8000`.

## Adicionando uma nova integração

1. Crie o arquivo em `docs/<nome-da-integracao>.html`, seguindo o padrão visual das páginas existentes (fonte Poppins, paleta verde, sumário lateral sticky).
2. Adicione um card em `index.html`, no grupo apropriado (crie um novo grupo se for uma categoria nova).
3. Links de volta ao hub usam `../index.html` a partir de `docs/`.
