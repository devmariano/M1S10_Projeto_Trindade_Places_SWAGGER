# M1S10_Projeto_Trindade_Places Adição da documentação por Swagger

<!---Esses são exemplos. Veja https://shields.io para outras pessoas ou para personalizar este conjunto de escudos. Você pode querer incluir dependências, status do projeto e informações de licença aqui--->


> O projeto Trindade Places é uma iniciativa importante da prefeitura de Trindade para fornecer informações precisas e atualizadas sobre as instituições que prestam serviços públicos na cidade. Através da API desenvolvida em Node.js, os usuários poderão pesquisar, criar, atualizar e excluir informações sobre essas instituições, como nome do lugar e localização.

> A escolha das tecnologias express e sequelize para o desenvolvimento do projeto permite uma implementação eficiente e escalável da API, enquanto a integração com o banco de dados garante que os dados sejam armazenados de forma segura e facilmente acessíveis para consulta e atualização.

> O principal objetivo do projeto é fornecer uma base de dados confiável para a cidade de Trindade, visando melhorar a gestão dos serviços públicos e aumentar a transparência das informações sobre as instituições públicas.

> Com a API desenvolvida, a prefeitura poderá fornecer aos cidadãos uma fonte confiável e atualizada de informações sobre os serviços públicos disponíveis na cidade, contribuindo para uma melhor qualidade de vida para a população.

O projeto ainda está em desenvolvimento e as próximas atualizações serão voltadas nas seguintes tarefas:

- [x] Tarefa 1: Após criar a estrutura inicial, é necessário criar um novo modelo Sequelize chamado Place para representar um local. Para isso, é importante definir corretamente seus campos para que possa ser utilizado adequadamente. Os campos que devem ser definidos são:

  * id: um número que serve como identificador único para o local.
  * name: uma string que representa o nome do local.
  * telefone: uma string que representa o número de telefone do local.
  * opening hours: uma string que representa o horário de funcionamento do local.
  * description: uma string que representa a descrição do local.
  * latitude: um número que representa a latitude do local.
  * longitude: um número que representa a longitude do local
  
- [x] Tarefa 2: Após criar o modelo Place no exercício anterior, é necessário implementar uma rota do tipo POST com o path "/places" que receba valores por meio de BODY params. Os seguintes valores devem ser recebidos:
```
{
"name":"Instituto nova 4",
"telephone":"2198645645665",
"opening_hours":"Abre as 8h fecha 12h",
"description":"instituto teste de app",
"latitude": -23.5505,
"longitude": -46.6333
}
```
 


- [x] Tarefa 3: Aprimore o projeto Trindade Places implementando uma rota GET com o path /places, que retorne a lista de lugares cadastrados na base de dados.

  Essa rota permitirá aos usuários consultar todas as instituições públicas disponíveis na cidade de Trindade, fornecendo informações relevantes sobre cada uma delas.

  Essa implementação é fundamental para a transparência e eficiência na gestão dos serviços públicos, permitindo aos cidadãos acessar informações sobre as instituições de forma fácil e rápida. Com isso, será possível melhorar a qualidade dos serviços públicos na cidade.
  
- [x] Tarefa 4: Para melhorar ainda mais a API do projeto Trindade Places, é necessário implementar uma rota DELETE. Essa rota deve permitir aos usuários excluir uma instituição pública específica da base de dados. Para isso, é preciso definir um identificador único para cada instituição, que será utilizado na requisição de exclusão.

  A rota DELETE pode ser implementada com o path /places/:id, onde o parâmetro :id representa o identificador único da instituição. Ao receber uma requisição DELETE com esse path, a API deve verificar se o identificador corresponde a uma instituição válida na base de dados e, em caso positivo, excluí-la.

  A implementação da rota DELETE é essencial para permitir que os usuários tenham controle sobre as informações presentes na base de dados, garantindo a integridade e a atualização dos dados. Além disso, essa rota é importante para manter a transparência e a eficiência na gestão dos serviços públicos, permitindo que as instituições sejam atualizadas ou excluídas quando necessário.
  
- [x] Tarefa 5: A rota PUT é outra funcionalidade importante que deve ser implementada na API do projeto Trindade Places. Essa rota permite que os usuários atualizem as informações de uma instituição pública específica na base de dados.

  Para implementar a rota PUT, é preciso definir um identificador único para cada instituição, que será utilizado na requisição de atualização. Além disso, é necessário definir quais campos da instituição poderão ser atualizados pelos usuários.


  A rota PUT pode ser implementada com o path /places/:id, onde o parâmetro :id representa o identificador único da instituição. Ao receber uma requisição PUT com esse path, a API deve verificar se o identificador corresponde a uma instituição válida na base de dados e, em caso positivo, permitir a atualização dos campos definidos.

  A rota permitirá atualizar todos os campos cadastrados, exceto o ID
  
