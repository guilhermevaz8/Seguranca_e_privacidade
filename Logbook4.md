# Trabalho Realizado na Semana #4

## 2.1 
   
   -Usamos os comandos 'print env' e obtivemos todas as variáveis ambiente que o sistema tinha de momento.
    -Usamos export com export MY_VAR=hello, para criar uma nova variavel ambiente chamada MY_VAR e em seguida usamos unset MY_VAR para eliminar essa variavel.

## 2.2 

   -Step 1: Compilamos e corremos o programa com 'gcc myprintenv.c' e 'a.out>file' e ao observar o file podemos ver as variaveis ambiente do processo filho.
    -Step2: Fizemos as alterações compilamos novamente e corremos novamente criando um novo ficheiro de texto, que continha as variaveis ambiente do processo pai.
    -Step3: Usando diff file1 file2, não obtemos nenhum output no terminal pelo que podemos concluir que não há diferenças, ou seja, o processo pai transmitiu todas as variaveis ambiente ao processo filho.

# 2.3
   -Step1:depois de compliar o programa'gcc myenv.c' e de o correr 'a.out' não obtivemos nenhum output o que indica que a lista de variaveis ambiente está vazia.
    -Step2:Depois de fazer as alterações repetimos o processo e, agora sim, foram impressas as variáveis ambiente.
    -Step3:A função execve serve para executar o programa env que exibe a lista de variaveis ambiente, a variável environ serve para passar as variaveis ambiente que já existem para o novo programa, como no primeiro caso não usavamos esta variavel as variaveis não eram transmitidas e, por isso, não obtiamos nenhum output. 

# 2.4  

   -Compilamos, corremos o programa e verificamos que ele imprime todas as variáveis ambiente porque ao usar o metodo system as variaveis ambiente são todas passadas para o novo processo criado, enquanto com o execve temos de especificar as variaveis que queremos que sejam passadas. 

# 2.5

   -Step1:Escrevemos o código.
    
   -Step2:Compilamos o programa torna-mos o user root como owner 'sudo chown root setuid'; e alteramos as permissões para torná-lo um SET_UID program.'sudo chmod 4755 setuid'

   -Step3: Criamos novas variáveis, corremos o progama e osbervamos que a variável PATH que já existia continua a existir, que a variável ANY_NAME definida com 'export ANY_NAME=12' continua a aparecer mas a variável LD_LIBRARY_PATH definida com'export LD_LIBRARY_PATH=/bin' não aparece. Segundo pesquisas que fizemos se o programa passa-se todas as variáveis para o processo filho era perigoso porque alguem mal intencionado podia definir variáveis que iam afetar a segurança do sistema. Por isso os SET-UID programs são cuidadosamente controlados pelo sistema, sendo algumas variáveis permitidas por padrão e outras não essenciais não.


# 2.6

   -Ao executar o programa já depois de ter as permissões de root foi possivel usar ls sem ser no terminal.

 
    





    

