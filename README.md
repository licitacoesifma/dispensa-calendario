# Cronograma e Itens — Dispensa Eletrônica ProEaD (Campus Porto Franco)

Material de apoio para a instrução do processo de aquisição de equipamentos e
contratação de serviços para a Coordenadoria do Curso Técnico em Informática
Subsequente EaD (ProEaD), do IFMA — Campus Porto Franco.

- **Processo:** nº 23249.010987.2026-19
- **UASG:** 158128
- **Referência:** Ofício nº 50/2026 — DDE-PFR/CAMP-PFR/IFMA, de 28/09/2026

## Conteúdo do repositório

| Arquivo | Descrição |
|---|---|
| `gantt.html` | Página interativa com o cronograma (gráfico de Gantt) das etapas da licitação, do cadastro do DFD à sessão pública. |
| `Itens_Oficio_50-2026_ProEaD_Porto_Franco.xlsx` | Planilha com os itens do Ofício nº 50/2026: aba `Itens` (valores de referência) e aba `Itens sem marca (TR)` (especificação técnica sem indicação de marca, para pesquisa de preços). |
| `build_planilha.py` | Script Python (openpyxl) que gera a planilha acima a partir dos dados do Ofício. |

## Cronograma (Gantt)

Etapas cobertas, de 6 de outubro a 2 de novembro de 2026:

1. DFD cadastrado no Compras.gov — 06 a 08/10
2. Pesquisa de preços — 06 a 13/10
3. Elaboração do ETP — 09 a 16/10
4. Elaboração do TR — 14 a 21/10
5. Elaboração do edital (aviso de contratação direta) — 22 a 27/10
6. Período aberto para propostas (dias úteis) — 28 a 30/10
7. Sessão pública — 02/11

### Como visualizar

`gantt.html` é uma página estática (HTML + CSS + JavaScript puro, sem dependências
externas além de uma fonte do Google Fonts). Para visualizar:

- Abra o arquivo diretamente no navegador, **ou**
- Publique com o GitHub Pages (`Settings → Pages → Deploy from branch`) e acesse
  pela URL gerada.

Adapta-se automaticamente ao tema claro/escuro do sistema e à largura da tela
(desktop e celular).

### Atualizar as datas

As etapas e datas estão no array `phases`, dentro da tag `<script>` em
`gantt.html`. Basta editar os campos `s` (início), `e` (fim) e `label` de cada
etapa — o layout recalcula as posições das barras automaticamente.

## Planilha de itens

Gerada com `openpyxl` a partir de `build_planilha.py`. Para regenerar após
qualquer ajuste de preços ou especificações:

```bash
pip install openpyxl
python3 build_planilha.py
```

O script escreve `Itens_Oficio_50-2026_ProEaD_Porto_Franco.xlsx` no diretório
atual, já com fórmulas de totalização (sem valores fixos).

## Observações

- Smartphone e assinatura de Office **não** constam como itens de aquisição:
  a linha móvel é contratada com o aparelho em regime de comodato, e o
  notebook já inclui o pacote de escritório licenciado.
- Os valores são referência preliminar (opção de menor preço do Ofício,
  seção 5) e não substituem a pesquisa formal de preços do Termo de
  Referência.
