# Introdução
## Porque precisamos de Threads ?
- Capacidade de resposta
- Performance

##### **Capacidade de resposta**
Exemplos de baixa capacidade de resposta
- Aguardar por uma resposta de cliente
- Resposta atrasada para uma solicitação
- Aplicações sem feedback

Com multithreading conseguimos atender diversas requisições simultaneamente
distribuindo essas requisições em threads diferentes.
Para multiplas tarefas ocorrendo em paralelo, podemos utilizar multiplos threads, um
para cada tarefa.Para alcançar isso Não é necessário multiplos core, conseguimos apenas com um.

##### **Performance**
Podemos criar a ilusão de multiplas tarefas acontecendo em paralelo utilizando apenas um core do processador.
Com múltiplos cores podemos executar tarefas tarefas completamente em paralelo.

Impactos positivos de uma alta performance
- Completar tarefas com velocidade
- Finalizar várias tarefas no mesmo período
- Escalar serviços
  * Menor quantidade de máquinas
  * Menor custo de hardware
  * Melhorar custo/benefício de infraestrutura