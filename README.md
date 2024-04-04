
#questão 1:  Defina uma função que calcule a area de um retangulo dados seus dois lados

def retangulo (x, y):
    print('A área é: ')
    return x*y

#É definido os lados do retângulo, com um input e logo lhe é retornado sua área

l1 = int(input('Insira um dos lados: '))
l2 = int(input('Insira o outro lado: '))

print(retangulo(l1, l2))

#questão 2: Defina uma funcao que calcule a area da superfıcie de um cubo que tem c por aresta.

def cubo(c):
    print('A área da superfície de um cubo de aresta c é: ')
    return 6*(c**2)

#A Função cubo é definida com base no tamanho da aresta, então é retornada a área de sua superfíce

c = int(input("Insira um valor à aresta: "))

print(cubo(c))

#questão 3: Defina uma funcao que calcule a area da coroa circular (anel) formada por dois cırculos de raios r1 e r2 (r1 > r2 e P i = 3.14)

def area(x, y):
    print('A área da coroa é: ')
    return 3.14*(x**2 - y**2)

#Função simples, texto e a formula para a área da coroa

x = int(input('Insira o raio de maior valor '))
y = int(input('Insira o raio de menor valor '))

print(area(x,y))

#questão 4: Termine o desenvolvimento da função que calcula a média de dois numeros.

def media (x, y):
    print('A média dos valores é: ')
    return (x + y)/2

#Função media na qual há o input de dois valores e retorna sua média

v1 = float(input('Insira o primeiro valor: '))
v2 = float(input('Insira o segundo valor: '))

print(media(v1, v2))


#questão 5: Defina uma função que calcule a ordenada de uma função de segundo grau dados os parâmetros a, b, c

def ordenada (a, b, c):
    return -1*(b**2 - 4*a*c)/4*a

a = float(input('Insira o valor a: '))
b = float(input('Insira o valor b: '))
c = float(input('Insira o valor c: '))

#É feito o cálculo seguindo os parâmetros dados, e então retornado o seu valor

print(ordenada(a, b, c))

#questão 6: média ponderada

def medpond (x, y, w, z):
    print('A média ponderada é:')
    return (x*y + w*z)/(y + z)

#Os valores são multiplicados pelos seus respectivos indíces de relevância e então divido pela somas desses indíces

x = float(input('Insira o primeiro valor: '))
y = float(input('Insira o peso do primeiro valor: '))
w = float(input('Insira o segundo valor: '))
z = float(input('Insira o peso do segundo valor: '))

print(medpond(x, y, w, z))

#questão 8: 15% de gorjeta

def gorjeta (c):
    print('A gorjeta é de: ')
    return c*0.15
    
#É feito uma simples conta de porcentagem pra retornar o valor da gorjeta de 15% baseado no valor da conta

conta = float(input('A conta foi de: '))

print(gorjeta(conta))

#questão 9: gorjeta variavel com a legislação

def gorjeta (c, g):
     print('A gorjeta é de: ')
     return c*g
     
#É feito o cálculo do valor da gorgeta baseado na porcentagem que é escrita e baseado no valor conta

conta = float(input('A conta foi de: '))
print('A gorjeta deve ser digitada em forma decimal, ex: 0.1 (10%)')
gorj = float(input('Insira a porcentagem para a gorjeta: '))

print(gorjeta(conta, gorj))


#questão 10: Saldo final, juros simples

def juros_simples(principal, taxa, tempo):
    juros = principal * taxa * tempo
    montante = principal + juros
    return montante

def main():
    principal = float(input("Digite o valor principal: "))
    taxa = float(input("Digite a taxa de juros (em decimal): "))
    tempo = int(input("Digite o período de tempo: "))

    resultado = juros_simples(principal, taxa, tempo)
    
print("O montante após {} meses será de: R$ {:.2f}".format(tempo, resultado))

if __name__ == "__main__":
    main()

# #questão 11: barco
def distancia_correnteza(velocidade_correnteza, largura_rio, velocidade_barco_perpendicular):
    tempo_travessia = largura_rio / velocidade_barco_perpendicular  # Calcula o tempo necessário para atravessar o rio
    distancia_arrastada = velocidade_correnteza * tempo_travessia  # Calcula a distância arrastada pela correnteza
    return distancia_arrastada

# Exemplo de uso da função:
velocidade_correnteza = 2  # Velocidade da correnteza em metros por segundo
largura_rio = 50  # Largura do rio em metros
velocidade_barco_perpendicular = 5  # Velocidade do barco perpendicular à correnteza em metros por segundo

distancia = distancia_correnteza(velocidade_correnteza, largura_rio, velocidade_barco_perpendicular)
print("A correnteza arrasta o barco por uma distância de", distancia, "metros.")
