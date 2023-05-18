# MEUTIME
Desenvolvimento da aplicação Meu Time utilizando Angular e containerização usando o Docker. Com as funcionalidade de login com a API KEY da API-FOOTBALL, permitindo a seleção de país, liga e time, exibindo os detalhes do time, jogadores, formações, estatísticas e gols por minuto.

Para desenvolver a aplicação Meu Time utilizando Angular e JavaScript, siga os passos abaixo:

Passo 1: Configuração do ambiente de desenvolvimento
Certifique-se de ter o Node.js e o npm (gerenciador de pacotes do Node.js) instalados em seu sistema.
Instale o Angular CLI globalmente executando o seguinte comando no terminal (arquivo 1)


Passo 2: Criação do projeto Angular
Abra o terminal e navegue até o diretório onde deseja criar o projeto.
Execute o seguinte comando para criar um novo projeto Angular (ARQUIVO 2)
Responda às perguntas interativas conforme necessário, como a folha de estilo a ser usada (CSS, SCSS, etc.).
Aguarde até que a criação do projeto seja concluída.


Passo 3: Implementação do login
Crie um componente para a tela de login (ARQUIVO 3)
Implemente a lógica de autenticação no componente de login. Utilize o serviço HttpClient do Angular para fazer a requisição de autenticação para a API-FOOTBALL usando a chave de autenticação fornecida pelo usuário. (ARQUIVO 4) 
Crie um template HTML para o componente de login (login.component.html) e estilize-o conforme necessário.


Passo 4: Implementação da seleção de país, temporada, liga e time
Crie componentes adicionais para cada etapa de seleção (país, temporada, liga e time) da mesma forma que foi feito para o componente de login.
Utilize o serviço HttpClient para fazer as requisições necessárias para a API-FOOTBALL e exibir os dados retornados ao usuário. (ARQUIVO 5)
Crie os templates HTML correspondentes para cada componente e estilize-os conforme necessário.


Passo 5: Implementação da visualização de dados do time
Crie um componente para exibir os detalhes do time selecionado. (ARQUIVO 6)
Utilize o serviço HttpClient para fazer uma requisição para obter os detalhes do time selecionado. (ARQUIVO 7)
Crie um template HTML para o componente team-details (team-details.component.html) para exibir os detalhes do time, jogadores, formações, estatísticas e gols por minuto.
Estilize o template conforme necessário.


Passo 6: Containerização da aplicação
Crie um arquivo chamado Dockerfile na raiz do projeto Angular.
Abra o arquivo Dockerfile e adicione o seguinte conteúdo: (ARQUIVO 8)
Abra o terminal e navegue até o diretório raiz do projeto.
Execute o seguinte comando para construir a imagem do Docker: (ARQUIVO 9)
Após a conclusão da construção da imagem, você pode executar o contêiner com o seguinte comando: (ARQUIVO 10) 
Acesse a aplicação no navegador utilizando o endereço http://localhost:80.

Com esses passos, você criou a aplicação Meu Time
utilizando o Angular e a API-FOOTBALL. A aplicação permite ao usuário realizar o login utilizando a chave de autenticação da API-FOOTBALL e, em seguida, selecionar um país, uma liga e um time para visualizar os detalhes relacionados.
Lembrando que a aplicação consome a API-FOOTBALL, portanto é necessário que o usuário tenha uma conta e gere sua própria chave de autenticação.

Para continuar o desenvolvimento da aplicação, siga os passos abaixo:


Passo 7: Criação do serviço de autenticação
Crie um novo serviço chamado AuthService para gerenciar a autenticação na aplicação. (ARQUIVO 11)
No componente de login, você pode injetar e utilizar esse serviço para realizar o login com a API-FOOTBALL e armazenar a chave de autenticação.
Importe e injete o AuthService no componente de login. (ARQUIVO 12)
Agora você pode utilizar o serviço AuthService para verificar se o usuário está autenticado em outros componentes da aplicação.


Passo 8: Implementação das regras de negócio
Nos componentes responsáveis por selecionar país, liga e time, você deve implementar as regras de negócio para garantir que as seleções sejam feitas corretamente, de acordo com os critérios de aceite definidos.
Utilize os métodos e propriedades do serviço AuthService para verificar se o usuário está autenticado antes de permitir a seleção de um país, liga ou time.
Implemente a lógica necessária para validar a sequência correta de seleções (país, liga e time) e garantir que não seja possível selecionar uma liga sem ter selecionado um país anteriormente, nem selecionar um time sem ter selecionado uma liga anteriormente.


Passo 9: Exibição dos detalhes do time e componentes relacionados
No componente TeamDetailsComponent, utilize as propriedades teamDetails, players, formations, teamStatistics e goalsByMinute para exibir os detalhes do time, jogadores, formações, estatísticas e gols por minuto na interface do usuário.
Utilize os dados obtidos das requisições à API-FOOTBALL para exibir as informações relevantes de cada seção.
Desenvolva o template do componente TeamDetailsComponent para exibir as informações do time, jogadores, formações, estatísticas e gols por minuto. Você pode usar os seguintes exemplos como referência: (ARQUIVO 13)
Certifique-se de que os dados do time, jogadores, formações, estatísticas e gols por minuto sejam carregados corretamente no componente TeamDetailsComponent antes de serem exibidos.


Passo 11: Containerização da aplicação
Para containerizar a aplicação Angular, você pode usar o Docker.
Crie um arquivo chamado Dockerfile na raiz do projeto com o seguinte conteúdo: (ARQUIVO 14)
Abra o terminal e navegue até a raiz do projeto.
Execute o seguinte comando para construir a imagem Docker: (ARQUIVO 15)
Após a conclusão do processo, você pode executar a imagem Docker em um contêiner: (ARQUIVO 16) 
Agora, a aplicação Angular estará disponível na porta 80 do seu localhost. Você pode acessá-la em um navegador digitando http://localhost:80.
