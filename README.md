# <a name="c1"></a> Abandono Zero

# <a name="c1"></a>Descrição

&nbsp;&nbsp;&nbsp;&nbsp;
No contexto atual, o abandono de animais é uma questão alarmante que afeta comunidades em todo o mundo. Enquanto esforços significativos têm sido feitos para abordar esse problema, a falta de dados concretos sobre os motivos que levam os donos a abandonarem seus animais representa um desafio significativo. Compreender as razões por trás do abandono é fundamental para desenvolver estratégias eficazes de prevenção e intervenção. Este projeto busca preencher essa lacuna, explorando a relação entre a falta de dados sobre os motivos do abandono de animais e os próprios motivos do abandono. Ao fazê-lo, não apenas esperamos fornecer dados para informar políticas e programas de conscientização, mas também contribuir para a proteção e o bem-estar dos animais em nossas comunidades.

&nbsp;&nbsp;&nbsp;&nbsp;
Estamos criando um website com um questionário que terá como objetivo coletar dados de usuários que tem, tiveram ou terão cachorros. Esses dados serão armazenados e posteriormente utilizados pelo INSPA (Instituto de Psicologia Animal), que busca oferecer cursos de pós-graduação que focam no comportamento e bem-estar humano-animal, para entender melhor o contexto de abandonos de cachorros e dessa forma tomar medidas efetivas baseadas em dados para acabar com esse problema. 

# <a name="c1"></a>Ferramentas de Diagramação
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
Posteriormente, o sistema apresenta três visualizações destinadas a armazenar informações das diferentes perguntas nos formulários disponíveis no site. A primeira é designada para a primeira pergunta (Forms Screen), a segunda para a pergunta subsequente (Future Form Screen) e a terceira para a última pergunta (Last Form Screen). Estes formulários são compostos por um título principal (h1) contendo a questão, uma caixa de resposta, uma barra de progresso, um botão para avançar para a próxima pergunta e outro para retroceder para a pergunta anterior. Na página Last Form Screen, em vez de um botão para a próxima pergunta, há um botão para enviar as respostas.
&nbsp;&nbsp;&nbsp;&nbsp;
Por fim, há uma visualização denominada Forms Results, reservada aos administradores que possuem acesso aos resultados da pesquisa. Nesta visualização, os administradores podem visualizar as tabelas contendo os dados preenchidos pelos respondentes. A interface do Admin inclui gráficos para exibir os resultados, um botão de busca para encontrar resultados específicos, um botão de filtragem por região e um botão para ocultar os dados exibidos na tela.


