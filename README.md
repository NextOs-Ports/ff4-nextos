# Final Fantasy IV — NextOS ports (3D Remake + The After Years)

Um repositório, dois jogos — mesmo modelo do `geometrydash-nextos`:

| Jogo | Pasta | Versão | Zip da release |
|---|---|---|---|
| Final Fantasy IV 3D Remake | [`ff4/`](ff4/) | 1.0.4 | `ff4-1.0.4.zip` |
| Final Fantasy IV: The After Years | [`ff4a/`](ff4a/) | 1.0.6 | `ff4a-1.0.6.zip` |

Ports nativos AArch64 (so-loader) da engine cuore/Matrix (GLES1 fixed-function)
para consoles portáteis Linux — NextOS, dArkOS/R36S e ROCKNIX. **BYO-data:
nenhum dado de jogo acompanha este repositório nem os zips** — o NXExtract
monta os dados a partir do APK do próprio usuário (`gamedata/`).

## Estado (25/08/2026)

- Zips **determinísticos** da onda v2 do framework (nxbootstrap 0.6.30,
  NXExtract 1.2.18, nxgl 0.2.14 com seleção de provedor GLES1 **por medição**).
- **Aprovados em campo**: dArkOS/R36S (prova física, frame proof 99%+) e
  **ROCKNIX RK3566** (logs de 25/08: provider vivo Panfrost, frame proof 100%,
  30fps, saída limpa) — o fix da tela preta do ROCKNIX está confirmado.
- Publicação pública aguarda validação NextOS (#22b).

## Build

Cada jogo builda da própria pasta: `cd ff4 && ./build_universal.sh` (idem
`ff4a/`). Os módulos do framework entram como vendor compilado via pins de
release (`nxrelease.json` / `nxproject.json`); o código do framework **não**
faz parte deste repositório.

Repositório **privado** — backup do trabalho NextOS. Publicação pública, se
houver, nasce de árvore limpa (histórico não vem junto).
