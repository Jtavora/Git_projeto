# Técnicas de Programação e Análise de Algoritmos PROJETO 2

Arquivos binários com os códigos executáveis do Projeto 2 (```server``` e ```main```)

## Exemplo de uso

```console
make all
User@PC:$ clear (Limpa tela)

User@PC:$ git branch branch1
Branch 'branch1' criada com sucesso!

User@PC:$ git branch branch2
Branch 'branch2' criada com sucesso!

User@PC:$ git branch
22 branch2
63 branch1
91 Master

User@PC:$ git checkout branch1
Mudada para branch 'branch1' com sucesso!

User@PC:$ git commit -m teste_branch1
Commit 'teste_branch1' criado com sucesso!

User@PC:$ git checkout branch2
Mudada para branch 'branch2' com sucesso!

User@PC:$ git commit -m teste_branch2
Commit 'teste_branch2' criado com sucesso!

User@PC:$ git log
Branch_atual: branch2
71 teste_branch1
From branch: branch1
86 teste_branch2
From branch: branch2
91 FirstCommit
From branch: Master

User@PC:$ git push
Iniciando Git ...
Socket do Git criado com fd: 3
Remoto diz: Repositório remoto iniciado!
Enviando o commit para o servidor...
DADOS ENVIADOS: 71 teste_branch1 branch1
DADOS ENVIADOS: 86 teste_branch2 branch2
DADOS ENVIADOS: 91 FirstCommit Master
Resposta do remoto: Commit recebido!

Conexão fechada


User@PC:$ ^Cmake: *** [Makefile:11: run] Interrupt (Ctrl + c)

```

## Console servidor:

```console
./prog2.exe
Abrindo socket do servidor...
-------------------------------------------------------------------------------------------
Iniciando o Servidor
Soquete do servidor criado com fd: 3
Ouvindo na porta 8080

Cliente conectado.
Aguardando acao do cliente ...

DADOS DO COMMIT RECEBIDO: 71 teste_branch1 branch1
DADOS DO COMMIT RECEBIDO: 86 teste_branch2 branch2
DADOS DO COMMIT RECEBIDO: 91 FirstCommit Master
Cliente desconectado.
Conexão fechada

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------
Iniciando o Servidor
Soquete do servidor criado com fd: 3
Ouvindo na porta 8080
```

## Abre novo cliente:

```console
./prog.exe
User@PC:$ clear (Limpa tela)

User@PC:$ git pull

Recebendo dados do servidor...
Dados recebidos: Repositório remoto iniciado!
DADOS DO COMMIT RECEBIDO: 75 teste_branch1 branch1
DADOS DO COMMIT RECEBIDO: 92 teste_branch2 branch2
DADOS DO COMMIT RECEBIDO: 94 FirstCommit Master
Recebendo dados do servidor...
Dados recebidos: Commit recebido!

Conexão fechada


User@PC:$ ^C
```

## Console do servidor:
```console
Abrindo socket do servidor...
-------------------------------------------------------------------------------------------
Iniciando o Servidor
Soquete do servidor criado com fd: 3
Ouvindo na porta 8080

Cliente conectado.
Aguardando acao do cliente ...

DADOS DO COMMIT RECEBIDO: 75 teste_branch1 branch1
DADOS DO COMMIT RECEBIDO: 92 teste_branch2 branch2
DADOS DO COMMIT RECEBIDO: 94 FirstCommit Master
Cliente desconectado.
Conexão fechada

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------
Iniciando o Servidor
Soquete do servidor criado com fd: 3
Ouvindo na porta 8080

Cliente conectado.
Aguardando acao do cliente ...

DADOS DO COMMIT ENVIADO: 75 teste_branch1 branch1
DADOS DO COMMIT ENVIADO: 92 teste_branch2 branch2
DADOS DO COMMIT ENVIADO: 94 FirstCommit Master
Conexão fechada

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------
Iniciando o Servidor
Soquete do servidor criado com fd: 3
Ouvindo na porta 8080
^C
```
