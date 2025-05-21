

salario_bruto = float(input("Informe seu salário bruto: "))
horas_trabalhadas = float(input("Informe a quantidade de horas trabalhadas: "))

if salario_bruto < 0 or horas_trabalhadas < 0:
    print('erro: Não é possível valores negativos')
else:
    if horas_trabalhadas > 160:
        hora_extras = horas_trabalhadas - 160
        valor_hora = salario_bruto/160
        valor_adicional = (hora_extras * valor_hora) * 1.5
        
    else:
        valor_adicional = 0
    
    salario_com_adicional = salario_bruto + valor_adicional #soma o salário bruto com o valor adicional
    
    # cálculo dos descontos
    
if salario_bruto < 800:
    imposto_renda = 0
    encargos = 0
    
elif salario_bruto <= 1600:
    imposto_renda = salario_com_adicional * 0.08
    encargos = salario_com_adicional * 0.05
    
else:
    imposto_renda = salario_com_adicional * 0.15
    encargos = salario_com_adicional *0.07
    
    # cálculo salário líquido
    
salario_liquido = salario_com_adicional - imposto_renda - encargos    
    
      #exibição dos resultados
      
print('\nResumo do pagamento')
print(f'Salário Bruto: R$ {salario_bruto:.2f}')
print(f'Adicional de horas extras: R$ {valor_adicional:.2f}')
print(f'Imposto de Renda: R$ {imposto_renda:.2f}')
print(f'Encargos: R$ {encargos:.2f}')
print(f'Salário Líquido: R$ {salario_liquido:.2f}')
