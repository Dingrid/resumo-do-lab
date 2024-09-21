![image](https://github.com/user-attachments/assets/3f23c185-d814-4979-83e3-09e60adaf51c)# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

# Introdução
-> Estou aprendendo sobre recursos básicos do Azure para tirar a certificação AZ-900.

A certificação AZ-900 é uma certificação introdutória que explora os recursos básicos da computação em nuvem. A computação em nuvem é o presente e é um recursos essencial para os desenvolvedores aprenderem.

# Tipos de nuvem
Essa certificação pede 3 tipos de nuvens:
1. Nuvem privada: Para só uma pessoa que opera os serviços dela mesmo.
2. Nuvem pública: + de uma organização na mesma nuvem, as empresas pagam apenas pelo oq utilizam
3. Nuvem híbrida: pública + privada: é o melhor dos 2 mundos, permite que use ambos os ambientes e coloque apps e infos nas 2.

# Benefícios Cloud
1 Alta disponibilidade ->
recurso sempre disponível, a disponibilidade 24/7 do serviço pode ficar de fora de acordo com o acordo (99%; 99,9%; 99.95% ou 99,99%). Se esse tempo for indisponível mais que o SLA então a Microsoft te dá um "voucher" que vc pode usar de desconto para sua próxima conta
SLA -> é um recurso da alta disponibilidade que garante determinados tempos de atividade conforme o tipo de serviço
SE O SERVIÇO FICAR DE FORA, NÃO HÁ O QUE FAZERMOS. BASTA ESPERAR

2 Escalabilidade ->
É a capacidade do sistema de adicionar recursos para se adequar a demanda (assim como reduzir recursos)

3 Elasticidade -> 
seus recursos podem ser implantados e expandidos (automaticamente ou manualmente) - BLACK FRIDAY
Ex: se o processamento passar para X % em X tempo então aumente em X% a capacidade o servidor

4 Confiabilidade ->
Sendo descentralizado (os servidores podem ser alocados em diversos locais do mundo), a confiabilidade da nuvem é ótimo e resiliente (elas se recupera das falhas e continua funcionando)

5 Previsibilidade -> 
Permite que avançe com confiança, sempre com sistemas disponíveis e aproveitando o melhor

6 Segurança -> 
A nuvem oferece segurança para implementação dq vc quiser. PORÉM A IMPLEMENTAÇÃO DAS PRÁTICAS SEGURAS NA SUA APLICAÇÃO NÃO É TRABALHO DA MICROSOFT
EX: Vc deve atualizar suas máquinas, instalar patches, etc.

7 Governança -> 
Há uma auditoria de nuvem que sinaliza oq está fora da padronização e oferece soluções para mitigação
Geralmente a área de governança cuida da de segurança (há sempre uma linha tênue entre elas)

8 Gerenciabilidade -> Há diversas opções de gerenciamento na computação em nuvem (ao decorrer iremos ver 2)
Gerenciar o seu ambiente de nuvem por meio do Portal ou linha de comando
Ex: Você pode escalar automaticamente a implantação de recursos com base na necessidade
Ex2: você pode implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual
Ex3: Você pode configurar usando APIs, powerShell ou o portal.

# SLA
-	Representa qual é o tempo aceitável que o seu serviço pode ficar fora.
-	Sempre estamos trabalhando com a possibilidade do serviço ficar indisponível. 
-	Quanto mais noves menos o serviço fica NOK.
-	Quanto mais você replica o dado em vários lugares então menos tempo de indisponibilidade você vai ter.


  # Tipos de serviço de nuvem
  - IaaS (Maior gestão): São serviços onde os clientes possuem mais acesso, eles atualizam as máquinas, setam os firewalls, etc

- PaaS (Gestão intermediária): Eu só me importo com a aplicação, e não com a máquina. 
Ex: Só quero saber do BD, não de qual é o SO da máquina que ele tá hospedado

- SaaS (Pouca gestão): A aplicação já existe, ela já tá pronta, eu já sei oq ele entrega e oq vai determinar oq eu vejo é a licença que eu adquiro. Os aplicativos SaaS também são chamados de softwares baseados na Web, softwares sob demanda ou softwares hospedados
Ex: Microsoft Teams, Office 365, e-mail, calendários, etc.

- Iaas -> PaaS -> SaaS (maior gestão -> menor gestão)

# REGIÕES
- As regiões são compostas de um ou mais datacenters muito próximos (sempre trabalhamos com a ideia de 3 datacenters)
- Nem todos os recursos estão disponíveis em todas as regiões
- As regiões preservam a residência dos dados com uma oferta abrangente (LGPD)
- Tem um mapa que dá pra saber onde estão as máquinas do azure
- Dependendo da onde você quer alocar, o custo muda
- A Microsoft tem regiões pelo mundo todo

- O delay ocorre quanto você aloca dois servidores em regiões distantes que dependem entre si.

- Diminuir a latência é uma responsabilidade da microsoft

# Backbone
- É uma rede exclusiva da Microsoft que estão interligadas entre si.

# Disaster Recovery
-> É ter uma réplica dos dados importantes em outra região, pra que quando o ambiente principal fique fora consigamos replicar ele em outro lugar


# Zona de disponibilidade
- É onde se tem uma série de pcs físicos que se comunicam no local
- Ela separa de forma física os datacenters dentro da mesma região, fazendo com que se um cair, o outro permaneça respondendo. (eles são independentes entre si)

  - Quanto mais disponibilidade mais caro
Para que se faça uma boa computação em nuvem deve-se pensar e fazer muitas perguntas


# PARES DE REGIÃO
- Toda região possui uma região par, essa região par é onde os serviços de disaster recovery são direcionados
- É ter sempre uma cópia do ambiente, para que se uma caia eu suba a outra
- Essa replicação pode ser automática para alguns serviços
- Deve-se ter no mínimo 300 milhas de separação entre os pares de regiões
- Quando se atualiza as regiões, as regiões são atualizadas sequencialmente para evitar indisponibilidade

# REGIÕES SOBERANAS DO AZURE
- São regiões exclusivas, que não estão disponíveis para clientes normais.
  
Ex: Há uma região soberana de serviços governamentais dos EUA (região governamental dos Estados unidos), onde é utilizada para serviço militar, ele é uma região a parte

Ex2: Há a Azure China, que é o primeiro provedor estrangeiro de serviços de nuvem pública da China, ela só fica disponível lá, é fisicamente separada e operada pela 21Vianet


# GRUPO DE RECURSOS
- É uma forma de se organizar as coisas (ex: grupo de recursos das máquinas, dos storages accounts, etc)
- É possível colocar recursos de regiões diferentes dentro de um grupo
- É possível aplicar regras para os grupos de recursos
- Os aplicativos podem consumir vários serviços em grupos de recursos distintos

# ASSINATURAS DO AZURE
- Quando se cria uma conta, ela tem uma única assinatura, porém você pode comprar outras.
  
Ex: Assinatura: do desenvolvimento, da produção, do teste

- UMA CONTA PODE TER DIVERSAS ASSINATURAS, MAS UMA ASSINATURA PERTENCE SOMENTE A UMA CONTA (N:1)
- Para cada assinatura se terá uma fatura diferente
- O dono da conta pode ter várias assinaturas, mas as assinaturas respondem para um único dono
- Com assinaturas, podemos restringir e dar permissões

# GRUPOS DE GERENCIAMENTO
- Através de um grupo de gerenciamento, é possível trabalhar padrões para mais de uma assinatura 
- Eles podem incluir várias assinaturas
- As assinaturas herdam as condições aplicadas ao grupo de gerenciamento

# SERVIÇOS DO AZURE
-	A certificação AZ-900 não exige que você saiba mexer nos apps, só exige que você saiba pra que eles servem

##	Área de trabalho virtual do Azure
- É uma virtualização da área de trabalho e aplicativos executada na nuvem
Ex: Ao invés de enviar um notebook pra empresa, você pode ipagar para a pessoa utilizar o dela e instalar uma área de trabalho lá
- Tem como criar um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway
- Implantações reais de várias sessões

##	Contêineres do Azure
- Eles fornecem um ambiente leve e virtualizado que não exige o gerenciamento do SO e pode responder a alterações sob demanda
- Ao invés de termos uma máquina que consome o servidor, criamos um container para reproduzir apenas uma rotina. Ele pode ser iniciado e interrompido a qualquer tempo

##	Instâncias de contêineres do Azure:
Ele possui instâncias, que é uma oferta da PaaS que executa um contêiner ou pod de contêineres no Azure

##	Aplicativos  de contêineres do Azure: 
É PaaS, que pode balancear a carga e escalar. (balanceamento de carga e escala = aplicativos)

##	Serviço de Kubernetes o Azure: 
É um serviço de orquestração para contêineres com arquiteturas distribuídas e grandes volumes de contêineres (gerencia o ciclo de vida deles)

##	Azure functions: 
PaaS, ela dá suporte a operações de computação sem servidor, o código dela é baseada em eventos, ou seja: ela não exige infraestrutura de servidor quando não está executando

##	Serviços de aplicativos: 
PaaS. É uma plataforma para criar, implantar e dimensionar Web e APIs rapidamente. Ele trabalha com .NET, .NET Core, Node.js, java. python ou php

# SERVIÇOS DE REDE DO AZURE

## Rede virtual do Azure (VNet): 
Permite que os recursos do Azure se comuniquem uns com os outros, com a internet e com as redes locais

## Sub-redes virtuais: 
segmentam sua rede para atender às suas necessidades
## Gateway de VPN:
É usado para enviar tráfego criptografado entre uma rede virtual do Azure e uma no local pela internet pública.
## ExpressRoute: 
estende as redes locais para o Azure por meio de uma conexão privada facilitada por um provedor de conectividade – É CONECTAR UM CABO DE FIBRA ÓPTICA DA SUA REDE ATÉ O SERVIDOR, É + CARO, PORÉM MAIS PERFORMÁTICO
## DNS do Azure: 
confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNA usando a rede Anycast


# STORAGE ACCOUNTS -> CONTAS DE ARMAZENAMENTO
- Elas devem ter um nome único globalmente
- Servem para determinar os serviços de armazenamento e as opções de redundância
- Quando se cria o storage account se precisa configurar a redundância. 

Redundância = o quanto você quer que um sistema fique disponível
![image](https://github.com/user-attachments/assets/79e839a4-578f-429d-bec2-5744d19866b7)
![image](https://github.com/user-attachments/assets/e1cbee9b-d380-42b7-a1fc-6966cbe6db69)

LRS - Síncrono	- Não é indicado para produção porque se o datacenter cair você perde os dados
ZRS – Assíncrono


# TIPOS DE DADOS DOS STORAGES ACCOUNTS

- Blob: Onde se pode colocar de tudo, principalmente arquivos grandes
- Disco do Azure: Adicionar discos para máquinas virtuais
- Fila: Se pode armazenar e recuperar uma grande quantidade de mensagens
- Arquivo: Compartilhamento de arquivos de rede altamente disponível, usando o protocolo de bloco de mensagens do servidor
- Tabelas: Fornece uma opção de chave/atributos para dados estruturados e relacionais
Eles são armazenados nos links:
![image](https://github.com/user-attachments/assets/dae993e5-fbfd-4dd7-a93e-a6c61517847f)
Link: nome do storage account + nome do tipo de arquivo + core.windows.net

# CAMADAS DE ARMAZENAMENTO DE ACESSO DO AZURE
- Quando você está criando um arquivo, ele vai te perguntar isso
  ![image](https://github.com/user-attachments/assets/6fe7c6dd-bba5-40c4-84d0-d2174d368792)
- Os arquivos mortos demoram mais tempo para serem recuperados, justamente porque a Microsoft “quebra” o arquivo e precisa juntar os pedaços para recuperar
- No modelo frequente o valor cobrado pela consulta é mais barato do que em outros modelos.

# MIGRAÇÃO DE DADOS AZURE
- Azure Data Box: É um equipamento de migração física totalmente criptografado que vai te ajudar a migrar até 80TB de dados. Com ele você coloca seus dados lá e manda pro datacenter da Microsoft, no datacenter eles vão carregar seus dados pra nuvem e deixar esse data box como backup de recuperação para desastre.
Cenário de uso: Um cliente bem longe do datacenter deseja migrar pra nuvem, mas possui tantos dados (acima de 40TB) que pela internet seria difícil levar.

- AzCopy: É um utilitário de linha de comando que serve pra copiar blobs ou arquivos de ou para sua conta de armazenamento. Um ponto importante é que a sincronização é só em uma direção 

- Gerenciador de armazenamento do Azure: Interface gráfica do usuário (de modo semelhante ao Windows Explorer), é compatível com Windows, MacOS e Linux

- Sincronização de arquivos do Azure: É bidirecional, serve para sincronizar os arquivos do Azure e locais. A camada de  nuvem mantém os arquivos acessados com frequência no local, enquanto libera espaço

OBS: Se deve conhecer o cliente e o produto para entender qual seria o melhor produto para se aplicar.






