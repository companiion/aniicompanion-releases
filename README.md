# AniiCompanion

Mapa ao vivo das ruínas do **Roubo dos Ovos** (Aniimo), por cima do jogo: mostra onde você está, os ninhos, os baús, a rota
e os avisos de reforço — com o mapa da sua equipe somado.

Este repositório guarda só as **versões publicadas** do app. Cada versão traz:

- `AniiCompanion-<versão>.zip` — o app (extraia a pasta inteira e abra o `AniiCompanion.exe`; o LEIA-ME está dentro);
- `manifest.json` e `manifest.json.sig` — o que o próprio app usa para se **atualizar sozinho**: ele confere a assinatura do autor e o
  SHA-256 do zip antes de instalar qualquer coisa.

## Baixar

Vá em **[Releases](https://github.com/companiion/aniicompanion-releases/releases/latest)** e baixe o `.zip`.
Depois de instalado, o app avisa quando houver versão nova ("Nova versão · Atualizar") e se atualiza com um clique.

## O Windows avisou ou bloqueou?

O app é gratuito e **não tem certificado pago de assinatura de código** — o mesmo vale para os outros mapas do Aniimo e de outros
jogos. Por isso:

1. **"O Windows protegeu o computador"**: clique em **Mais informações** → **Executar assim mesmo** (só na primeira vez).
2. **O antivírus removeu o app**: Segurança do Windows → Proteção contra vírus e ameaças → **Histórico de proteção** → Ações →
   **Restaurar**. Se repetir, adicione a pasta do AniiCompanion em **Exclusões**.
3. **Controle Inteligente de Aplicativos (Smart App Control)**: com ele ligado, nenhum app sem assinatura abre, e não há como
   liberar só um. Desligar é decisão sua (o Windows não deixa religar sem reinstalar).

Para conferir que o zip é o original, compare o **SHA-256** da página da versão com o do seu arquivo
(PowerShell: `Get-FileHash .\AniiCompanion-<versão>.zip`).

## O que o app faz e não faz

- Olha **só a imagem da janela do jogo** (como uma captura de tela) para achar você no minimapa.
- **Não** lê a memória do jogo, **não** injeta nada no jogo e **não** usa mods.
- Na internet: baixa os mapas das ruínas (aniidex.com, hideoutgacha.com), confere atualizações aqui no GitHub e, no modo online,
  conversa com os amigos que você adicionou (relays Nostr públicos).
- Mapas e marcadores: [aniidex.com](https://aniidex.com) e [HideoutGacha](https://www.hideoutgacha.com). Aniimo é marca da
  Pawprint Studio / FunPlus; este é um projeto de fã, sem ligação com eles.
