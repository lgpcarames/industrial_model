# industrial_model


São apresentados dados de sensores que, inicialmente, possuem intervalos com medidas bem definidos e intervalos uniformes. Porém, como qualquer problema real, possui ruídos passíveis de tratamento. Para realizarmos construímos uma classe DataSensor para armazenar os dados da primeira parte de maneira eficaz e fornecendo os métodos necessários para tratar os dados e também para realizar o filtro. Para o filtro, definimos duas estratégias: 
1. Reconhecer e utilizar os harmônicos, no domínio da frequẽncia, de maior amplitude em ordem para a conversão para o sinal no domínio do tempo.
2. Utilizar um threshold em referência ao harmônico de maior amplitude, onde este threshold vai de 0 até 1. Para valores em que o threshold é 0, todos os harmônicos no domínio da frequência são utilizados na composição do sinal, logo, não há filtro, caso o threshold seja 1, apenas o harmônico de maior amplitude será considerado.


Já num segundo momento, temos uma situação um pouco diferente, possuímos duas bases de dados, uma com especificações de equipamentos ao qual um sensor foi acoplado. O sensor faz uma medida de cada componente da velocidade e aceleração a cada x segundos, após um intervalo y, o sensor armazenará em uma base de dados os valores quadráticos médios (RMS) de cada componente armazenadas ao longo do intervalo da medição, o valor da temperatura também é obtido.

Esse experimento possibilitou obter uma base de dados onde a distribuição do tempo das amostras não é uniforme. Ao final, devemos criar uma função que possibilite calcular o tempo de _downtime_, _uptime_ e também identificar o padrão das vibrações de modo a poder identificar se uma máquina está próxima de uma possível falha.
