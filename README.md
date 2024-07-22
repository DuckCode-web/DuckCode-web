import random
import time
cores = {'t':'\033[m','ver':'\033[1;31m','azul':'\033[1;34m','roxo':'\033[1;40m'}
print('ola eu sou a \033[1;35mBA (Burra artificial)\033[m :), vamos fazer um jogo\nno qual você e um detetive')
time.sleep(1)
nome = str(input('primeiro escolha um nome: '))
time.sleep(0.99)
print('ola \033[1;34;40m{}{}'.format(nome,cores['t']))
time.sleep(0.99)
print('mas antes,quando aparecer as escolhas, porfavor coloque exatamente igual as escolhas\ne sem espaços')
time.sleep(4)
play = str(input(f'começar:{cores['azul']}sim{cores['t']}/{cores['ver']}não{cores['t']}: '))
if play == 'sim':
  print('...')
  time.sleep(1)
  print('você, recebe uma denuncia de uma pessoa, com falta de ar,com o pescoço vermelho')
  time.sleep(1)
  print('a pessoa estava assustada e machucada')
  time.sleep(1)
  p1 = str(input(f'você {cores['azul']}investigar{cores['t']}/{cores['ver']}deixar{cores['t']}: '))
  if p1 == 'investigar':
    print('você vai,olha o corpo(lembrando que você foi sozinho)')
    time.sleep(1)
    print('você percebe um bilhete')
    time.sleep(1)
    print('oque você acha?')
    time.sleep(1)
    p2 = str(input(f'{cores['azul']}amardilha{cores['t']}/{cores['ver']}perdido: '))
    if p2 == 'amardilha':
      print('você percebe que e uma amardilha')
      time.sleep(1)
      print('então chama ajuda')
      time.sleep(1)
      print(f'então, {nome}(você),junto com sua ajuda, e acha uma cabana\nentra e ve um porão e decide entrar, e acha o assasino com uma faca, esperando você\n mas você trouce ajuda e pega ele')
      time.sleep(1)
      print('\033[1;34;40m ====VENCEUUU!!====')
    elif p2 == 'perdido':
      print('você pega o bilhete')
      time.sleep(1)
      p4 = str(input(f'{cores['azul']}ler{cores['t']}/{cores['ver']}não ler{cores['t']}: '))
      if p4 == 'ler':
        print('você acha uma localização')
        time.sleep(1)
        p3 = str(input('ir/não ir'))
        if p3 == 'ir':
          print('você vai, e acha uma cabana')
          time.sleep(1)
          print('voce decide entrar, e acha um porão')
          time.sleep(1)
          print('você entra e acha o assasino esperando você')
          time.sleep(1)
          p6 = str(input(f'{cores['azul']}lutar{cores['t']}/{cores['ver']}não lutar{cores['ver']}'))
          if p6 == 'lutar':
            print('(vamos usar um dado se cair {} 1 {} você vence a luta se cair {}2{} você perde e morre >:)'.format(cores['azul'],cores['t'],cores['ver'],cores['t']))
            time.sleep(1)
            dado = random.randint(1,2)
            if dado <= 1:
              print(f'{cores['azul']}====VENCEUU====')
              time.sleep(1)
              print('você vence e pega ele')
            elif dado <= 2:
              print('perdeu,{}você morreu'.format(cores['ver']))
        elif p3 == 'não ir':
          print('você leva o bilhete como prova,passa alguns dias e os assasinatos continuam')
          time.sleep(1)
          print('você começa a suspeitar de seu colegas, pois parece que a policia sempre pega todas as provas e queimam')
          time.sleep(1)
          print('você suspeita dos policias que cuidam dos casos de afogamento,assasinato geral e guarda de Transito')
          time.sleep(1)
          p5 = str(input(f'{cores['roxo']}afogamento/transito/assasinato geral{cores['t']}'))
          if p5 == 'assinato geral':
            print('você, investiga ele mas não acha nada :(')
            time.sleep(1)
            p5 = str(input(f'{cores['roxo']}afogamento/transito/assasinato geral{cores['t']}'))
          elif p5 == 'transito':
            print('você investiga ele, e acha provas')
            time.sleep(1)
            print('e você  prova que e ele')
            print(f'\033[1;34;40m====VENCEUU====')
          elif p5 == 'afogamento':
            print('você investiga ele mas não acha nada :(')
            p5 = str(input(f'{cores['roxo']}afogamento/transito/assasinato geral{cores['t']}'))
      elif p4 == 'não ler':
        print('você leva o bilhete como prova,passa alguns dias e os assasinatos continuam')
        time.sleep(1)
        print('você começa a suspeitar de seu colegas, pois parece que a policia sempre pega todas as provas e queimam')
        time.sleep(1)
        print('você suspeita dos policias que cuidam dos casos de afogamento,assasinato geral e guarda de Transito')
        time.sleep(1)
        p5 = str(input(f'{cores['roxo']}afogamento/transito/assasinato geral{cores['t']}'))
        if p5 == 'assasinato geral':
          print('você  investiga ele mas não acha nada :(')
          time.sleep(1)
          p5 = str(input(f'{cores['roxo']}afogamento/transito/assasinato geral{cores['t']}'))
        elif p5 == 'Transito':
          print('você, investiga ele, e acha provas')
          time.sleep(1)
          print('e você, prova que e ele')
          print(f'\033[1;34;40m====VENCEUU====')
        elif p5 == 'afogamento':
          print('você investiga ele mas não acha nada :(')
          p5 = str(input(f'{cores['roxo']}afogamento/transito/assasinato geral{cores['t']}'))
          if p5 == 'assasinato geral':
            print('você e burro né?')

          elif p5 == 'Transito':
            print('você, investiga ele, e acha provas')
            time.sleep(1)
            print('e você, prova que e ele')
            print(f'\033[1;34;40m====VENCEUU====')
          elif p5 == 'afogamento':
            print('você e burro né?')

  elif p1 == 'deixar':
    print(f'caramba, você e uma pessoa fria,{cores['ver']}SEM CORAÇÃO!!')
    exit()
elif play == 'não':
  exit()
else:
  print(f'{cores['ver']}porfavor responda')
