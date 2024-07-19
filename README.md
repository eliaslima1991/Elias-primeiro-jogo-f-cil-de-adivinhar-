# Jogo de Adivinhação Elias Lima

## Descrição

Este projeto é um simples jogo de adivinhação escrito em Python. O objetivo do jogo é adivinhar um número secreto escolhido aleatoriamente pelo computador, dentro de um intervalo de 1 a 100. O jogador tem um número limitado de tentativas para adivinhar o número corretamente.

## Como Funciona

1. O computador escolhe um número secreto aleatório entre 1 e 100.
2. O jogador tem até 10 tentativas para adivinhar o número secreto.
3. A cada palpite, o jogo informa se o número secreto é maior ou menor que o palpite dado.
4. O jogo termina quando o jogador adivinha o número corretamente ou quando esgotam-se as tentativas.

## Executando o Jogo

Para jogar, siga estas etapas:

1. Certifique-se de ter o Python instalado em sua máquina.
2. Clone este repositório.
3. Navegue até o diretório do projeto.
4. Execute o script `jogo_adivinhacao.py`.

### Exemplo de uso:
# Elias-primeiro-jogo-f-cil-de-adivinhar-

print("****************") 

import random

def jogo_adivinhacao():
    numero_secreto = random.randint(1, 100)
    tentativas = 0
    max_tentativas = 30

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

print( 'Obrigado por testar nosso jogo ') 