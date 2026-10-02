# nassauTickets

Frontend visual de um sistema de atendimento para laboratório de análises clínicas, feito em React e Vite. Duas telas: Atendimento e Cadastro/Emissão de Senha.

## Executar

Dentro de `frontend/`, execute:

```sh
npm install
npm run dev
```

Para gerar a versão de produção: `npm run build`. Para pré-visualizá-la: `npm run preview`.

## Escopo

Somente interface. Não há backend, API, autenticação, banco, persistência ou integração. Todos os pacientes são fictícios. A pasta backend é apenas um espaço reservado da estrutura exigida.

A navegação usa `#atendimento` e `#emissao`. A busca, os filtros, a paginação e os controles demonstram estados locais da interface. A emissão mostra uma senha fixa A036 com os dados fictícios preenchidos; não altera a fila. Os controles de atendimento não gerenciam uma fila real nem atualizam o histórico. Recarregar a página restaura os mocks. O formulário verifica somente campos vazios para demonstrar mensagens visuais, sem validar CPF ou aplicar regras clínicas.

## Organização

- `frontend/src/components/`: botões, cards, badges, campos, navegação, tabela, fila e estado vazio reutilizáveis.
- `frontend/src/pages/`: as duas telas principais.
- `frontend/src/layouts/`: layout compartilhado.
- `frontend/src/data/mockData.js`: dados de demonstração.
- `frontend/src/styles/global.css`: identidade visual e responsividade.
- `docs/`: espaços reservados para documentação do projeto.

Os componentes recebem propriedades e callbacks para facilitar a integração futura. Button oferece variantes primary, secondary e danger, além de disabled e loading. Input e Select aceitam error; Table mostra EmptyState para listas vazias. StatusBadge e PriorityBadge centralizam as representações de status e prioridade.

## Design e acessibilidade

Paleta neutra com verde discreto, bordas leves e cantos pequenos. Navegação móvel recolhível, cards e formulário adaptáveis, tabelas com rolagem horizontal contida. Labels associados aos campos, mensagens acessíveis, foco visível, botões identificados e link para pular ao conteúdo. Sem animações decorativas.

Licença MIT.
