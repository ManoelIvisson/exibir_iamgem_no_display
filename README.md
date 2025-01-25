# Como exibir uma imagem no display da Bitdoglab

Eae pessoal, vi alguns colegas mostrando imagens no display que está na placa Bitdoglab, tentei fazer sozinho e tive alguns erros, mas no final consegui exibir uma imagem com sucesso! Ai resolvi fazer um tutorial para quem tem a curiosidade mas ainda não sabe como fazer, logo espero que seja de algum proveito o tutorial :)

## 1 - Formatação da imagem que será usada no display

A imagem que exibiremos precisa ser 128 x 64, pois essas são as dimensões do nosso display. Para redimensionar a imagem você pode escolher qualquer software gráfico como Photoshop ou Gimp, mas escolhi usar um mais simples que já tinha no meu computador, o Paint 3D. Quando a imagem estiver redimensionada salve o arquivo como _.bmp_.   
![paint](https://github.com/user-attachments/assets/1918ae41-818d-4718-8a35-be6db7a68257)

## 2 - Converter imagem em código

Para convertemos a imagem em código podemos utilizar o site [image2cpp](https://javl.github.io/image2cpp/). Agora seguiremos os seguintes passos:
1. Escolha a imagem a ser convertida:  
   ![Captura de Tela (87)](https://github.com/user-attachments/assets/75ee0b30-70d1-418a-a237-e5d0481aff64)

2. Deixe as dimenesões em 128 x 64, ajuste o brilho de acordo com a sua preferência e o mais importante: Vire a imagem para que fique em pé, 270 graus:  
![Captura de Tela (88)](https://github.com/user-attachments/assets/c00ec794-0568-4c6e-9819-ad347fefef8b)

3. Configure a saída, utilize o formato Arduino Code, modo de desenho na horizontal - 1 bit per pixel e troque os bits por byte:  
   ![Captura de Tela (90)](https://github.com/user-attachments/assets/623dc8e6-c92c-4d7d-a000-8d51bb76a6a8)

4. Gere o código e copie apenas o código hexadecimal.

## 3 - Adicionar o código hexadecimal ao arquivo .c

Utilize o repositório do display da placa [Bitdoglab](https://github.com/BitDogLab/BitDogLab-C/tree/main/display_oled) ou use o template desse repositório, em seguida apenas troque os códigos hexadecimais pelos os que foram gerados anteriormente e compile o código.

## 4 - Resultado
https://github.com/user-attachments/assets/52d5340c-c8f4-4b46-bc6e-3da3f055bed3
