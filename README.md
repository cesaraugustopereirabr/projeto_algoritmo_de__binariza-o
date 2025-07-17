
# Conversão de Imagem BMP para Tons de Cinza e Preto e Branco

Este projeto em Python converte imagens no formato BMP (24 bits) para:

    1. Escala de cinza (0 a 255)

    2. Imagem binarizada (preto e branco: 0 ou 255)

    3. Desenvolvido sem o uso de bibliotecas externas para processamento de imagem, seguindo a lógica da leitura e manipulação manual do formato BMP.

 ## Estrutura

    * imagem.bmp: imagem original (precisa estar no formato BMP 24 bits)

    * imagem_cinza.bmp: imagem resultante em tons de cinza

    * imagem_binaria.bmp: imagem binarizada (preto e branco)

    * conversor_colab.py (ou notebook): código-fonte

## Como funciona

O código realiza as seguintes etapas:

1.  Lê o arquivo BMP diretamente via leitura binária (struct);

2. Converte para escala de cinza, aplicando a fórmula perceptual:

Cinza = 0.299 * R + 0.587 * G + 0.114 * B

3. Binariza a imagem a partir de um limiar (default = 127);

4. Exibe as imagens diretamente no notebook (Google Colab) usando matplotlib.

## Como usar no Google Colab

* Abra o Colab e envie a imagem imagem.bmp pela aba lateral "Arquivos";

* Execute o código;

* Veja o resultado diretamente no notebook: original, cinza e binária.

## Requisitos

* A imagem deve estar no formato BMP 24 bits sem compressão;

* O código usa apenas:

    * struct (padrão do Python)

    * matplotlib e PIL.Image apenas para exibição no Colab (não para processamento).

## Observações

* Este projeto é ideal para fins educacionais, demonstrando como funciona a estrutura de um arquivo BMP e a manipulação de pixels sem bibliotecas externas;

* Para formatos como PNG ou JPG, recomenda-se o uso de bibliotecas como OpenCV, Pillow ou scikit-image.
