## Parte 1: Projeto de Introdução a Teoria da Informação (ITI)

### 📚 Organização do repositório
O repositório raíz esta organizado em duas pastas (1. corpus_files e 2. disco_files) e um arquivo pdf (Relat_rio_ITI.pdf) que contendo algumas informações adicionais sobre o projeto.
Divisão das pastas:
- 📁 **corpus_files**: esta pasta contém duas subpastas (1. saidaCompressao e 2. saidaDEScompressao) que correspondem respectivamente a saída do arquivo txt corpus em diferentes tamanhos de MB após o processo de compressão e descompreção usando o LZW. Além disso, esta pasta dispõe do arquivo original (corpus16MB.txt) e também o código fonte em *python* (parte1_ITI_txt.ipynb) usando para a compressão e descompressão do arquivo.
- 📁 **disco_files**: esta pasta de modo analogo a primeira contém a mesma divisão das pastas e arquivos duas subpastas (1. saidaCompressao e 2. saidaDEScompressao), arquivo original e código fonte em *python* entretanto usando o arquivo em video (disco.mp4).

### 📄 Descrição do projeto 
Foi implementado um compressor e descompressor utilizando o utilizando o algoritmo LZW. Considerando que as mensagens são geradas por fontes com alfabeto A = {0, 1, ..., 255}. Os testes do compressor/descompressor foram feitos com um corpus de texto em português de 16MB e com um arquivo binário de vídeo.

Se fosse utilizado o LZW:

O índice do dicionário deveria ser testado com diferentes tamanhos K bits (parâmetro). 

Exemplo: K=9bits tamanho do dicionário: 2^9=512, K=10bits tamanho do dicionário 2^10=1024. 

No relatório era necessário apresentar as curvas de RC x K e de Tempo de Processamento x K, para K = 9, 10, 11, 12, 13, 14, 15, 16 bits.
A variação do K deve ser realizada no eixo x do gráfico (horizontal). Também sendo necessário indicar a quantidade total de índices presentes na mensagem final para cada K.

📌 Observações:
- Os símbolos do arquivo de teste devem ser lidos no modo binário (números) e não no modo texto (caracteres/strings).
- O codificador deve receber como entrada um arquivo e gerar como saída o arquivo codificado.
- O decodificador deve receber como entrada o arquivo codificado e gerar com o saí da o arquivo decodificado, este deve ser igual ao original.
- A execução dos experimentos é demorada.

✍ Pontos a serem avaliados no relatório:
1. Desenvolveu em qual linguagem? Fez utilizando PPMC ou LZW? Utilizou alguma biblioteca como base?
2. A compressão e descompressão funcionou para os 2 arquivos de testes?
a. No arquivo de texto, teve algum problema com os caracteres acentuados?
b. Se não funcionou perfeitamente, qual o problema que ocorreu?
c. O arquivo de vídeo continua sendo "tocável" após a descompressão?
d. Utilize o programa diff ou FC para comparar se o arquivo original é igual ao arquivo descomprimido. Informe se a comparação indicou que os arquivo são iguais.
3. Conseguiu fazer com todos os valores de Ks solicitados (9 a 16 no LZW ou 0 a 8 no PPM)?
4. Conseguiu salvar a quantidade exata de K bits no arquivo?
a. Usou qual técnica? Conversão de bits para String? Bitstream? Salvou todos os índices em 2 bytes?
5. Apresentou a curva RCxK e Tempo x K para os 2 arquivos de testes?
a. Como calculou a RC? RC = tamArqOriginal / tamArqComprimido RC = tamArqOriginal / ((totalIndices x K)/8)
6. Dicionário ficou estático depois que atingiu o tamanho máximo? Em que Ks ele atingiu o tamanho máximo?

### ⚙ Como rodar
Para executar os programas, o arquivo de entrada deve estar no mesmo diretório, além das pastas "saidaCompressao" e "saidaDEScompressao".
1. Faça um clone do repositório
2. Use o Jupyter ou Colab para abrir o projeto
3. No Colab clique em Ambiente de execução -> Executar Tudo, ou use o comando ctrl+F9.
4. No Jupyter basta clicar em *run*
