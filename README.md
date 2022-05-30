# Desafio-Regulatory Ops
Desafio proposto pela Stone sobre conceitos e funcionalidades do PIX.

## **1. Conceitos fundamentais sobre PIX**

O PIX foi desenvolvido pelo Banco Central para ser um meio de pagamento amplo e prático. Onde os recursos são transferidos em poucos segundos, 24 horas por dia, 7 dias por semana.

Os potenciais relacionados ao PIX são inúmeros, e não a toa hoje __*19 meses*__ após o seu lançamento ele é considerado um sucesso. Pois tem a capacidade comprovada de alavancar a competitividade e eficiência nas formas de pagamento. Além de baixo custo, incentiva o pagamento eletrônico do mercado de pagamento do varejo. Sem mencionar o preenchimento de diversas lacunas existentes nas formas de pagamentos disponíveis à população.
O Pix nasceu para facilitar os métodos de compra para os consumidores e empresas.

### Suas principais características são:
* Rapidez
   * Transações concluídas em segundos e recursos disponíveis ao recebedor em tempo real.
* Barato
   * Grátis para pessoas físicas e baixo custo em outros casos.
* Facilidade e disponibilidade
   * Simples para o uso da população em geral. E disponível 24/7 inclusive em feriados.
* Aberto
   * O pagamento pode ser realizado entre instituições distintas.
* Versátil
   * Pode ser usado em diversas propostas, independente do tipo de pagamento ou valor da transação. Abrangendo pessoas. empresas e até mesmo o governo.
* Seguranca
   * Diversos mecanismos desenvolvidos para garantir a segurança das transações.
* Integrado
   * Disponibilidade de importantes informações para facilitar a automação de processos e a conciliação de pagamentos.

### Critérios para instituições possam participar do Pix
As IPs não sujeitas à autorização de funcionamento ou em processo de autorização de funcionamento pelo Banco Central do Brasil deverão:
- [x] aderir às regras, às condições e aos procedimentos estabelecidos no Regulamento;
- [x] possuir capacidade técnica e operacional para cumprir os deveres e as obrigações previstos no Regulamento;
- [x] possuir contrato firmado com participante responsável;
- [x] comprovar a integralização e a manutenção de, no mínimo, R$1.000.000,00 (um milhão de reais) de capital.

A participação no Pix é obrigatória para as instituições financeiras e para as instituições de pagamento autorizadas a funcionar pelo Banco Central do Brasil com mais de quinhentas mil contas de clientes ativas. Consideradas as contas de depósito à vista, as contas de depósito de poupança e as contas de pagamento pré-pagas.

## **2. Sistemas do Bacen responsáveis pelo PIX**

O Banco Central além de Regulador é também o Gestor das plataformas no âmbito do Pix. Pois é papel do mesmo promover as infraestruturas tecnológicas necessária para o funcionamento dos fluxos transacionais.

O Pix possui três interfaces:

* *DICT*
   * DICT é o Diretório de Identificadores de Contas Transacionais.
* *ICOM (Acesso ao SPI)*
   * ICOM é a interface ISO 20022 que da acesso ao SPI, Sistema de Pagamento Instantâneo, sendo esta a infraestrutura de liquidação.
* *ARQ*
    * ARQ esta é a interface usada para se fazer download de arquivos que são gerados pelo SPI (gerado a partir de mensagem) ou pelo DICT (gerado a partir requisição).

O ecossistema de pagamentos instantâneos formado pelo Bacen, Sistema Pagamentos Instantâneos (SPI), que faz a liquidação das transações realizadas entre diferentes instituições participantes de forma bruta e em tempo real, sem gerar exposição financeira entre os participantes, e também pelos prestadores de serviços de pagamento participantes do arranjo aberto instituído pelo BC. 
Foi desenvolvido também o operador e gestor da base de dados única e centralizada de endereçamento do ecossistema (DICT). Onde ficam armazenadas as informações das chaves que servem para identificar as contas transacionais dos usuários de forma fácil e simplificada.

