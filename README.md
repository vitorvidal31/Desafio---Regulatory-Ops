# Desafio-Regulatory Ops
Desafio proposto pela Stone sobre conceitos e funcionalidades do PIX

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

### Critérios para instituicoes possam participar do Pix
As IPs não sujeitas à autorização de funcionamento ou em processo de autorização de funcionamento pelo Banco Central do Brasil deverão:
- [x] aderir às regras, às condições e aos procedimentos estabelecidos no Regulamento;
- [x] possuir capacidade técnica e operacional para cumprir os deveres e as obrigações previstos no Regulamento;
- [x] possuir contrato firmado com participante responsável;
- [x] comprovar a integralização e a manutenção de, no mínimo, R$1.000.000,00 (um milhão de reais) de capital.

A participação no Pix é obrigatória para as instituições financeiras e para as instituições de pagamento autorizadas a funcionar pelo Banco Central do Brasil com mais de quinhentas mil contas de clientes ativas. Consideradas as contas de depósito à vista, as contas de depósito de poupança e as contas de pagamento pré-pagas.

## **2. Sistemas do Bacen responsáveis pelo PIX.**

O Banco Central além de Regulador é também o Gestor das plataformas no âmbito do Pix. Pois é papel do mesmo promover as infraestruturas tecnológicas necessária para o funcionamento dos fluxos transacionais.

O Pix possui três interfaces:

* *DICT*
   * DICT é o Diretório de Identificadores de Contas Transacionais.
* *ICOM (Acesso ao SPI)*
   * ICOM é a interface ISO 20022 que da acesso ao SPI, significa Sistema de Pagamento Instantâneo, sendo esta a infraestrutura de liquidação.
* *ARQ*
    * ARQ esta é a interface usada para se fazer download de arquivos que são gerados pelo SPI (gerado a partir de mensagem) ou pelo DICT (gerado a partir requisição).

O ecossistema de pagamentos instantâneos é formado pelo Bacen, pelo Sistema Pagamentos Instantâneos (SPI), que faz a liquidação das transações realizadas entre diferentes instituições participantes de forma bruta e em tempo real, sem gerar exposição financeira entre os participantes, e também pelos prestadores de serviços de pagamento participantes do arranjo aberto instituído pelo BC. 
Foi desenvolvido também o operador e gestor da base de dados única e centralizada de endereçamento do ecossistema (DICT). Onde ficam armazenadas as informações das chaves que servem para identificar as contas transacionais dos usuários de forma fácil e simplificada.

Desta forma o Banco Central é responsável por desenvolver e gerenciar a base única e centralizada de endereçamento (DICT) e a infraestrutura única e centralizada de liquidação das transações (SPI), que funcionará 24 horas por dia, todos os dias do ano.


As partes dentro do ecossistema do Pix são divididas da seguinte forma:

* **Pagador:** quem paga ou transfere valores.
* **Beneficiário:** quem recebe o valor.
* **participantes diretos:** Instituições Financeiras que possuem contas no BACEN para liquidação.
* **Participantes Indiretos:** Fintechs, Contas de Pagamento e outros que NÃO possuem conta no BACEN.
* **Provedores de Serviços:** Softwares e instituições onde o usuário possui contas de pagamento.
* **Infraestrutura e liquidação:** O Sistemas de Pagamentos Instantâneo do Pix.

## **3.Principais Fluxos Transacionais**

As transações com o Pix serão realizadas principalmente a partir dos seguintes modelos:

* Chaves
* Códigos QR estáticos
* Códigos QR Dinâmicos
* Pix saque e Pix troco

A chave é o apelido dado a sua conta para que ela seja identificada dentro do Pix.
Sua conta pode até ter 5 chaves caso seja de pessoa física. Para contas PJ podem ser usadas até 20 chaves diferentes. Desde que as chaves sejam diferentes para cada conta.

O processo de efetivação do Pix é definido em dois fluxos:
* Fluxo de geração de ordem de pagamento pelo usuário pagador;
* Corresponde aos procedimentos executados pelo pagador para identificação do usuário recebedor.
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

Desta forma o fluxo de geração da ordem de pagamento pelo usuário pagador segue as seguintes modelos:


