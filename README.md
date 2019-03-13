# Validador-de-CPF
def validarCPF(cpf):<br>
    cpf = str(cpf)
    lista = []
    primeiro = segundo = 0
    while True:
        for x in cpf:
            if x.isnumeric() == True:
                lista.append(x)
        if len(lista) != 11:
            return(False)
            break
        y = 0
        for x in range(10,1,-1):
            primeiro += (int(lista[y])*x)
            y += 1
        primeiro *= 10
        primeiro %= 11
        if primeiro == 10:
            primeiro = 0
        y = 0
        for x in range (11,1,-1):
            segundo += (int(lista[y])*x)
            y += 1
        segundo *= 10
        segundo %= 11
        if segundo == 10:
            segundo = 0
        if primeiro == int(lista[-2]) and segundo == int(lista[-1]):
            return(True)
        else:
            return(False)
        break

"""
Variável como parâmetro de entrara do tipo char
Variável de retorno do tipo boolean
"""
