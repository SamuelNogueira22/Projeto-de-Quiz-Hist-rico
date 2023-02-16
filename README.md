# Projeto-de-Quiz-Hist-rico
# Validação Para começar o código, se o usuário digitar "N" o programa fecha
respst_user = input("Quer Começar? (S/N)")
if respst_user != 'S':
   quit()

#Criação do sistema de pontuação, inicialmente começa 0 e vai sendo aumentado conforme cada acerto
pontuacao = 0
print("Começando.....")

#Primeira pergunta
print("Em que ano foi iniciada a República Brasileira? \n (A)1889 \n (B)1822 \n (C)1890 \n (D)1888")
respst1 = input('Resposta: ')
if respst1 == 'A':
    print("Resposta Correta!, \n A República brasileira foi proclamada em 1889 por um grupo de militares.")
    pontuacao = pontuacao + 1
else:
    print("Resposta Incorreta!, A República foi procamada em 1889.")
    
#Segundaa pergunta
print("Em que ano foi iniciado a Segunda Guerra Mundial? \n (A)1939 \n (B)1918 \n (C)1945 \n (D)1916")
respst2 = input('Resposta: ')
if respst2 == 'A':
    print("Resposta Correta!, \n A WW2 foi iniciada em 1939 com a invasão alemã da Polônia.")
    pontuacao = pontuacao + 1
else:
    print("Resposta Incorreta!, a Segunda Guerra Mundial teve início em 1939.")
    
#Terceira pergunta
print("Em que ano a União Soviética Caiu? \n (A)1989 \n (B)1971 \n (C)1991 \n (D)1990")
respst3 = input('Resposta: ')
if respst3 == 'C':
    print("Resposta Correta!, \n Após diversas crises a União Soviética foi dissolvida no ano de 1991.")
    pontuacao = pontuacao + 1
else:
    print("Resposta Incorreta!, A União Soviética teve seu fim no ano de 1991.")
    
#Revelação do Resultado do Quiz, nas várias hipóteses de quantidade de acertos
if pontuacao == 0:
    print("Você errou todas!, Estude mais história e tente novamente!")
elif pontuacao == 3:
    print("Parabéns!, você passou com excelência, não errando nenhuma.")
else:
    print("Você Acertou ", pontuacao, "de 3, Está no caminho certo, mas continue estudando bastante históra.")
    
#Divulgação da porcentagem de acertos do Quiz, complementando o código
porcentagem = (pontuacao / 3) * 100
print("Porcentagem de acertos: {:.0f}%".format(porcentagem))
