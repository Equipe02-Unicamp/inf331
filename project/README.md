# Projeto `Advanced Store`

# Equipe 2
* Caroline Augusti
* Felipe Emygdio de Salles
* Gustavo Porto Guedes
* Luan Neves Silva
* Paulo Mellin Gimenes
* Thiago Natanael


# Nível 1

## 1. Componente Cadastro Usuário (Roxo): 
Este componente tem o intuito de verificar se o usuário possui um cadastro registrado no sistema do Marketplace. Se o usuário possuir cadastro, os dados do usuário serão encaminhados para o componente Login. Se o usuário não possuir cadastro, o componente irá encaminhá-lo para realizar um novo cadastro no sistema.
	Para realizar um novo cadastro, deve-se, primeiramente, escolher qual será o tipo de cadastro, ou seja, se será um cadastro administrativo, de lojista ou de cliente. Em seguida, irá abrir uma interface com os campos de autenticação e verificação respectivos a escolha realizada. 
Para ser administrador do sistema, por exemplo, é preciso ter a autorização do owner e um código de identificação para liberar o acesso, além dos outros campos a serem preenchidos. Já para ser lojista do marketplace é preciso de um CNPJ em caso de loja registrada ou de um CPF em caso de ser pessoa física, por exemplo.
Em resumo, cada tipo de cadastro deverá ter todos os seus campos verificados de acordo com a forma de preenchimento estabelecida pelo sistema, e validados para garantir a autenticidade das informações.
Por questão de segurança, todos os usuários deverão escolher uma senha contendo as seguintes orientações: pelo menos uma letra maiúscula, pelo menos uma letra minúscula, pelo menos um número, e pelo menos 8 caracteres. Além disso, o usuário deverá escolher uma pergunta-chave e inserir a resposta correta e a qual irá se recordar no futuro. Esta pergunta-chave seja utilizada caso seja necessário registrar uma nova senha.
Assim que todos os dados forem validados e registrados, uma notificação será enviada através do e-mail cadastrado pelo usuário para confirmar seu acesso, e permitir sua entrada no sistema.

## 2. Componente Login (Rosa):
	Os dados do usuário armazenados no sistema serão enviados a este componente para que quando ele inserir seu login (e-mail)  e sua senha, o sistema do marketplace possa confirmar se os códigos de acesso estão corretos, e assim permitir a entrada no sistema. 
Entretanto, caso os dados estejam incorretos, o usuário será notificado que há incompatibilidade entre o código de acesso inserido com o registrado, e pode vir a realizar outras tentativas ou recuperar o acesso através do registro de uma nova senha.
Para recuperar o acesso, o usuário irá ser direcionado a outra interface e nela inserir o e-mail cadastrado no campo solicitado. Caso este e-mail não esteja cadastrado no sistema, uma notificação irá ser apresentada ao usuário. Caso contrário, um link do sistema será enviado ao e-mail com o assunto “recuperação de acesso”. O usuário pode inserir a última senha de que se recorde, ou responder a pergunta-chave. Em ambas as opções, se o campo for preenchido corretamente, o sistema do marketplace irá permitir o registro de uma nova senha, a qual será utilizada posteriormente para realizar um novo login.

## 3. Componente Perfil Acesso (Verde):
	Após a confirmação de permissão do sistema, este componente irá redirecionar o usuário de acordo com seu perfil, ou seja, se o usuário for administrador, ele irá ser direcionado para a interface de visualização administrativa do sistema, o mesmo ocorre para os perfis de lojista e cliente, ao serem redirecionados às interfaces de seus perfis de cadastro.

## 4. Componente DashBoard Administrador (Azul):
	Este componente representa o gerenciamento realizado pelo administrador. 
O administrador tem permissão para gerenciar os lojistas, fornecedores e/ou parceiros, através de seus dados, seus históricos de vendas e de interações com os clientes, a fim de proporcionar aos usuários uma melhor experiência. Dentre as informações disponíveis dos lojistas, pode-se citar  a quantidade de vendas entregues dentro do prazo, média de preços praticados, localização geográfica e alcance da entrega, facilidade na resolução de problemas, entre outras. Estas informações auxiliam os administradores a decidirem quem deve ser mantido e recomendado aos clientes.
Além disso, o administrador auxilia no desenvolvimento e na estabilidade do sistema, promovendo funcionalidades para que os lojistas e os clientes acompanhem seus pedidos em aberto e entregues, gerencie seus perfis, interagem entre si e registrem todas as operações realizadas em um banco de dados para armazenar os dados e possibilitar a auditoria do sistema.
O administrador também é responsável por assegurar a confiabilidade, segurança e privacidade do sistema do marketplace, pois é fundamental que as transações financeiras efetuadas pelo site, assim como os dados pessoais dos usuários estejam seguros e restritos.

