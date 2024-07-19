# Elias-primeiro-jogo-f-cil-de-adivinhar-
import random

def jogo_adivinhacao():
    numero_secreto = random.randint(1, 100)
    tentativas = 0
    max_tentativas = 10

    print("Bem-vindo ao jogo de adivinhação!")
    print("Eu pensei em um número entre 1 e 100.")
    print(f"Você tem {max_tentativas} tentativas para adivinhar o número.")

    while tentativas < max_tentativas:
        try:
            palpite = int(input("Digite o seu palpite: "))
        except ValueError:
            print("Por favor, insira um número válido.")
            continue

        tentativas += 1

        if palpite < numero_secreto:
            print("O número secreto é maior.")
        elif palpite > numero_secreto:
            print("O número secreto é menor.")
        else:
            print(f"Parabéns! Você adivinhou o número em {tentativas} tentativas.")
            break
    else:
        print(f"Você excedeu o número máximo de tentativas. O número secreto era {numero_secreto}.")

if __name__ == "__main__":
    jogo_adivinhacao()