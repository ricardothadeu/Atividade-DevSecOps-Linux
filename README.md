# Atividade 7 - DevSecOps - Linux

O principal foco desta atividade é configurar e instalar uma máquina virtual (VM) do Oracle Linux 8.6 no VirtualBox.

# Obtendo o Oracle Linux 8.6

A iso do Oracle Linux 8.6, assim como outras versões do sistema, pode ser obtida no [site da Oracle](https://yum.oracle.com/oracle-linux-isos.html). 
Realizado o download da iso, podemos avançar para a etapa de criação e instalação da VM.

# Criando a máquina virtual Oracle Linux no VirtualBox

Na tela inicial do VirtualBox, clique em New, ou utilize o atalho Ctrl+N. Realizaremos algumas etapas para criar a máquina virtual.

INSERIR IMAGEM   

1. O nome da VM é arbitrário. Após selecionar as opções que correspondem ao Oracle Linux, clicar em Next.  
2. Agora deve-se escolher a quantidade de memória RAM alocada para a VM. O recomendado é alocar no mínimo 2048 MB (2GB) para a VM. Definida a quantidade de RAM alocada, clicar em Next.  
3. Nessa etapa o VirtualBox pergunta se desejamos criar um disco rígido virtual ou usar algum já existente. Mantenha a opção padrão, `create a virtual hard disk now`. Clicar em Next.  
4. O VirtualBox deseja saber qual o tipo de disco rígido virtual você deseja criar. Caso você tenha a intenção de usar essa máquina virtual em outro software de virtualização, escolha a opção VHD. Caso contrário, a opção VDI pode ser mantida. Clicar em Next.  
5. Agora você deve escolher se o seu disco rigido virtual será alocado dinamicamente ou terá tamanho fixo. A primeira opção é mais recomendada, pois desta forma o disco vai crescendo de acordo com o seu uso. Assim como também diminuirá se você liberar espaço nele. Definida a opção desejada, clicar em Next.  
6. Por último, devemos escolher o tamanho que esse disco rígido virtual terá. Na atividade foram definidos 30 GB de disco. Clicar em Create.  

A máquina virtual foi criada. Agora devemos fazer algumas configurações nessa VM. Para isso, clique em Settings (ou usar o atalho Ctrl+S).  
Aqui podemos fazer algumas configurações interessantes. Por exemplo, em `System > Motherboard` podemos alterar a quantidade de memória alocada para a máquina virtual.  
Uma etapa essencial é carregar na máquina virtual a iso do Oracle Linux que foi baixada anteriormente. Para isso, vamos em `Storage`  

INSERIR IMAGEM  

Selecionamos a iso do Oracle Linux.  

Outra configuração importante é a da rede da máquina virtual. Para configurá-la, basta ir em `Network`. Em `Adapter 1`, vamos em `Attached to` e selecionamos a opção `Bridge Adapter`. Desta forma, nossa VM terá conexão com a internet, utilizando o driver de rede do Host, ou seja, da máquina que está rodando o VirtualBox.  

INSERIR IMAGEM

Feitas essas configurações, clique em Ok. De volta à tela inicial do VirtualBox, podemos selecionar nossa VM e clicar em `Start`.  

# Instalando o Oracle Linux

Pressione a tecla Enter na opção `Install Oracle Linux 8.6.0`.  
#### 1. Selecionando o idioma do sistema operacional
A primeira etapa é selecionar o idioma. É uma boa práticar instalar o sistema operacional em inglês, pois dessa forma podemos obter novas atualizações de forma mais rápida. Portanto, selecione `English (United States)`.  

#### 2. Selecionando o idioma do teclado
Em `Keyboard Layout`, clica no sinal de +. Procure a opção `Portuguese (Brazil)` e clique em `Add`. Selecione a opção `English (US)` e clique no sinal de `-`. Clique em `Done`.

#### 3. Configurando data e hora do sistema
Selecione a região Américas e a cidade que melhor se encaixa na sua situação. Nesta atividade, foi selecionada a cidade de São Paulo, horário de Brasília. Clique em `Done`.  

#### 4. Selecionando o tipo de instalação
Prosseguindo em nossa instalação, devemos selecionar o tipo de instalação que desejamos para o sistema operacional. Em `Software Selection`, selecione a opção `Minimal Install`. Ou seja, estamos instalando o Oracle Linux sem interface gráfica. Clique em `Done`.  

#### 5. Selecionando disco de instalação
O próximo passo é selecionar o disco no qual será feita a instalação do Oracle Linux. Para isso, vamos na opção `Installation Destination`. Em `Local Standard Disks`, selecionamos o disco disponível, que foi o disco que criamos alguns passos atrás. Em `Storage Configuration`, podemos selecionar a opção 
`Automatic`, na qual o próprio sistema decide o tamanho das partições que serão criadas no disco, ou a opção `Custom`, na qual nós criamos as partições de acordo com nossas preferências. Nessa atividade, a escolha foi pela opção automática.  

#### 6. Configurando rede e host name
Em `Network & Host Name`, selecione o dispositivo de rede disponível e o habilite, clicando no botão `OFF/ON`. Mais abaixo também é possível alterar o Host Name. Feitas as configurações, clicar em Done.  

#### 7. Criando senha do root e novos usuários
Por último, em `Root Password`, podemos definir a senha do usuário root do sistema. Digite uma senha forte e, ao final, clique em Done. Agora também temos a opção de criar outro usuário. Se desejar esta opção, basta preencher as informações que são pedidas. Uma das opções é a de dar direitos de administrador para este novo usuário. Criado o usuário, basta clicar em Done.  

#### 8. Concluindo instalação
Após as etapas acima, já podemos iniciar a instalação do Oracle Linux. Clicar em `Begin Installation`. O processo de instalação levará alguns minutos para ser concluído. Quando o processo terminar, devemos reiniciar o sistema. Clicar em `Reboot System`. Nossa máquina virtual com o Oracle Linux 8.6 está pronta para ser utilizada.  


# Snapshots
Neste momento, o uso de snapshots já começa a ser interessante. O snapshot é uma poderosa ferramenta do VirtualBox. Por meio dos snapshots, conseguimos salvar as configurações e dados atuais do sistema. Desta forma, depois podemos restaurar todo o sistema para o exato ponto em que o snapshot foi criado.  
Os snapshots devem ser utilizados com moderação. O acúmulo de snapshots pode fazer com que a VM se comporte de forma inadequada, além de ser um desperdício de espaço. Os snapshots não são recomendados para restaurações de longo prazo.  
Os snapshots são especialmente úteis antes de realizar atualizações, configurações, testes. Em caso de algo errado acontecer, basta restaurar o sistema para o último snapshot criado.  
Para criar um snapshot, basta ir em `Machine > Take Snapshot`, ou utilizar o atalho `Host+T`.  