## 5. Componente DashBoard Cliente (Azul Claro):
	Este componente representa o gerenciamento realizado pelo cliente.
	O cliente pode gerenciar seus pedidos em aberto e entregues, seus dados pessoais, como endereço e dados para pagamento, e suas interações com os fornecedores como solicitações de informações, negociações e feedbacks.

## 6. Componente DashBoard Lojista (Laranja Claro):
	Este componente representa o gerenciamento realizado pelo lojista.
	O lojista, fornecedor e/ou parceiro pode, de modo geral, gerenciar suas vendas, seus produtos e seus pedidos abertos e entregues. Exemplos de informações disponíveis são a quantidade de vendas entregues dentro do prazo, quanto dos valores financeiros que serão repassados de seus produtos, média de preços praticados, localização geográfica e alcance da entrega, facilidade na resolução de problemas, entre outras.
	Além disso, ele também poderá acompanhar seus produtos vendidos e entregues, e suas interações com os clientes, como feedbacks e dúvidas relacionadas às informações adicionais ou técnicas do produto, por exemplo.
	Já o gerenciamento de produto é fundamental, pois os lojistas são responsáveis pela disponibilização e manutenção das informações dos produtos comercializados, tais como, quantidade em estoque, preços, tamanhos, fotografias, entre outras.

## 7. Componente Cadastro Produto (Amarelo Claro):
	Este componente representa o registro de um novo produto através do fornecedor, ou lojista. Para cadastrar um novo produto é preciso assegurar que ele está contido na lista dos produtos permitidos a serem comercializados dentro do marketplace.
	Após a seleção e confirmação do tipo de produto, será preciso preencher os campos disponíveis de acordo com a orientação pré-estabelecida através dos comentários de cada um dos campos, como, por exemplo, a imagem deve ser de boa qualidade, os campos de preço aceitarem apenas números, ter um limite de caracteres que podem ser utilizados nos campos de texto, e assim em diante.
	O sistema irá calcular as taxas e os valores financeiros que poderão ser repassados ao fornecedor caso o produto tenha a venda bem-sucedida. Após estes critérios, o produto será cadastrado ao sistema, uma notificação será apresentada ao usuário e o produto irá ser adicionado à sua lista de produtos para gerenciar seu desempenho.

## 8. Componente Filtro Produto (Verde Claro):
  Este componente permite que o usuário busque pelo produto desejado através da barra de busca da interface. O cliente pode comprar produtos como em uma loja virtual tradicional, porém podendo escolher entre diferentes lojas/fornecedores.
	Uma listagem inicial será apresentada ao usuário através do método de “leilão invertido”, o qual irá apresentar os produtos mais recomendados ordenados pelo menor preço. O cliente poderá, posteriormente, optar por selecionar um dos produtos para averiguar melhor suas informações ou selecionar um ou mais dos outros filtros disponíveis pelo sistema.
	Além do “leilão invertido”, o sistema toma como base os históricos do cliente e dos fornecedores do produto solicitado, como localidade para determinar o alcance disponível de entrega, a classificação do produto e do fornecedor, feedbacks apresentados por outros usuários que já compraram este produto, entre outros atributos. Estas informações também estarão disponíveis para que o cliente possa consultar antes de realizar a compra, com o intuito de proporcionar uma melhor experiência.
	Assim que o cliente selecionar um ou mais produtos desejados para compra, eles serão armazenados no carrinho de compras, até que o usuário decida realizar e finalizar o pedido, ou excluir os produtos.

## 9. Componente Checkout (Laranja):
Este componente irá buscar os produtos presentes no carrinho para realizar o processo de pedido de compra.
O sistema irá buscar pela lista de produtos, e estruturar o pedido de compra, ao mesmo tempo em que verifica e captura os dados do usuário. O usuário deverá preencher e confirmar todos os campos do pedido.
O sistema irá verificar os dados bancários e os de endereço para garantir, respectivamente, que sejam dados de uma conta bancária válida, e enviem o produto e/ou a cobrança para o endereço correto. Caso os dados estão incorretos ou inválidos, uma mensagem será exibida ao usuário para que ele confirme novamente os dados, ou insira outros.
	Quando todos os campos estiverem preenchidos e validados, a confirmação do pedido será exibida na interface do usuário e ainda será enviada ao e-mail cadastrado. Caso o usuário tenha escolhido “boleto” como forma de pagamento, ele poderá optar por abrir o boleto na tela, enviar para o e-mail ou imprimir. O pedido só será confirmado quando o pagamento for realizado e concluído com sucesso dentro do período estimado pelo boleto ou cartão. Caso contrário, o pedido será cancelado.

