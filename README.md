# Atividade 7 - DevSecOps - Linux

O foco desta atividade é instalar e configurar uma máquina virtual (VM) do Oracle Linux 8.6 no VirtualBox.

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
Aqui podemos fazer algumas configurações interessantes. Por exemplo, em `System &rarr; Motherboard` podemos alterar a quantidade de memória alocada para a máquina virtual.  
Uma etapa essencial é carregar na máquina virtual a iso do Oracle Linux que foi baixada anteriormente. Para isso, vamos em `Storage`  

INSERIR IMAGEM  

Selecionamos a iso do Oracle Linux.  

Outra configuração importante é a da rede da máquina virtual. Para configurá-la, basta ir em `Network`. Em `Adapter 1`, vamos em `Attached to` e selecionamos a opção `Bridge Adapter`. Desta forma, nossa VM terá conexão com a internet, utilizando o driver de rede do Host, ou seja, da máquina que está rodando o VirtualBox.  

INSERIR IMAGEM

Feitas essas configurações, clique em Ok. De volta à tela inicial do VirtualBox, podemos selecionar nossa VM e clicar em `Start`.  

# Instalando o Oracle Linux











