import os

def processar_resposta(resposta, nome):
    if resposta == '1':
        print(f'{os.linesep}{nome} Segunda a Domingo das 08:00 às 17:00.{os.linesep}')
    elif resposta == '2':
        print(f'{os.linesep}{nome} RT-PCR Indicado para pessoas que tiveram contato com pessoas infectadas nos últimos dias. SOROLOGIA Indicado para pessoas que tiveram contato com vírus há mais de 14 dias.{os.linesep}')
    elif resposta == '3':
        print(f'{os.linesep}{nome}, RT-PCR até 24 horas úteis. SOROLOGIA até 24 horas úteis.{os.linesep}')
    elif resposta == '4':
        print(f'{os.linesep}{nome} RT-PCR R$ 340,00 SOROLOGIA R$ 169,00{os.linesep}')
    else:
        print('Digite apenas 1, 2, 3 ou 4')

def start():
    # Apresentar o chatbot
    print('Olá! Bem-vindo a ProntoTestes.com')
    # pedir o nome
    nome = input('Digite seu nome: ')
    # pedir o e-mail
    email = input('Digite seu e-mail: ')
    while True:
        # Oferer o menu de opções
        resposta = input(
            f'O que gostaria de saber hoje?{os.linesep}[1] - Horário para Realizar o teste.{os.linesep}[2] - Testes disponíveis.{os.linesep}[3] - Tempo para o resultado dos testes.{os.linesep}[4] - Valores dos testes.{os.linesep}')
        # Processar a resposta enviada
        processar_resposta(resposta, nome)

if __name__ == '__main__':
    start()