## 10. Componente Acompanhamento (Cinza):
  Este componente é responsável pelo procedimento após a confirmação do pedido.
  O pedido será enviado ao fornecedor, o qual deverá retirar o produto do estoque e enviar ao usuário, gerando por meio disto um código de rastreio do pacote para que o cliente possa acompanhar seu novo produto até seu endereço.
	O código será enviado para o e-mail do cliente, o qual será notificado de toda e qualquer atualização referente ao status de seu produto. Embora ele ainda possa consultar manualmente o trajeto através do sistema do marketplace.
	Assim que o produto for entregue, o cliente receberá no e-mail, alguns dias depois, a opção de registrar seu feedback do fornecedor e do produto no marketplace, como elogios, críticas e/ou sugestões. Este comentário será registrado e armazenado para que outros clientes possam utilizar como referência no momento de sua compra.
	Caso o usuário queira devolver ou trocar o produto, ele deverá preencher um formulário justificando o motivo da devolução, para que o fornecedor esteja validando a razão e assim tomar as medidas necessárias. Em caso de discordância entre o fornecedor e o cliente, o administrador do sistema pode e deve interferir e trabalhar como mediador para resolver a situação da melhor maneira.

## 11. Componente Chat (Amarelo):
  Este componente representa a interação entre os usuários do marketplace. Em outras palavras, ele possibilita que o cliente tenha uma interface para se comunicar diretamente com o fornecedor ou representante da loja do produto desejado. 
  Por meio deste chat, é possível obter respostas a dúvidas técnicas, ou adicionais do produto, solicitar negociações ou descontos especiais, por parcerias ou cupons e até mesmo elogiar, criticar ou sugerir alguma mudança em relação ao atendimento.
  O fornecedor por sua vez pode realizar e concluir o pedido do cliente, solicitando seus dados e os preenchendo nos campos correspondente, aplicando descontos ou adicionando novas funcionalidades ao produto, caso seja do desejo do cliente. 

## 12. Componente Leilão Invertido (Barramento):
  Este componente irá receber o produto buscado pelo cliente, assim como seu histórico de compras e dados pessoais, como localidade (endereço), pacote escolhido pelo usuário durante o cadastro, ou ao longo do tempo de utilização da plataforma, para que assim ele possa gerar o dado completo de busca e enviar ao barramento.

## 13. Componente Lojistas (Barramento):
  Este componente irá receber a lista de produtos e os dados históricos de cada lojista, fornecedor e/ou parceiro. Por meio do produto desejado pelo cliente, o componente irá  listar os fornecedores que possuem o produto e são melhor indicados de acordo com seus dados históricos.
	Esta lista de fornecedores será enviado ao barramento contendo o produto, a descrição, o preço e outras informações que ajudaram o cliente a tomar a melhor decisão para ele.

## 14. Componente Rankeamento (Barramento):
  Este componente será responsável por ranquear as melhores escolhas de fornecedores e seus produtos e listá-las na interface do usuário. Lembrando de que este ranqueamento se trata da filtragem inicial e comum a todos as buscas realizadas no sistema.
	Levando em consideração o procedimento de leilão invertido, o componente irá capturar a lista de fornecedores que possuem o produto, e classificá-las do menor preço ao maior preço. Entretanto, o sistema também irá utilizar como base as informações específicas de uma compra como a forma de pagamento e o endereço de entrega do usuário. Além disso, pode utilizar o histórico dos fornecedores para auxiliar na definição de classes de parceiros/fornecedores diferenciadas, onde parceiros em classes mais altas podem ter vantagens ou prioridade na recomendação, por exemplo.
  Em resumo, o ranqueamento irá classificar os produtos do menor ao maior preço, ao mesmo tempo que ele também irá considerar os históricos dos fornecedores, assim como os dados de pagamento e frete do cliente. 
  Com isso, este componente possibilita um processo de compra mais eficiente, pois evita o cliente de precisar buscar tão a fundo o produto desejado, o que poderia ocasionar na perda de interesse do produto ou da plataforma. Além de também disponibilizar os produtos mais adequados de acordo com o perfil de cada usuário.



Componente de Checkout




## Diagrama Geral do Nível 1

Apresente um diagrama conforme o modelo a seguir:

> ![Modelo de diagrama no nível 1](images/coreografia.png)

### Detalhamento da interação de componentes

O detalhamento deve seguir um formato de acordo com o exemplo a seguir:

* O `componente X` inicia o leilão publicando no barramento a mensagem de tópico "`leilão/<número>/início`" através da interface `Gerente Leilão`, iniciando um leilão.
* O `componente Y` assina no barramento mensagens de tópico "`leilão/+/início`" através da interface `Participa Leilão`. Quando recebe uma mensagem…

Para cada componente será apresentado um documento conforme o modelo a seguir:

