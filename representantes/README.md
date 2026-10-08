# Agente de Pesquisa de Carteira — versão para representantes

Página única, sem senha e sem carteira embutida. Cada representante abre o link, escolhe a carteira que baixou do sistema (`.xls` ou `.xlsx`) e a página monta o painel, a lista de pedidos atrasados, o filtro de mês e a busca direta.

- O arquivo é lido no próprio navegador; nada é enviado a servidor algum.
- A última carteira carregada fica guardada só naquele navegador (IndexedDB). O botão "Remover deste navegador" apaga essa cópia.
- Não usa IA: a busca é por palavras e filtros ("atrasados", "em aberto", "por cliente", nome de um mês…).
- Colunas lidas: as mesmas da página principal (ver o README da raiz). O cabeçalho é reconhecido com ou sem acento e em maiúsculas ou minúsculas.
- Aceita Excel de verdade (`.xls`, `.xlsx`) e também `.xls` que seja uma tabela HTML ou texto, com números no formato brasileiro (1.234,56).
- Linhas sem número de pedido (por exemplo, uma linha de total no fim do relatório) são ignoradas, e a página avisa quantas foram.

## Arquivos

- `index.html` — a página inteira.
- `xlsx.full.min.js` — leitor de Excel (SheetJS 0.18.5), servido do próprio site.
