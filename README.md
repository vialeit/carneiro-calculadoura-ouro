# Calculadora de Teor de Ouro

Ferramenta de página única para avaliar ouro por **pesagem hidrostática**: informa a densidade,
o teor estimado, o quilate e quanto de ouro fino ou de liga adicionar para chegar ao teor desejado.

Não tem dependências nem build — é um arquivo HTML só, funciona offline e no celular.

## Uso

1. Pese a peça seca e anote o **peso seco (g)**.
2. Pese a peça submersa em água e informe o **empuxo** (peso seco − peso submerso) ou,
   alternando o botão, o **peso na água** direto.
3. Escolha o **quilate desejado** para ver quanto adicionar.

## Fórmulas

| Grandeza | Cálculo |
|---|---|
| Densidade | `peso seco ÷ empuxo` |
| Teor (fração de ouro `x`) | mistura por volume: `1/d = x/ρ_ouro + (1−x)/ρ_liga` |
| Quilates | `teor% × 24 ÷ 100` |
| Ouro fino atual | `peso × teor` |
| Adicionar fino (subir o teor) | `peso × (h − t) ÷ (1 − h)` |
| Adicionar liga (baixar o teor) | `fino ÷ h − peso` |

`t` = teor atual, `h` = teor desejado, ambos em fração.

## Calibração

O teor por densidade depende da **densidade da liga**, que varia com a composição
(cobre, prata, zinco) — valores usuais ficam entre 8,5 e 10,0. O padrão é **9,5**,
ajustável no cabeçalho e guardado no navegador.

Calibre uma vez com uma peça de teor conhecido: mexa na densidade da liga até o teor
calculado bater com o teor real da peça. Depois é só usar.
