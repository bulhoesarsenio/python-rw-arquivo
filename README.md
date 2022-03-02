# python_escrita_em_arquivo
### Demonstrando como Ler, Escrever em arquivos com Python<br>
### O código está abaixo<br>

```
from fileinput import close
nome = ''
email = ''
cpf = ''
print('[1] - Cadastrar Cliente ')
print('[2] - Pesquisar Cliente ')
print('[3] - Sair')      
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
        break```
```
