# Actions_Docker
Repositorio contem projeto em php, que foi dockerizado e utilizando as actions é enviado para AWS.

Projeto php clonado de [Semaphore](https://github.com/TomFern/semaphore-demo-php-unsplash)
Um projeto php com Laravel e utilizando a plataforma Unsplash, para mais detalhes entrar no repositorio.
Projeto foi contruído um Dockerfile para rodar em container.
Adicionado actions para construir a imagem e atualizar ela no DockerHub.
Adicionado actions para realizar o CI/CD no ambiente AWS.
E por fim adicionado action para realizar o teste de carga no projeto.

****Algumas issues abertas, projeto em desenvolvimento.

Para acesso do projeto acessar os seguintes IP's 54.213.15.4 ou 54.190.184.226 
O projeto faz o deploy na AWS apenas quando tem novas releases
Quando se faz alteracao na main, o projeto sobe a nova imagem no DockerHub automatico através das actions

Projeto em contrucao, a intenção é incluir no ambiente AWS um proxyreverso para que o deploy automatico sempre funcione, atualmente está com duas instancias dentro de um cluster, pois como a AWS é um serviço que preza alta disponilibidade ela nao 'derruba' um serviço sem o outro estar de pé, dessa maneira sem o proxy reverso não há maneira de dois services estar rodando na mesma porta. Por isso a necessidade da implantação de um proxy reverso que ja está nas Issues.

