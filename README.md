# ORGANIZA – Gerenciador Inteligente de Tarefas (versão corrigida)

Aplicação web para cadastro, organização e acompanhamento de tarefas. Desenvolvida com HTML5, CSS3 e JavaScript.

## Como abrir
1. Extraia o arquivo ZIP.
2. Abra `index.html` no navegador. O cadastro e o armazenamento local funcionam sem servidor.
3. Para testar também a integração com a API, recomenda-se abrir a pasta no Visual Studio Code e iniciar o **Live Server**. A consulta externa depende de conexão com a internet.

## Funcionalidades
- Adicionar tarefas com título, descrição, categoria, prioridade e data de vencimento.
- Marcar como concluída, editar e excluir.
- Filtrar todas, ativas e concluídas.
- Buscar por palavra-chave.
- Salvar tarefas no LocalStorage, mantendo os dados após fechar/atualizar a página no mesmo navegador.
- Estatísticas de total, concluídas e pendentes.
- Tema claro/escuro com preferência salva.
- Reordenar cartões por drag and drop.
- Exportar tarefas para JSON.
- Consultar sugestão de atividade usando Fetch API e async/await.

## API pública
JSONPlaceholder: https://jsonplaceholder.typicode.com/
Endpoint: `https://jsonplaceholder.typicode.com/todos/{id}`
Não exige chave de API. A API fornece uma sugestão de tarefa de exemplo; as tarefas pessoais ficam no LocalStorage.

## Estrutura
```text
trabalho3/
├── index.html
├── css/style.css
├── js/app.js
├── js/api.js
├── js/storage.js
├── images/
└── README.md
```

## Conceitos demonstrados
Manipulação do DOM (`querySelector`, `createElement`, `textContent`, `classList`), eventos (`click`, `submit`, `input`, `change`), delegação de eventos, Fetch API, programação assíncrona (`async/await`, `try/catch/finally`), LocalStorage, `JSON.parse()` e `JSON.stringify()`.

## Observação sobre os dados
Os dados são guardados no armazenamento local do navegador e não são sincronizados entre dispositivos. Utilize **Exportar JSON** para criar uma cópia de segurança. Se abrir o projeto em outro navegador ou limpar os dados do site, a lista local não será a mesma.

## Testes para validar
1. Cadastre uma tarefa e veja se aparece imediatamente na lista.
2. Atualize a página e confirme que a tarefa continua registrada.
3. Edite, conclua e exclua uma tarefa.
4. Teste busca e filtros.
5. Alterne o tema e atualize a página.
6. Exporte o JSON.
7. Clique em “Buscar sugestão” com internet disponível.
