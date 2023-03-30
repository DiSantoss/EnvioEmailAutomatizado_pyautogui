```python
import pyautogui as py
import time
import pyperclip

py.PAUSE = 1

#Passos 
#abrir uma aba, escrever site gmail e apertar enter e esperar 4 segundos
py.hotkey('ctrl','t')
py.write('escrevaositedeondequerenviaromeial') #porexemplo www.gmail.com
py.press('enter')
time.sleep(4)

#clicar em escrever
py.click(x=97, y=169)

time.sleep(5)

#ESCREVER EMAIL DESTINATÁRIO e apertar tab 2x
py.write('escrevaoemailaqui')
py.press('tab')
py.press('tab')

#ESCREVER ASSUNTO e apertar tab
pyperclip.copy('escrevaoassuntoaqui')
py.hotkey('ctrl','v')
py.press('tab')

#ESCREVER CORPO DO EMAIL

pyperclip.copy('''
    Olá,

    Estou muito interessado em fazer parte da equipe da como estagiário em Desenvolvimento Front-end. Com minha experiência em tecnologias como HTML5, CSS, JavaScript, Bootstrap, Git e Github, juntamente com meu curso tecnólogo superior em Análise e Desenvolvimento de Sistemas eu ótimo curso de fullstack da B7WEB, estou confiante em minha capacidade de ser um grande contribuinte para sua equipe de tecnologia!

Estou entusiasmado com os desafios e animado em participar de reuniões diárias com a equipe de tecnologia e interagir com outros membros da equipe para ajudar a alcançar nossos objetivos.

Estou muito motivado a aprender e crescer nesta posição.

Agradeço sua consideração e espero ter a oportunidade de discutir minha aplicação futuramente.


Atenciosamente,
Diego dos Santos
21 98108-5639
''')
py.hotkey('ctrl','v')

#clicar em anexo
py.click(x=960, y=690)

#escrever nome do arquivo e apertar enter
py.click(x=666, y=54)
pyperclip.copy(r'escrevaoseuendereçoondeestaoarquivooucurriculo')
py.hotkey('ctrl','v')

py.press('enter')

py.click(x=642, y=547)
py.write('nomedoarquivo')
py.press('enter')


time.sleep(4)
py.click(x=842, y=690)

```

# Automatizando o Envio de E-mails com PyAutoGUI
Este projeto tem como objetivo demonstrar como é possível utilizar a biblioteca PyAutoGUI para automatizar o envio de e-mails. Com ele, você será capaz de enviar mensagens de e-mail de forma rápida e eficiente, economizando tempo e reduzindo erros manuais.

# Pré-requisitos
Antes de começar, certifique-se de ter as seguintes ferramentas instaladas:

Python 3.x
Jupyter Notebook
PyAutoGUI
Gmail API
Chromedriver


# Utilização
Ao executar o arquivo automated_email.ipynb, você será solicitado a fornecer as informações necessárias para enviar o e-mail, incluindo o endereço de e-mail do destinatário, o assunto e o corpo da mensagem. O PyAutoGUI irá então automatizar o processo de abertura do Gmail, preenchimento dos campos necessários e envio da mensagem.

# Contribuição
Se você encontrar algum problema ou tiver sugestões de melhoria, sinta-se à vontade para abrir uma issue ou um pull request. Suas contribuições são muito bem-vindas!

