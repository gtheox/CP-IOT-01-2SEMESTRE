# RM555962 Gabriel Teodoro Gonçalves Rosa
# RM558123 Luka Ura Shibuya
# RM555030 Eduardo Ribeiro Giovannini

Aqui está as questões escreitas contendo  informações detalhadas do dataset.

- Questão 2
Resposta: Global_active_power: é a potência ativa consumida (energia efetivamente usada pelos aparelhos) e Global_reactive_power: é a potência reativa, associada a campos magnéticos (como em motores, transformadores). Não realiza trabalho útil, mas circula na rede.
PARTE 4 - Exercícios no Orange Data Mining(Iremos comentar os passos a passos de cada ação)
- Questão 36
Resposta: No Orange, comecei carregando o dataset pelo widget CSV File Import. Depois conectei ao Data Table para enxergar as primeiras linhas. A tabela mostra várias variáveis como Date, Time, Global_active_power, Voltage, Global_intensity, Sub_metering_1, entre outras.Ao observar, dá para notar que o dataset tem milhões de registros, pois ele contém medições minuto a minuto durante vários anos. As variáveis numéricas já aparecem reconhecidas corretamente, enquanto as colunas de data/hora podem precisar de tratamento extra dependendo da análise.
- Questão 37
Resposta: Depois usei o widget Sample Data e configurei para pegar apenas 1% da base. Essa amostra, apesar de pequena, ainda tem milhares de registros, então continua sendo representativa. Conectando ao Distribution (variável Global_active_power), percebi que o formato do histograma da amostra é muito parecido com o da base completa. Ou seja, mesmo com 1% dos dados, a distribuição não se altera muito: a maior parte dos valores fica em torno de consumos baixos, com alguns picos. Isso mostra que a amostragem preserva a característica da base.
- Questão 38
Resposta: Usei o widget Distribution especificamente para visualizar Global_active_power. O histograma confirma que o consumo é concentrado em valores baixos (a maior parte abaixo de 2 kW). Há registros com valores bem mais altos, mas em menor quantidade — são os “picos” de consumo, provavelmente em horários de maior uso de aparelhos elétricos. Isso indica que, em geral, o consumo das residências é moderado, mas existem momentos de uso intenso que puxam a curva para a direita.
- Questão 39
Resposta: No Scatter Plot, configurei Voltage no eixo X e Global_intensity no eixo Y. O gráfico mostra uma tendência clara de correlação positiva: à medida que a intensidade (corrente elétrica) aumenta, também há variação associada na tensão. Os pontos não ficam em uma linha reta perfeita, mas a nuvem de dados sugere que existe relação direta entre as duas variáveis.Isso faz sentido do ponto de vista físico: maior intensidade de corrente está ligada a maior potência consumida, e isso impacta a rede elétrica.
- Questão 40

Resposta: Apliquei o widget k-Means configurado com 3 clusters, usando as variáveis Sub_metering_1, Sub_metering_2 e Sub_metering_3. Ao conectar ao Scatter Plot, os dados foram coloridos conforme os clusters encontrados. A interpretação é que cada cluster representa um padrão distinto de consumo doméstico. Por exemplo:
Um grupo pode ter consumo maior em Sub_metering_1 (cozinha, iluminação).
Outro grupo pode ser mais alto em Sub_metering_2 (aquecimento ou água quente).
O terceiro pode estar mais equilibrado entre os três submeterings. Ou seja, o K-Means conseguiu separar perfis de consumo diferentes, que podem representar comportamentos energéticos distintos das famílias.
