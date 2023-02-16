# Projeto-de-Quiz-Hist-rico
 
 import random

print("Bem-vindo ao Quiz de História!\n")

perguntas = [
    {
        "pergunta": "Em que ano foi iniciada a República Brasileira?",
        "alternativas": {
            "A": "1889",
            "B": "1822",
            "C": "1890",
            "D": "1888"
        },
        "resposta": "A",
        "resposta_correta": "A República brasileira foi proclamada em 1889 por um grupo de militares."
    },
    {
        "pergunta": "Em que ano foi iniciada a Segunda Guerra Mundial?",
        "alternativas": {
            "A": "1939",
            "B": "1918",
            "C": "1945",
            "D": "1916"
        },
        "resposta": "A",
        "resposta_correta": "A WW2 foi iniciada em 1939 com a invasão alemã da Polônia."
    },
    {
        "pergunta": "Em que ano a União Soviética Caiu?",
        "alternativas": {
            "A": "1989",
            "B": "1971",
            "C": "1991",
            "D": "1990"
        },
        "resposta": "C",
        "resposta_correta": "Após diversas crises a União Soviética foi dissolvida no ano de 1991."
    }
]

random.shuffle(perguntas)
pontuacao = 0

for i, pergunta in enumerate(perguntas):
    print(f"\nPergunta {i + 1}: {pergunta['pergunta']}")
    for alternativa, resposta in pergunta["alternativas"].items():
        print(f"({alternativa}) {resposta}")
    resp = input("Sua resposta: ")
    if resp.upper() == pergunta["resposta"]:
        print(f"Resposta correta! {pergunta['resposta_correta']}")
        pontuacao += 1
    else:
        print(f"Resposta incorreta! A resposta correta era {pergunta['resposta_correta']}")

print("\nFim do Quiz!")
print(f"Você acertou {pontuacao} de {len(perguntas)} perguntas")
porcentagem = (pontuacao / len(perguntas)) * 100
print(f"Porcentagem de acertos: {porcentagem:.0f}%")