Desta forma o Banco Central é responsável por desenvolver e gerenciar a base única e centralizada de endereçamento (DICT) e a infraestrutura única e centralizada de liquidação das transações (SPI), que funcionará 24 horas por dia, todos os dias do ano.


As partes dentro do ecossistema do Pix são divididas da seguinte forma:

* **Pagador:** quem paga ou transfere valores.
* **Beneficiário:** quem recebe o valor.
* **participantes diretos:** Instituições Financeiras que possuem contas no BACEN para liquidação.
* **Participantes Indiretos:** Fintechs, Contas de Pagamento e outros que NÃO possuem conta no BACEN.
* **Provedores de Serviços:** Softwares e instituições onde o usuário possui contas de pagamento.
* **Infraestrutura e liquidação:** O Sistemas de Pagamentos Instantâneo do Pix.

## **3. Principais Fluxos Transacionais**

As transações com o Pix serão realizadas principalmente a partir dos seguintes modelos:

* Chaves
* Códigos QR estáticos
* Códigos QR Dinâmicos
* Pix saque e Pix troco

A chave é o apelido dado a conta para que ela seja identificada dentro do Pix.
Está conta pode ter até 5 chaves caso seja de pessoa física. Para contas PJ podem ser usadas até 20 chaves diferentes. Desde que as chaves sejam diferentes para cada conta.

O processo de efetivação do Pix é definido em dois fluxos:
* Fluxo de geração de ordem de pagamento pelo usuário pagador;
   * Procedimentos executados pelo pagador para identificação do usuário recebedor.
* Fluxo de efetivação do Pix;
   * Iniciado pelo prestador de serviço de pagamento (PSP) do pagador, após a geração da ordem de pagamento.

Os códigos QR estáticos permitem que várias transações sejam realizadas a partir de um único código. Desse modo, é possível definir preços fixos para um produto ou mesmo deixar o pagador inserir um valor, o que é interessante para pequenas empresas, prestadores de serviço e pessoas físicas.

Já os códigos QR dinâmicos são exclusivos para cada transação, só podem ser utilizados uma vez, pelo menos em teoria. Além do valor, é possível inserir outras informações como a identificação do beneficiário, por exemplo.

Na prática o fluxo transacional por QR Code acontece da seguinte forma:

* O recebedor gera os QR Codes por meio do app do seu PSP;
* QR Code gerado mostra o nome da empresa geradora da cobrança e a PSP;
* APP conta digital do pagador;
* O cliente efetua o pagamento do QR code por meio do APP da sua conta digital;
* As informações do pagamento são enviadas pelo PSP do pagador e a transação é liquidada no SPI (Bacen)
* A PSP do recebedor recebe as informações da transação e disponibiliza o saldo para a empresa que envio a cobrança.

Na categoria de Pix Saque e Pix troco, o cliente poderá ter a opção de retirada de dinheiro em espécie diretamente no estabelecimento comercial. O dinheiro em espécie corresponderá ao valor da transação Pix realizada. Enquanto que no Pix Troco, o valor entregue será a diferença entre o valor total do Pix em relação ao valor da compra realizada no estabelecimento. Vale ressaltar que essa categoria de Pix é facultativa para os estabelecimentos comerciais e estão relacionadas diretamente as transações por QR Code. 

PIX | Disponível
---|---
Saque | QR estático ou dinâmico
Troco | QR dinâmico

Se o estabelecimento aceitar apenas chave Pix é necessário que este, verifique a integração para a geração de QR Code junto a instituição detentora da conta do estabelecimento para ajustar o contrato com a instituição (PSP) que realize o serviço facilitador de serviço de saque (FSS).

Resumidamente, o cliente pagador usa a interface de um PSP, para fazer pagamentos e transferências. Esse PSP vai recorrer ao DICT para encontrar os dados da chave informada ou seja, a agência, a conta, o dígito e outros dados importantes.
 
