# Simula-oOpera-esBanc-rias
Simples código em Pyhton para criação de conta bancária, e operações, saldo/ saques, cliente


class Cliente:

    def __init__(self, nome, cpf, Nconta, saldo, deposito, saque):
        self.nome = nome
        self.cpf = cpf
        self.Nconta = Nconta
        self.saldo = saldo
        self.deposito = deposito
        self.saque = saque



    def depositar (self, deposito):
        vlrDep = (self.saldo + self.deposito)
        print("Foi depositado", vlrDep)



    def sacar (self, saque):
        #vlrSaque = self.deposito - self.saque
        print("Valor atualizado do saldo é:", self.deposito - self.saque)


#**********************************

from cliente import Cliente
from random import *


nome = input("Digite nome:")
cpf = int(input("Digite cpf:"))
Nconta = randint(1,10)
saldo = 0
deposito = float(input("Digite valor do depósito:"))
saque = float(input("Digite valor do saque:"))




cliente1 = Cliente(nome, cpf, Nconta, saldo, deposito,saque)

cliente1.depositar(deposito)
cliente1.sacar(saque)

print("======DadosCliente 1================")
print("Nome do Cliente", cliente1.nome)
print("CPF d0 cliente:", cliente1.cpf)
print("Numero Da conta", cliente1.Nconta)
print("Saldo Inicial:", cliente1.saldo)
print("Deposito Inicial", cliente1.deposito)
print("Valor do saque", cliente1.saque)








