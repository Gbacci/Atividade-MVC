# <a name="c1"></a> Abandono Zero

# <a name="c1"></a> Descrição

&nbsp;&nbsp;&nbsp;&nbsp;
No contexto atual, o abandono de animais é uma questão alarmante que afeta comunidades em todo o mundo. Enquanto esforços significativos têm sido feitos para abordar esse problema, a falta de dados concretos sobre os motivos que levam os donos a abandonarem seus animais representa um desafio significativo. Compreender as razões por trás do abandono é fundamental para desenvolver estratégias eficazes de prevenção e intervenção. Este projeto busca preencher essa lacuna, explorando a relação entre a falta de dados sobre os motivos do abandono de animais e os próprios motivos do abandono. Ao fazê-lo, não apenas esperamos fornecer dados para informar políticas e programas de conscientização, mas também contribuir para a proteção e o bem-estar dos animais em nossas comunidades.

&nbsp;&nbsp;&nbsp;&nbsp;
Estamos criando um website com um questionário que terá como objetivo coletar dados de usuários que tem, tiveram ou terão cachorros. Esses dados serão armazenados e posteriormente utilizados pelo INSPA (Instituto de Psicologia Animal), que busca oferecer cursos de pós-graduação que focam no comportamento e bem-estar humano-animal, para entender melhor o contexto de abandonos de cachorros e dessa forma tomar medidas efetivas baseadas em dados para acabar com esse problema. 

# <a name="c1"></a> Ferramentas de Diagramação
&nbsp;&nbsp;&nbsp;&nbsp;
Para fazer o MVC eu utilizei a ferramenta <a href="https://app.diagrams.net/">Draw.io</a> que foi indicada pelo professor Afonso durante a aula.

# <a name="c1"></a> Views
&nbsp;&nbsp;&nbsp;&nbsp;
As views, constituem a interface de apresentação da aplicação, desempenhando um papel crucial na exibição dos dados ao usuário de forma acessível e interativa. Elas atuam como o ponto de contato direto entre o sistema e o usuário, traduzindo informações complexas em elementos visuais compreensíveis e proporcionando uma experiência de interação intuitiva.
&nbsp;&nbsp;&nbsp;&nbsp;

O meu projeto tem 6 views, sendo elas a Initial Screen, Registration/Login Screen, Forms Screen, Future Form Screen, Last Form Screen e Form Results.
&nbsp;&nbsp;&nbsp;&nbsp;

A primeira tela, denominada "Initial Screen", abrange todos os elementos presentes na tela inicial da aplicação, incluindo a Navigation Bar, Header, Imagens relacionadas ao projeto e um Footer. Além disso, oferece funcionalidades interativas por meio de botões que direcionam o usuário para outras seções dentro dessa mesma tela inicial. Por não necessitar de interações com outros componentes, não há setas que a conectem a algum Controller.
&nbsp;&nbsp;&nbsp;&nbsp;

A segunda tela, conhecida como "Register/Login Screen", é acessível por meio do botão "Register/Login" ou do botão "Forms" na Initial Screen. Nesta etapa, os usuários têm a opção de inserir seu endereço de e-mail e senha para efetuar login ou registro, ou optar por fazer login usando a conta do Google. Todas as informações fornecidas são registradas, verificadas e validadas por meio de um controller chamado "User", que encaminha esses dados para serem armazenados no banco de dados.
&nbsp;&nbsp;&nbsp;&nbsp;

Posteriormente, o sistema apresenta três visualizações destinadas a armazenar informações das diferentes perguntas nos formulários disponíveis no site. A primeira é designada para a primeira pergunta "Forms Screen", a segunda para a pergunta subsequente "Future Form Screen" e a terceira para a última pergunta "Last Form Screen". Estes formulários são compostos por um título principal "h1" contendo a questão, uma caixa de resposta, uma barra de progresso, um botão para avançar para a próxima pergunta e outro para retroceder para a pergunta anterior. Na página Last Form Screen, em vez de um botão para a próxima pergunta, há um botão para enviar as respostas.
&nbsp;&nbsp;&nbsp;&nbsp;

