# resumo-do-lab
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