Em seguida, com as informações em mãos, o PSP do cliente pagador comunica ao Banco Central a intenção em fazer o Pix. Então, o SPI entra em cena para liquidar a transação e repassar o valor para a instituição do recebedor. Por fim, o PSP do recebedor valida os dados do destinatário e responde ao SPI se aceita ou não a transferência.

Embora pareça um processo extenso e complicado, tudo isso acontece em poucos segundos e o dinheiro cai na conta do recebedor no mesmo instante. 
Além da instantaneidade, encurtar o caminho que o dinheiro faz de uma conta até outra faz com que o custo de implementação seja menor. Isso torna o Pix mais econômico tanto para o banco, quanto para o usuário final.

* *Fluxo de Efetivação do Pix*
   * Fluxo de Transações entre participantes Diretos;
   * Fluxo de Transações entre participantes Indiretos;
   * Fluxo de Transações nos livros do PSP;
   * Fluxo de Transações entre participantes indiretos com mesmo liquidante.

*Por fim vale ressaltar as diferenças entre Pix com chave, Lendo QR code ou por meio de Indicação*

Há algumas situações em que a dinâmica com o serviço de iniciação oferece uma experiência mais simples ao usuário. Por exemplo, se você está usando um aplicativo para troca de mensagens ou para efetuar uma compra, é mais simples iniciar a transação diretamente nesse próprio aplicativo e já ser redirecionado ao app do seu banco apenas para autenticar a transação do que precisar abrir manualmente o aplicativo do banco, selecionar a opção Pix, selecionar a forma desejada (digitar a chave ou via Pix copia e cola) e só então autenticar a transação. Ou seja, é mais uma forma de fazer um Pix que pretende facilitar ainda mais a realização de pagamentos e transferências.

## **4. Qr-code dinâmico**

### **_Criação_**
---
O QR Code dinâmico é personalizável, ou seja, ele pode ser modificado. Podem ser adicionada as informações do produto, do cliente, definir vencimentos, aplicado acréscimo como juros ou até mesmo desconto para o cliente. Ele funciona como se fosse um boleto bancário. Ideal para identificar de onde vem o pagamento. 

A característica que define o QR Code dinâmico é sua flexibilidade. O QR Code dinâmico, em sua estrutura interna, é configurado com uma URL que é acessada no momento de sua leitura. Essa funcionalidade abre diversas possibilidades de uso, dado que as informações trazidas pela URL podem variar em função de diversos parâmetros, como nos exemplos supracitados. 

O QR Code dinâmico necessita de uma integração com alguma PSP. Vale ressaltar que esse serviço não é obrigatoriamente oferecidos pelos PSP. Desta forma também é possível implementar uma integração manualmente sendo configurado através do PHP. Logo esse Qr Code é gerado consumindo API do prestador de serviço de pagamento do recebedor. Diferente do QR Code estático que é gerado direto no software utilizado.

Para gerar esses QR code, o sistema de automação da empresa vai gerar o QR através da integração com a Pix API. Essa API é disponibilizada pelo banco onde a pessoa recebe o Pix. A Pix API é padronizada pelo BACEN, permite a criação de QR code dinâmico individual ou em lote ajudando a verificar o recebimento de todos os QR codes, e ainda suporte em processos de devolução. Uma das grandes vantagens dessa API é que ela não te deixa amarrada a nenhum Banco, caso o usuário queira mudar o recebimento para outra instituição o API será a mesma. Não precisando adaptar o sistema para outra API.

Para *criar a integracao* com a PSP é necessário acessar o repositório Pix API no github do Banco Central (inserir link). Para se ter acesso a especificação do API Pix. Garantindo assim um padrão entre todos os PSP.

