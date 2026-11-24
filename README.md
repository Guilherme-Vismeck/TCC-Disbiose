# Evidências de disbiose em bases de dados integradas — site do TCC

Página interativa em um único HTML (sem build, sem dependências) com os gráficos do TCC de Guilherme Vismeck Costa Stabel (UniBrasil, 2026).

## Publicar no GitHub Pages
1. Crie um repositório e envie `index.html`, `build_data.py` e este `README.md`.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.
3. O endereço sai em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

## Rastreabilidade
`build_data.py` lê os CSVs de `Processados/` (e o xlsx de espécies) e gera `data.json`, que `template.html` embute em `index.html` (marcador `__DATA__`).
Cada gráfico cita o notebook e o CSV de origem, e a seção final baixa em CSV os números de cada figura.
Regerar: `python build_data.py Processados` e substituir `__DATA__` do `template.html` pelo conteúdo de `data.json`.
