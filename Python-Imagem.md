TRATAMENTO DE IMAGEM UTILIZANDO PYTHON POR MEIO DA BIBLIOTECA OPENCV.

/// NEGATIVO DE UMA IMAGEM.
#negativo

#img_negative[ : , : ,0] = 255 - img[ : , : ,0]
#img_negative[ : , : ,1] = 255 - img[ : , : ,1]
#img_negative[ : , : ,2] = 255 - img[ : , : ,2]

#img_in = cv2.imread('data/Fig0304(a)(breast_digital_Xray).tif',1)
img_in = cv2.imread('data/t1.jpg',0)

img_out = 255 - img_in

cv2_imshow(img_in)
cv2_imshow(img_out)
'''
cv2_imshow('in', img_in)
cv2.waitKey(0)
cv2.imshow('out', img_out)
cv2.waitKey(0)
cv2.destroyAllWindows()


/// EXPLICAÇÃO GERAL:
     O negativo que vemos disponiveis em diversos softwares de imagens é amplamente utilizado quando se deseja trabalhar em cima de uma figura, tratando-a para muito das vezes facilitar na análise de detalhes que não seriam vistos em imagens originais.
     Normalmente, a função negativo atribuido a uma imagem é observada quando transformamos as áreas mais claras em mais escuras e as áreas mais escuras nas mais claras. Explicando de uma maneira bem simploria, uma imagem colorida armazena 3 canais diferentes que formam a sua composição base: vermelho, verde e azul (RGB). Dessa forma, para fazer o negativo da mesma basta inverter os valores desses 3 canais.
     
     ///EXEMPLO DE IMAGEM:
     ![image sem negativo](https://user-images.githubusercontent.com/106936217/172080900-7a802502-1369-43ee-a4a6-7ec9e93fd418.png)
     ![image com negativo](https://user-images.githubusercontent.com/106936217/172080923-608d640b-4d74-4462-9559-32e59bcedf18.png)

/// EXPLICAÇÃO DO CÓDIGO:
     Observa-se que cada um dos parametros RGB possui 256 valores, sendo o RGB (255,255,255) a cor branca, e o RGB (0,0,0) a cor preto. 
     No código, pode-se observar que a implementação da incersão da funcionalidade "negativa" é realizada por meio do calculo "255 - valor do pixel da img". Isso deve, como apresentado acima, por conta dos valores variarem de 0 á 255. Portanto, observa-se que quanto maior for o valor do pixel da img, menor vai ser o resultado do cálculo estabelecido, e isso cria o efeito de negativo, onde tonalidades mais claras se tornam escuras após o processamento, e tonalidades escuras se tornam mais claras.
