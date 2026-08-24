# cp1-sem-2-michele
#recolher informações do usuário e calcular a média final do 2º semestre
cp1 = float(input("Nota do Checkpoint 1: "))
cp2 = float(input("Nota do Checkpoint 2: "))
cp3 = float(input("Nota do Checkpoint 3: "))
sp1 = float(input("Nota da Sprint 1: "))
sp2 = float(input("Nota da Sprint 2: "))
gs = float(input("Nota da Global Solution: "))

#identificar a menor nota do checkpoint Utilizar obrigatoriamente uma estrutura de repetição for para solicitar e armazenar as notas em uma lista ou dicionário;
checkpoints = [cp1, cp2, cp3]
menor_cp = checkpoints[0]
for nota in checkpoints:
    if nota < menor_cp:
        menor_cp = nota

#Calcule a média do 2º semestre conforme a regra estabelecida media = ((cp1 + cp2 + cp3 − menor_cp + sp1 + sp2) / 4) × 0,4 + gs × 0,6
soma_4 = sum(checkpoints) - menor_cp + sp1 + sp2
media_parcial = (soma_4 / 4) * 0.4
media_final = media_parcial + gs * 0.6
print(f"Menor nota de checkpoint: {menor_cp:.1f}")
print(f"Média do 2º semestre: {media_final:.1f}")
