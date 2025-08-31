# JO-KEN-P-

from random import randint

itens = ('Pedra', 'Papel', 'Tesoura')

while True:
    print(" JO KEN PÔ")
    print('''
    [0] Pedra
    [1] Papel
    [2] Tesoura
    ''')

    jogador = int(input("Sua escolha: "))
    pc = randint(0, 2)
    print('=-'*14)
    print(f"Você escolheu: {itens[jogador]}")
    print('=-'*14)
    print(f"O computador escolheu: {itens[pc]}")
    print('=-'*14)


    # regras
    regras = {
        0: 2,  # Pedra ganha de Tesoura
        1: 0,  # Papel ganha de Pedra
        2: 1   # Tesoura ganha de Papel
    }

    if jogador == pc:
        print("Empate!")
        print('=-' * 14)

    elif regras[jogador] == pc:
        print("Você ganhou! ")
        print('=-' * 14)

    else:
        print("Você perdeu! ")
        print('=-' * 14)

    # pergunta se continua
    resp = input("Continuar: ")
    print('=-'*14)

    if resp.lower() == 'n':
        break

print("Fim do jogo!!!")