Por fim, há uma visualização denominada Forms Results, reservada aos administradores que possuem acesso aos resultados da pesquisa. Nesta visualização, os administradores podem visualizar as tabelas contendo os dados preenchidos pelos respondentes. A interface do Admin inclui gráficos para exibir os resultados, um botão de busca para encontrar resultados específicos, um botão de filtragem por região e um botão para ocultar os dados exibidos na tela.

# <a name="c1"></a> Controllers
&nbsp;&nbsp;&nbsp;&nbsp;
Na arquitetura Modelo-Visão-Controlador (MVC), os controladores assumem a responsabilidade de receber as requisições feitas pelo usuário, interpretá-las e coordenar as interações entre os models e as views. Eles asseguram que a lógica de negócios seja adequadamente aplicada aos dados e que a interface do usuário seja atualizada conforme as ações do usuário e as alterações nos dados.
&nbsp;&nbsp;&nbsp;&nbsp;

No modelo apresentado acima, são identificados seis controladores. O primeiro, denominado Users, desempenha o papel de arquivar e validar as informações do usuário junto ao servidor, atuando como uma interface entre a tela de login e o banco de dados que armazena os dados dos usuários. Este controlador possui os métodos "archive" para armazenar os dados no banco de dados, "Validate" para autenticar as informações quando um usuário tenta fazer login e "CheckRole" para determinar o acesso do usuário com base em seu papel no sistema, seja para visualizar formulários, resultados ou outras funcionalidades correspondentes ao seu papel.
&nbsp;&nbsp;&nbsp;&nbsp;

Por fim, há um controller destinado a facilitar as operações relacionadas à parte administrativa. Este controller conta com os métodos "search", para permitir a pesquisa das informações desejadas pelo administrador, e "RegionButton", que tem o propósito de exibir as regiões dos usuários que responderam ao formulário.

# <a name="c1"></a> Models
&nbsp;&nbsp;&nbsp;&nbsp;

Os modelos desempenham um papel fundamental na arquitetura MVC (Model-View-Controller), representando a camada responsável pelo acesso aos dados e pela lógica de negócios subjacente à aplicação. Em uma aplicação típica baseada em MVC, os modelos são encarregados de gerenciar os dados da aplicação e as regras de negócios associadas a esses dados.
&nbsp;&nbsp;&nbsp;&nbsp;


Na arquitetura delineada anteriormente, foram desenvolvidos 5 modelos, correspondendo a cada controller definido. O primeiro modelo, denominado User, está associado ao controller User. Ele inclui os atributos ID, Role, Name e Password, que são essenciais para o cadastro e login dos usuários na aplicação. Esses atributos são diretamente relacionados às operações de acesso ao banco de dados quando ocorrem tais eventos, permitindo o funcionamento adequado da aplicação.
&nbsp;&nbsp;&nbsp;&nbsp;

Em seguida, os models para acesso aos dados dos formulários são implementados, exibindo atributos como ID, Name e Answer. Esses atributos desempenham um papel crucial na persistência das respostas dos usuários e na identificação do usuário correspondente. Ao armazenar essas informações, os modelos garantem a integridade e rastreabilidade das respostas fornecidas pelos usuários nos formulários.
&nbsp;&nbsp;&nbsp;&nbsp;

No final da lista de models, temos o controller Admin, que possibilita ao administrador acessar, por meio de sua página no sistema de administração, as tabelas e gráficos contendo os dados da pesquisa. Este controller é responsável por coordenar a apresentação dos dados de forma organizada e compreensível para o administrador, permitindo uma análise eficaz dos resultados da pesquisa.

# <a name="c1"></a> Infraestrutura
&nbsp;&nbsp;&nbsp;&nbsp;
O projeto utiliza um banco de dados PostgreSQL para armazenar informações cruciais, como os dados dos usuários, respostas dos formulários e outras informações relacionadas à pesquisa. Os controladores interagem com os modelos para acessar e manipular os dados conforme necessário, garantindo a aplicação adequada da lógica de negócios nos dados armazenados no banco de dados.