- [x] Tarefa 6: Após as implementações anteriores, é necessário criar um novo modelo Sequelize chamado "User" para representar um usuário válido no sistema. Para isso, é importante definir corretamente seus campos para que possa ser utilizado adequadamente. Os campos que devem ser definidos são:

  id: um número que serve como identificador único para o usuário.
  name: uma string que representa o nome completo do usuário.
  email: uma string que representa o endereço de email do usuário. Deve ser única e válida.
  username: uma string que representa o nome de usuário do usuário. Deve ser única.
  password: uma string que representa a senha do usuário. Deve ter no mínimo 8 caracteres.

  Ao criar o modelo "User" com esses campos definidos corretamente, será possível utilizá-lo para representar usuários válidos no sistema e armazenar suas informações de maneira segura e eficiente.

- [x] Tarefa 7: Após criar o modelo User no exercício anterior, é necessário implementar uma rota do tipo POST com o path "/users" que receba valores por meio de BODY params.

- [x] Tarefa 8: Após criar a rota POST no exercício anterior, é necessário implementar uma rota do tipo POST com o path "/sessions" que receba um username e password.

  Na rota POST com o path "/sessions", devem ser recebidos um username e password como parâmetros da requisição. Em seguida, a aplicação deve verificar se o usuário existe no banco de dados. Se o usuário existir, deve ser gerado um token JWT (JSON Web Token) contendo o id do usuário e injetado no corpo da resposta.

  É importante garantir que o token seja gerado com segurança, seguindo as boas práticas de codificação e criptografia. Além disso, é importante que as informações sejam retornadas de forma clara e organizada para que a integração com outros sistemas ou aplicações seja facilitada.

- [x] Tarefa 9: Para garantir a segurança da aplicação, implemente um middleware que valide se o token recebido é válido. Esse middleware será responsável por verificar se o token foi gerado corretamente e se ainda está válido.

  Além disso, é importante definir que todas as rotas da aplicação, exceto a rota raiz e a rota de sessão, devem ser privadas. Isso significa que apenas usuários autenticados, ou seja, aqueles que possuem um token válido, terão acesso a essas rotas.

- [x] Tarefa 10: Para tornar a estrutura do projeto mais organizada e fácil de gerenciar, é importante realizar algumas ações importantes.

  Separar os controllers em arquivos diferentes, para facilitar o gerenciamento do código;
  Criar middlewares de validação utilizando a biblioteca YUP, garantindo que as informações enviadas pelo cliente estejam corretas e possam ser processadas pela aplicação;
  Implementar variáveis de ambiente para dados sensíveis, como senhas, chaves de API e tokens, para evitar que esses dados sejam expostos acidentalmente e aumentar a segurança da aplicação;
  Agrupar as rotas em arquivos diferentes, de acordo com o objetivo ou funcionalidade específica, para facilitar o gerenciamento do código e manter a organização do projeto de forma clara e concisa.
  Essas ações são simples de implementar, mas podem fazer uma grande diferença na estrutura do projeto, tornando-o mais seguro, organizado e fácil de gerenciar. Além disso, podem ajudar a reduzir o tempo de desenvolvimento, aumentar a produtividade e garantir um produto final de alta qualidade e eficiência.

- [x] Tarefa 11: Documente todas as rotas do projeto utilizando Swagger.
  - Para atualizar a documentação utilize o comando: npm run swagger-autogen
  - Utilize o comando http://localhost:3535/doc/#/ para ver a docuemntação no navegador
![image](https://user-images.githubusercontent.com/86934710/235498745-bd0aed21-bb54-46c5-8454-0cd06d54c1df.png)


## 💻 Pré-requisitos

Para iniciar um novo projeto Node.js + Express e contribuir para o desenvolvimento da API do projeto Trindade Places, siga os seguintes passos:

* Certifique-se de ter o Node.js instalado em sua máquina.
* Abra um terminal e crie uma nova pasta para o seu projeto.
* Navegue até a pasta criada e inicialize o npm com o comando "npm init".
* Instale o Express utilizando o comando "npm install express".
* Crie um arquivo chamado "index.js" na raiz do seu projeto.
* Abra o arquivo "index.js" e importe o Express com o comando "const express = require('express')".
* Inicie o servidor Express e defina a porta 3333

## 🚀 Como testar o projeto

No postgre SQL crie uma base de dados trindade_places

Rode a aplicação node via terminal atrvés do comando
```
<npm start>
```

1. Rota para criar um cadastro :
```
localhost:3000/places/cadastro
```
enviar através POST um body com o seguinte Json
```
{
"name":"Instituto nova 4",
"telephone":"2198645645665",
"opening_hours":"Abre as 8h fecha 12h",
"description":"instituto teste de app",
"latitude": -23.5505,
"longitude": -46.6333
}
```

2. Rota para atualizar um cadastro :
```
localhost:3000/places/atualiza/1
```
enviar através UPDATE defina o id do cadastro a atualizar e envie um body com a seguinte estrutura Json
```
{
"name":" ",
"telephone":" ",
"opening_hours":" ",
"description":" ",
"latitude": -0,
"longitude": 0
}
```

3. Rota para deletar um cadastro :
```
localhost:3000/places/deleta/5
```
enviar através DELETE definindo o id do cadastro a excluir

4. Rota para listar um cadastro :
```
localhost:3000/places/pesquisa/5
```
enviar através GET definindo o id do cadastro a pesquisar

5. Rota para listar todos cadastros :
```
localhost:3000/places/pesquisa/
```



[⬆ Voltar ao topo]<br>