* Dados para criação do QR Code
   * URL base do PSP
   * Client ID e Client Secret (Autenticação ou autorização Alf 2 dentro da API do Pix)
   * Certificado TLS 1.2 ou superior (Emitido pelo PSP para assinar as requisições e manter o acordo de segurança exigido pelo BC)
   * Chave Pix cadastrada no PSP (Qualquer chave)

Desta forma com esses dados em mãos o programador devera criar uma classe dentro do PSP, para gerenciar a comunicação com o API Pix. Para que as cobranças esteja de acordo com a documentação presente no repositório do BACEN no github (inserir link), e o recurso a ser utilizado esta na área da CobPayload, Cob, put / Cob/ Txid.

Para efeito de ilustração segue a baixo a pagina onde se localiza o recurso citado.


   ![Imagem COB 5](https://user-images.githubusercontent.com/105951194/170846805-8555981a-f970-4a28-8e8f-1b94f5cdcb71.png)

### **_Fluxo de pagamento e recebimento_**
---

1. O usuário pagador, ao realizar a compra, informa que deseja pagar com Pix; 
1. O software de automação utilizado pelo usuário recebedor acessa a API Pix para criação de uma cobrança e, com os dados recebidos como resposta, gera um QR Code Dinâmico, que é apresentado em um dispositivo de exibição qualquer:
   1. em uma compra presencial, tipicamente uma tela próxima ao caixa ou mesmo um POS;
   2. nas compras online, no dispositivo em uso pelo pagador. 
3. O usuário pagador lê, a seguir, o QR Code com o App do seu PSP e efetua o pagamento; 
4. O usuário recebedor, de forma automatizada, por meio de nova consulta à API Pix, verifica se o pagamento foi realizado;
5. O usuário recebedor libera os produtos para o usuário pagador ou, no caso das compras online, confirma o recebimento do pagamento. 

Para apresentar visualmente o processo supracitado segue a ilustracao.

![fluxo na API de recebimentos ](https://user-images.githubusercontent.com/105951194/170847025-922ced02-55a7-48a9-a41f-6eaeff3ce0a3.png)

## **5. Principais regulamentações e seus pontos mais relevantes**

Por meio da [RESOLUÇÃO BCB Nº 1, DE 12 DE AGOSTO DE 2020](https://www.in.gov.br/en/web/dou/-/resolucao-bcb-n-1-de-12-de-agosto-de-2020-271965371), o BC estabelece a criação de vários manuais técnicos, os quais complementam a regulamentação do PIX e organiza o ecossistema brasileiro de pagamentos instantâneos em quatro estruturas:

1. a plataforma PIX;
2. o provedor responsável por liquidar as transações realizadas entre diferentes instituições participantes do SPI;
3. o diretório de identificadores de contas transacionais (DICT), que armazenará as informações das chaves PIX e dos dispositivos que identificarão as contas dos usuários recebedores;
4. as instituições prestadoras de serviços de pagamento do arranjo.

Através desta resolução ficam definidas as bases normativas para a regulamentacão do Pix em todo território nacional. São determinados os arranjos de pagamento, o regulamento que disciplina o seu funcionamento, as normas e as obrigatoriedade para participação do Pix, os processos e estruturas de governança a serem garantidas, o Fórum Pix e a instituição do DICT.

Porém além das normas contidas na Resolução citada compõem o regulamento do Pix os seguintes Manuais:

* Manual de Uso da Marca;
* Manual de Padrões para Iniciação do Pix;
* Manual de Fluxos do Processo de Efetivação do Pix;
* Requisitos Mínimos para a Experiência do Usuário;
* Manual de Redes do SFN;
* Manual de Segurança do SFN;
* Catálogo de Serviços do SFN;
* Manual das Interfaces de Comunicação;
* Manual de Tempos do Pix;
* Manual Operacional do DICT;
* Manual de Resolução de Disputas; 
* Manual de Penalidades.

Desta forma, vale ressaltar, que todos os Manuais tem sua importância determinada para o funcionamento do Pix de forma padronizada e qualitativa. Tendo em vista que sem eles poderia se criar um terreno fértil de possibilidades para fraudes e diversas funcionalidades escusas inerentes a operação que se propõem a criação do Pix.

Entretanto alguns manuais e regulamentações são mais importantes por possuir pontos mais relevantes. Entre eles estão:

>   * O Manual de Uso da Marca. Onde se regula a forma de uso da Marca pix em um padrão normativo pré estabelecido para trazer orientações para o uso coerente e consistente da marca Pix e seus elementos visuais. Para garantir a construção da personalidade e da experiencia Pix na mente de todos os usuários.
>
>   * Outro ponto de extrema importância é o Manual de Padrões para a iniciação do Pix. Por ser através dele que teremos as informações necessárias para a Iniciação do pagamento por Pix. Seja ela a forma que o usuário for usar. Estão presentes neste documentos os termos e parâmetros técnicos para determinar a funcionalidade das transações realizadas pelo Pix. Determina ainda os conceitos de negócio do API Pix. Os Casos de uso para cada forma de pagamento seja QR Code Estático ou Dinâmico, devolução ou remoção/alteração de cobrança. Contém ainda as Especificações técnicas de protocolos e tecnologias envolvidas, os requisitos e recomendações de segurança visando boas praticas de segurança para garantir o pleno funcionamento e desenvolvimento da API Pix.
> 
>    * O conhecimento do Manual de Fluxo do Processo de Efetivação é outro ponto que vale ser ressaltado. Contendo nele os processos de efetivação do Pix e seus procedimentos a serem realizados. Como o Fluxo de Geração da ordem de pagamento pelo usuário. O Fluxo de efetivação e devolução do pix entre participantes diretos ou indiretos. 
> 
>   * Requisitos Mínimos para Experiencia do usuário tem o objetivo de estabelecer critérios a experiencia em transações usando Pix. O conteúdo deste manual tem como objeto principal pessoas físicas, haja vista ser um público mais sensível à padronização de experiência em aplicativos, principalmente os smartphones, por serem o principal canal de acesso aos usuários do Pix.
> 
>    * Manual operacional do DICT, recai uma grande importância por ser o local onde ficam armazenadas as bases de dados de endereçamento, Chaves pix e demais informações necessárias para as transações entre usuários. Regula ainda como sera feita o fluxo de notificações, exclusão, portabilidade, reivindicação de pose, alteração de dados, consultas, verificação de sincronismo e segurança das chaves Pix.

Ainda relevante quanto a questão de segurança.O Bacen divulgou um manual, com os requisitos básicos que as instituições financeiras e demais participantes precisam seguir.
Este manual mostra duas medidas de segurança principais que os participantes precisam seguir de modo a evitar fraudes e proteger as transações e os dados dos usuários: a criptografia e a autenticação.

* **Criptografia** – é um método de proteção e privacidade que codifica uma informação de modo que só o emissor e o receptor consigam decifrá-la
* **Autenticação** – é o processo de reconhecimento da identidade de um usuário.

Em consequencia desta, sabemos que as instituições financeiras que participarem do Pix deverão obrigatoriamente possuir sistemas de segurança adequados às orientações do Bacen para proteger a privacidade e os dados dos clientes. 

## **6. Finalidade da Conta Pagamento Instantâneo**

O Sistema de Pagamentos Instantâneos é a infraestrutura centralizada e única para liquidação de pagamentos entre instituições distintas no território nacional brasileiro. 
O SPI faz a liquidação bruta e em tempo real de cada transação instantânea, os pagamentos são liquidados com lançamentos em contas de propósito específico que as instituições participantes diretos do sistema mantem no BC. Tais contas são denominadas Contas PI. Vale ressaltar que as transações são irrevogáveis e não se aceita lançamentos descoberto, desta forma as Contas PI não podem ter saldo negativo.

Tendo em vista que o BACEN tem principalmente dois grandes sistemas que participam do ecossistema de pagamentos instantâneos: SPI e DICT Cada um com sua responsabilidade pre definida, realizam um papel chave para o funcionamento geral das transações instantâneas no Brasil. 
Logo a Finalidade  da SPI é garantir a comunicação entre as PSP e os sistemas operados pelo BCB através da Rede Do Sistema Financeiro Nacional (RSFN) para que através desta as PSP tenham acesso ao DICT de forma direta ou indireta para garantir o pleno funcionamento do Pix em todo Brasil.

![IMAGEM PARTICIPA SPI](https://user-images.githubusercontent.com/105951194/170847706-caa1b791-cd45-4452-af18-3f4ef3f5e7ab.png)

O STR é onde acontece a liquidação final de todas as operações que são transacionadas pelas instituições financeiras. Ele é responsável pela transferencias de fundos com liquidação bruta em tempo real. É nesse sistema que acontece a transferencia de balanço entre os bancos. O Sistema de Transferencia de Reserva é considerado o coração do Sistema Brasileiro de Pagamentos, por ser onde ocorre a liquidação final de todas as obrigações financeiras no Brasil.

Desta forma sem a existência da STR não seria possível realizar nenhuma operação de credito através do pagamento instantâneo. Pois é nele que as contas de reservas bancarias tem sua liquidação final na operação transacional de credito.

O Conselho Monetário Nacional (CMN) autorizou o BC a conceder linha de redesconto às instituições financeiras participantes diretas do SPI. São operações de compra com compromisso de revenda de títulos públicos federais registrados no Sistema Especial de Liquidação e de Custódia (Selic), com instituições financeiras participantes diretas do SPI, titulares de Conta Pagamentos Instantâneos (Conta PI).

O objetivo é ofertar liquidez fora do horário de operações do Sistema de Transferência de Reservas (STR), minimizando o risco de insuficiência de recursos para os participantes. Desta forma os recursos serão liberados diretamente na conta específica para o pagamento instantâneo aos participantes do Pix, logo após o fechamento diário do STR. Fato este que garante ainda um dos conceitos fundamentais do Pix, que é estar disponível 24 horas por dia, 7 dias por semana.

O acesso ao STR é feito por meio da Rede do Sistema Financeiro Nacional (RSFN) ou pela Internet. Os detentores de conta Reservas Bancárias e as câmaras e prestadores de serviços de compensação e de liquidação devem obrigatoriamente acessar o STR por meio da RSFN, e os demais podem optar entre as duas formas de acesso.

![ESTRUTURA DO STR](https://user-images.githubusercontent.com/105951194/170847736-f5e8d78a-c197-430f-b7d4-fc0b631d3e39.png)

A relação da Conta Pagamento Instantâneo com as contas correspondente a Moeda Eletrônica se faz através de mensagem do Grupo de Serviços (SME) pelas instituições participantes do STR acontece por meio da Rede do Sistema Financeiro Nacional (RSFN) ou pela internet, utilizando o aplicativo STR-Web. Para a movimentação de recursos correspondente a Moeda Eletrônica. Pois é através desse sistema que se permite o pagamento ao usuário final. 

Assim, as liquidações de operações no STR é realizada por meio de lançamentos na conta participante mantida no BC. Logo essa conta pode ser de dois tipos:
		
* Reservas Bancarias
* Conta de Liquidação

A Conta de Liquidação obrigatória, para câmaras e prestadores de serviços de compensação e de liquidação responsáveis por sistemas de liquidação considerados sistemicamente importantes e facultativa, para as demais câmaras e prestadores de serviços de compensação e de liquidação e para as instituições autorizadas a funcionar pelo Banco Central do Brasil.

Desta forma a relação principal das contas de pagamento instantâneo com a conta de liquidação ocorre por ser através dela que se realiza a Movimentação de Recursos entre o Banco Central e os as contas de Reserva Bancarias ou de Conta de Liquidação é realizada de forma exclusiva entre elas.




