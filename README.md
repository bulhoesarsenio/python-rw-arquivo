# kjiukjgkgkkkk
### Demonstrando como Ler, Escrever em arquivos com Python<br>
hjhjjgfjhfgkjfgkkk

Nesse bloco abaixo, estou lendo um arquivo "arq01.txt" em modo de apenas leitura.
```
#Este programa tem como objetivo abrir um arquivo, se opção desejada igual a 1 você cadastra o cliente,
#e este cliente fica salvo dentro do arquivo,
#e se opção igual a 2 procura você procura pelo cliente cadastrado,
#opção 9 para sair,
from fileinput import close
nome = ''
email = ''
cpf = ''
print('############################')
print('##[1] - Cadastrar Cliente ##')
print('##[2] - Pesquisar Cliente ##')
print('##[3] - Sair              ##')      
print('###########################')
x = 0
while True:

    opcao = int(input('QUAL OPERAÇÃO VOCÊ DESEJA EXECULTAR: '))
    x += 1
    if opcao == 1:
        nome = str(input('INFORME SEU NOME: '))
        email = str(input('INFORME SEU EMAIL: '))
        cpf = input('INFORME SEU (CPF): ') 
    elif opcao == 2:
        #arquivo = open('cad.txt', 'a')
        with open('arq01.txt', 'a+') as arquivo:
         nome_cliente = str(input('informe o nome do cliente: '))
         if nome_cliente == nome:
            arquivo.write(f'nome do cliente: {nome} \n')
            arquivo.write(f'email do cliente: {email} \n')
            arquivo.write(f'cpf do cliente: {cpf} \n')                     
            arquivo.close()
         else:
             print('clienete inexistente')
        with open('arq01.txt', 'r') as arquivo:
            print(arquivo.read())
    elif opcao == 9:
        break
```
