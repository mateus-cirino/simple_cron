# Exemplo simples da utilização do CRON no Linux  
## Diferença entre CRONJOB e CRONTABLE
CRONJOB é de fato a tarefa que você quer executar, já o CRONTABLE é a tabela que ficará registrada os CRONJOB's.  
Para acessar a tabela de cron, digite no terminal o seguinte código: `crontab -e`, ao fazer isso você verá algumas linhas comentando como funciona a CRONTABLE e como declarar um CRONJOB.  
### Criando um CRONJOB
Após digitar o comando `crontab-e` no final do arquivo nós vamos adicionar o seguinte comando: `* * * * * echo "testando o cron" >> ~/Área\ de\ Trabalho/readme.md
` salve o arquivo segurando as teclas CTRL + S e para sair CTRL + X.
O comando digitado acima irá dar um `echo` em um arquivo README.md com o texto "testando o cron" a cada minuto.  
#### Estrutura de um CRONJOB
Um CRONJOB possuí 6 campos, sendo os cinco primeiros relacionados ao tempo de execução e o último o comando a ser executado.  
* (minuto) * (hora) * (dia) * (mês) * (de um dia até outro dia) (comando).
O caracter (*) serve para ser executado sempre, por exemplo se colocarmos o caracter (*) no campo de minutos, este será executado a cada minuto.
### Adicionando um CRONJOB na tabela
Após digitar o comando `crontab-e`, basta adicionar o seu CRONJOB no final dela.
### Listar todos os CRONJOBS da tabela
Basta executar o comando `crontab -l`.



