# Validador-de-CPF
def validarCPF(cpf):<br>
    cpf = str(cpf)<br>
    lista = []<br>
    primeiro = segundo = 0<br>
    while True:<br>
        for x in cpf:<br>
            if x.isnumeric() == True:<br>
                lista.append(x)<br>
        if len(lista) != 11:<br>
            return(False)<br>
            break<br>
        y = 0<br>
        for x in range(10,1,-1):<br>
            primeiro += (int(lista[y])*x)<br>
            y += 1<br>
        primeiro *= 10<br>
        primeiro %= 11<br>
        if primeiro == 10:<br>
            primeiro = 0<br>
        y = 0<br>
        for x in range (11,1,-1):<br>
            segundo += (int(lista[y])*x)<br>
            y += 1<br>
        segundo *= 10<br>
        segundo %= 11<br>
        if segundo == 10:<br>
            segundo = 0<br>
        if primeiro == int(lista[-2]) and segundo == int(lista[-1]):<br>
            return(True)<br>
        else:<br>
            return(False)<br>
        break<br>

"""<br>
Variável como parâmetro de entrara do tipo char<br>
Variável de retorno do tipo boolean<br>
"""
