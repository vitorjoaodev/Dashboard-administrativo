Dashboard Interativo
Um painel administrativo interativo e responsivo desenvolvido com HTML, CSS e JavaScript puro, utilizando Tailwind CSS para estilização e Chart.js para visualização de dados. Essa aplicação demonstra como criar um dashboard moderno e funcional sem a necessidade de frameworks complexos.

Características

Design Responsivo: Funciona em dispositivos de todos os tamanhos
Cards Estatísticos: Exibição clara de KPIs importantes
Visualizações Gráficas: Gráficos de linha e barras para análise de tendências
Tabela de Dados: Exibição tabular de dados detalhados
Filtros Interativos: Filtros por categoria e período para refinamento dos dados
Simulação de Dados em Tempo Real: Atualização automática para demonstrar recursos dinâmicos

Tecnologias Utilizadas

HTML5: Estruturação semântica da página
CSS/Tailwind CSS: Framework CSS utilitário para estilização rápida
JavaScript (ES6+): Lógica de interatividade e manipulação de dados
Chart.js: Biblioteca para criação de gráficos interativos
Fetch API: Para simulação de chamadas a APIs RESTful

Como Usar? 

Instalação Local

Clone este repositório:
bashCopiargit clone [URL-DO-REPOSITÓRIO]
cd [NOME-DA-PASTA]

Abra o arquivo index.html em seu navegador.

Uso no Replit

Crie um novo Replit usando o template "HTML, CSS, JS"
Substitua todo o conteúdo do arquivo index.html pelo código do projeto
Execute o projeto clicando em "Run"

Conectando a uma API Real
Para conectar o dashboard a uma API REST real, modifique a função fetchData() no arquivo index.html:
javascriptCopiarasync function fetchData(filter = '') {
  try {
    const url = `https://sua-api.com/dados${filter ? `?filter=${filter}` : ''}`;
    const response = await fetch(url);
    
    if (!response.ok) {
      throw new Error('Falha ao obter dados');
    }
    
    return await response.json();
  } catch (error) {
    console.error('Erro ao buscar dados:', error);
    return [];
  }
}
Estrutura do Projeto
Copiardashboard/
│
├── index.html      # Arquivo principal com HTML, CSS e JavaScript
└── README.md       # Este arquivo de documentação
Customização
Adicionando Novos Cards Estatísticos
Para adicionar novos cards estatísticos, expanda o array mockData.stats com novos objetos:
javascriptCopiar{
  title: 'Título do Card',
  value: 'Valor',
  icon: 'Ícone', 
  color: 'bg-red-100 text-red-600'
}
Modificando os Gráficos
Os gráficos são criados usando Chart.js. Para modificar tipos, cores ou comportamentos, altere as configurações nos objetos Chart dentro da função renderCharts().
Recursos Adicionais

Para adicionar autenticação, considere implementar JWT ou OAuth2
Para persistência de dados, adicione integração com localStorage ou IndexedDB
Para análises mais complexas, considere adicionar bibliotecas como D3.js

Limitações Atuais

Dados simulados (mock data) em vez de dados reais
Funcionalidades de exportação de dados não implementadas
Sem sistema de autenticação de usuários

Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com melhorias.
Licença
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.
Contato
Desenvolvido por João Vitor - https://www.linkedin.com/in/joaovitorfullstack/
