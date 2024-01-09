<h1 style="color:#0373fc">Introdução</h1>

<h2 style="color: #00bfa3">O que são Threads?</h2>
Thread (linha de execução) é uma sequência de instruções que faz parte de um processo principal.
Um software é organizado em processos. Cada processo é dividido em threads, que formam tarefas independentes, mas
relacionadas entre si.
CPUs podem realizar multithreading simultâneo (SMT) para ter mais desempenho.

<h2 style="color: #00bfa3">Como funcionam os threads de um processador?</h2>
Os sistemas operacionais organizam as tarefas a serem executadas em processos,
divididos em um ou mais threads. Cada processo é uma sequência de instruções
que está ligada a um software. Se um processo está sendo executado por um
núcleo do processador, significa que o software ligado a ele está em execução.
<span style="color: #e0730d; font-weight: bold">Os threads formam conjuntos menores de instruções numa tarefa
maior</span>.
CPUs modernas suportam multithread (ou multithreading), conceito em que
<span style="color: #e0730d; font-weight: bold">dois ou mais threads são executados simultaneamente
para aumentar a eficiência do sistema</span>.
Para isso, <span style="color: #e0730d; font-weight: bold">cada thread é direcionado a um núcleo do processador</span>.

<span style="color: #e0730d; font-weight: bold">
Os núcleos físicos da CPU podem ainda ser divididos em núcleos virtuais por meio da técnica de SMT.
</span>

<h2 style="color: #00bfa3">O que é multithreading simultâneo (SMT)?</h2>
<span style="font-weight: bold">Multithreading simultâneo (SMT)</span> é uma técnica que permite que múltiplos threads
sejam executados simultaneamente,
por um único núcleo físico do processador. As CPUs seguem um fluxo de processamento sequencial de dados,
ao contrário da GPUs (chips para processamento gráfico), que podem ter até milhares de núcleos para permitir
processamento paralelo. Ao possibilitar a execução simultânea de vários threads, o SMT compensa essa limitação nas CPUs.
As técnicas de SMT fazem os núcleos físicos serem divididos em núcleos virtuais, cada um deles também chamado
de thread.
Assim, se um processador quad-core tiver dois threads por núcleos, ele terá quatro núcleos e oito threads.
Da mesma forma, um chip octa-core terá oito núcleos e 16 threads. Na implementação do SMT, a execução dos threads
não é exatamente simultânea. Os núcleos físicos fazem seu trabalho de modo sequencial, mas alternam tão rapidamente
entre os threads que é como se a execução deles ocorresse simultaneamente.
Nem sempre a quantidade de threads equivale ao dobro do número de núcleos. Nos chips Core de 12ª geração e sucessores, a
Intel implementou dois threads somente nos núcleos de alto desempenho, deixando os núcleos de eficiência energética(
menos potentes) com um thread cada.

<h2 style="color: #00bfa3">Qual é a diferença entre thread e processo?</h2>
Um processo é uma sequência de instruções que corresponde a um software ativo. 
Cada processo ocupa um espaço individual de memória que contém os dados necessários para
a sua execução. Um software pode gerar mais de um processo, com todos eles sendo
vinculados a um processo principal.
Já um thread é um segmento de um processo, como se formasse uma sub-tarefa. 
Nos sistemas operacionais convencionais, um processo sempre tem um ou mais threads. Essa abordagem melhora o aproveitamento de recursos da CPU e otimiza o fluxo de execução de instruções, dando mais eficiência à operação.

<h2 style="color: #00bfa3">Quais são as vantagens das threads em computação?</h2>
- Aumento de velocidade: a divisão de tarefas em threads é um método de paralelismo que otimiza o fluxo de instruções a serem executadas, contribuindo para o aumento de desempenho da CPU;
- Maior eficiência: o uso de threads diminui o risco de núcleos ficarem ociosos à espera de dados ou instruções;
- Compartilhamento de recursos: como os threads estão relacionados em si, eles compartilham determinados recursos, como endereçamento de memória e dados específicos;
- Controle de custos: a abordagem dos threads pode reduzir os custos de desenvolvimento de um chip porque a otimização do fluxo de execução elimina a necessidade de mais núcleos físicos.
- Escalar serviços
  * Menor quantidade de máquinas;
  * Menor custo de hardware;
  * Melhorar custo/benefício de infraestrutura.
Com multithreading conseguimos atender diversas requisições simultaneamente
distribuindo essas requisições em threads diferentes.
Para multiples tarefas ocorrendo em paralelo, podemos utilizar múltiplos threads, um
para cada tarefa. Para alcançar isso Não é necessário múltiplo core, conseguimos apenas com um.
Podemos criar a ilusão de múltiplas tarefas acontecendo em paralelo utilizando apenas um core do processador.
Com múltiplos cores podemos executar tarefas completamente em paralelo.

