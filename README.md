# Tarefas

1. **Parte 1: Implementação de um Latch RS com Clock**
   - Criação de um circuito de trava RS com clock (gated RS latch) em VHDL, utilizando tabelas de consulta (LUTs) de 4 entradas em um FPGA. O objetivo é demonstrar como criar elementos de armazenamento sem utilizar flip-flops dedicados.

2. **Parte 2: Implementação de um Latch D com Clock**
   - Implementação de um latch D com clock (gated D latch) utilizando portas NAND. Esta etapa expande a funcionalidade para incluir um latch D, proporcionando um entendimento maior dos circuitos de armazenamento.

3. **Parte 3: Implementação de um Flip-Flop Master-Slave**
   - Implementação de um flip-flop master-slave de onda de subida (rising edge) em VHDL. Esta tarefa foca na criação de flip-flops que utilizam uma configuração master-slave para capturar e armazenar dados na borda de subida do clock.

4. **Parte 4: Implementação de um Circuito Combinado**
   - Criação de um circuito que combina um latch gated D com dois flip-flops master-slave, um de onda de subida (rising edge) e outro de onda de descida (falling edge). Este circuito finaliza a tarefa ao integrar diferentes tipos de elementos de armazenamento em um único design.



## Resumo da Tarefa  1

Esta tarefa envolve a criação e simulação de um circuito de trava (latch) RS com clock usando FPGA, especificamente utilizando o software Quartus da Intel. O objetivo é demonstrar como elementos de armazenamento podem ser criados em um FPGA sem utilizar flip-flops dedicados.

## Parte I: Descrição do Latch RS com Clock

Na primeira parte, é apresentado um circuito de trava RS com clock (gated RS latch), como mostrado na Figura 1. O circuito é descrito em VHDL usando expressões lógicas, conforme o código fornecido na Figura 2. Esse código utiliza portas lógicas para implementar o latch RS em uma FPGA que possui tabelas de consulta (LUTs) de 4 entradas.

### Implementação com LUTs

Embora o latch possa ser implementado corretamente em uma única LUT de 4 entradas, isso não permite a observação dos sinais internos (`R_g` e `S_g`). Para resolver isso, é utilizada uma diretiva do compilador Quartus chamada `KEEP`, que garante que cada sinal interno seja preservado e implementado em elementos lógicos separados. O resultado final é um circuito com quatro LUTs de 4 entradas, como mostrado na Figura 3b.

## Resumo da tarefa 2

Nesta tarefa, a partir da análise de um Latch D fornecido, foi solicitado que fosse implementado no Quartus/VHDL, executado na placa FPGA e analisado sua simulação no Modelsim.

## Parte I: Análise do Latch D fornecido

O latch D fornecido é implementado apenas com portas NAND e possui comportamento semelhante ao Latch da tarefa 1.

## Parte II: Implementação no Quartus/VHDL

A implementação foi realizada de duas formas. 
A primeira resume-se em desenvolver um código VHDL com base no fornecido para o Latch da tarefa 1, ou seja, foram feitas modificações na lógica de implementação do primeiro código para que o funcionamento fosse transformado para o latch D.
Já a segunda, foi feita através da implementação em circuito esquemático e, então, convertido em bloco de VHDL por meio das ferramentas do Quartus.

## Parte III: Execução na placa FPGA

A placa utilizada foi a placa V. Dessa forma, foram construídos as correspondências na seção 'Assignments 
