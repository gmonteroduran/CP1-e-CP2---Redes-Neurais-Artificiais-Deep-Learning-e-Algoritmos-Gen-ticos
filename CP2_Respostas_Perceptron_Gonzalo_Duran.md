# CP2 - Perceptron | Perguntas e respostas

## 1. O que é um Perceptron?
É um modelo simples de neurônio artificial que recebe entradas, faz uma soma usando pesos e depois toma uma decisão. No nosso caso, decide se o cliente recebe ou não a oferta.

## 2. Quais são os principais elementos que compõem um Perceptron?
São as entradas, os pesos, a soma ponderada, a função de ativação e a saída. Também podemos usar o bias para ajustar o ponto da decisão.

## 3. Qual é a função dos pesos dentro do Perceptron?
Os pesos mostram a importância de cada entrada na decisão. Durante o treinamento eles vão mudando conforme os erros, para o modelo aprender a resposta correta.

## 4. Qual é a função da função de ativação?
Ela pega o resultado da soma e transforma em uma resposta. Usamos a função degrau: se a soma é maior ou igual a zero, retorna 1; se é negativa, retorna 0.

## 5. Quantas épocas foram necessárias para o Perceptron convergir sem viés?
Não conseguiu convergir nas 10 épocas que treinamos. Continuou tendo erros em todas elas.

## 6. O modelo conseguiu chegar a uma época com zero erros sem viés?
Não. Em cada uma das 10 épocas tivemos 4 erros durante o treinamento.

## 7. Explique por que esse comportamento ocorreu. Observe principalmente a entrada [0, 0].
Quando a entrada é [0, 0], a soma sem bias sempre dá zero, independente dos pesos. Como a função degrau retorna 1 para zero, a previsão fica 1, mas o esperado era 0. E como as entradas são zero, esse erro também não consegue mudar os pesos. Por isso não resolve o problema sem bias.

## 8. Quantas épocas foram necessárias para o modelo convergir com viés?
Foram necessárias 6 épocas. Na sexta época tivemos zero erros.

## 9. Quais foram os pesos finais encontrados?
Os pesos finais foram [0.2, 0.1].

## 10. Qual foi o valor final do bias?
O bias final foi -0.3.

## 11. Para que serve o viés em um Perceptron? Explique com suas palavras.
O bias ajuda a ajustar o limite para liberar a resposta 1. É como colocar uma exigência a mais na soma. Nesse exercício ajudou o modelo a liberar a oferta somente quando as duas condições estavam certas.

## 12. Qual foi a principal diferença entre o treinamento sem viés e o treinamento com viés?
Sem bias o modelo continuou errando e não convergiu. Com bias ele conseguiu ajustar melhor a decisão e chegou a zero erros na época 6.

## 13. O viés substitui os pesos? Explique.
Não. Os pesos continuam indicando quanto cada entrada influencia a soma. O bias é um valor adicional que ajusta o limite da decisão. Os dois trabalham juntos.

## 14. Um único Perceptron com viés seria suficiente para resolver um problema XOR? Explique.
Não. O XOR não pode ser separado por uma única reta, então um Perceptron simples, mesmo com bias, não consegue resolver todos os casos. Para isso precisamos de mais neurônios e uma camada oculta.

## Conclusão
Aprendi que os pesos mudam conforme os erros para o Perceptron tentar acertar as respostas.
Cada época é uma passagem por todos os exemplos, e convergência é quando chegamos a uma época sem erros.
No exercício sem bias vimos que os pesos sozinhos não conseguiam resolver a entrada [0, 0].
Com o bias conseguimos ajustar o limite da decisão e chegar a zero erros.
Assim ficou mais claro para mim como o modelo aprende com cada tentativa.