## Componente `<Nome do Componente>`

> <Resumo do papel do componente e serviços que ele oferece.>

![Componente](diagrama-componente-mensagens.png)

**Interfaces**
> * Listagem das interfaces do componente.

As interfaces listadas são detalhadas a seguir:

## Detalhamento das Interfaces

### Interface `<nome da interface>`

> Resumo do papel da interface.

**Tópico**: `<tópico que a respectiva interface assina ou publica>`

Classes que representam objetos JSON associados às mensagens da interface:

![Diagrama Classes REST](images/diagrama-classes-rest.png)

~~~json
<Formato da mensagem JSON associada ao objeto enviado/recebido por essa interface.>
~~~

Detalhamento da mensagem JSON:

Atributo | Descrição
-------| --------
`<nome do atributo>` | `<objetivo do atributo>`

## Exemplo

### Interface DadosPedido

Interface para envio de dados do pedido com itens associados.

**Tópico**: `pedido/{id}/dados`

Classes que representam objetos JSON associados às mensagens da interface:

![Diagrama Classes REST](images/diagrama-classes-rest.png)

~~~json
{
  "number": 16,
  "duoDate": "2009-10-04",
  "total": 1937.01,
  "items": {
    "item": {
       "itemid": "1245",
       "quantity": 1
    },
    "item": {
       "itemid": "1321",
       "quantity": 1
    }
  }  
}
~~~

Detalhamento da mensagem JSON:

**Order**
Atributo | Descrição
-------| --------
number | número do pedido
duoDate | data de vencimento
total | valor total do pedido
items | itens do pedido

**Item**
Atributo | Descrição
-------| --------
itemid | identificador do item
quantity | quantidade do item

# Nível 2

Apresente aqui o detalhamento do Nível 2 conforme detalhado na especificação com, no mínimo, as seguintes subseções:

## Diagrama do Nível 2

Apresente um diagrama conforme o modelo a seguir:

> ![Modelo de diagrama no nível 2](images/diagrama-subcomponentes.png)

### Detalhamento da interação de componentes

O detalhamento deve seguir um formato de acordo com o exemplo a seguir:

* O componente `Entrega Pedido Compra` assina no barramento mensagens de tópico "`pedido/+/entrega`" através da interface `Solicita Entrega`.
  * Ao receber uma mensagem de tópico "`pedido/+/entrega`", dispara o início da entrega de um conjunto de produtos.
* Os componentes `Solicita Estoque` e `Solicita Compra` se comunicam com componentes externos pelo barramento:
  * Para consultar o estoque, o componente `Solicita Estoque` publica no barramento uma mensagem de tópico "`produto/<id>/estoque/consulta`" através da interface `Consulta Estoque` e assina mensagens de tópico "`produto/<id>/estoque/status`" através da interface `Posição Estoque` que retorna a disponibilidade do produto.

Para cada componente será apresentado um documento conforme o modelo a seguir:

## Componente `<Nome do Componente>`

> <Resumo do papel do componente e serviços que ele oferece.>

![Componente](images/diagrama-componente.png)

**Interfaces**
> * Listagem das interfaces do componente.

As interfaces listadas são detalhadas a seguir:

## Detalhamento das Interfaces

### Interface `<nome da interface>`

> ![Diagrama da Interface](images/diagrama-interface-itableproducer.png)

> <Resumo do papel da interface.>

Método | Objetivo
-------| --------
`<id do método>` | `<objetivo do método e descrição dos parâmetros>`

## Exemplos:

### Interface `ITableProducer`

![Diagrama da Interface](images/diagrama-interface-itableproducer.png)

Interface provida por qualquer fonte de dados que os forneça na forma de uma tabela.

Método | Objetivo
-------| --------
`requestAttributes` | Retorna um vetor com o nome de todos os atributos (colunas) da tabela.
`requestInstances` | Retorna uma matriz em que cada linha representa uma instância e cada coluna o valor do respectivo atributo (a ordem dos atributos é a mesma daquela fornecida por `requestAttributes`.

### Interface `IDataSetProperties`

![Diagrama da Interface](images/diagrama-interface-idatasetproperties.png)

Define o recurso (usualmente o caminho para um arquivo em disco) que é a fonte de dados.

Método | Objetivo
-------| --------
`getDataSource` | Retorna o caminho da fonte de dados.
`setDataSource` | Define o caminho da fonte de dados, informado através do parâmetro `dataSource`.

# Multiplas Interfaces

> Escreva um texto detalhando como seus componentes  podem ser preparados para que seja possível trocar de interface apenas trocando o componente View e mantendo o Model e Controller.
>
> É recomendado a inserção de, pelo menos, um diagrama que deve ser descrito no texto. O formato do diagrama é livre e deve ilustrar a arquitetura proposta.
