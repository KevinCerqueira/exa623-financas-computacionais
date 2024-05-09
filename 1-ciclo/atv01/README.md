# EXA623 - FINANÇAS COMPUTACIONAIS
## Atividade 01 – Criação de EA’s e instalação no MT5

**Alunos:**
- Aurelio Barreto (aurelionadjabarreto@gmail.com)
- Kevin Cerqueira Gomes (kevingomes.uefs@gmail.com)

**Instituição:** Engenharia de Computação - Universidade Estadual de Feira de Santana (UEFS)

**Localização:** Caixa Postal 252 e 294 – 44.036-900 – Feira de Santana – BA – Brasil

#### Todos os arquivos que geramos e foram utilizados nesse documento estão no drive: [abrir](https://drive.google.com/drive/folders/1NqI2BnjuykKXhf3ce2kiEnVFhyYdnZ-u?usp=drive_link)

## Diário (Swing Trade) - Símbolo escolhido: EURUSD Forex
- Relatório da Estratégia do SQX: [abrir](https://drive.google.com/file/d/1UoJUxhqdtcDYlAnyQK0larPsjtEZ6dQE/view?usp=drive_link)

### Sumário das Configurações no SQX

![Resumo das configuracoes no SQX](forex/(EURUSD)%20SQX%20-%20Resumo%20das%20Configuracoes.png)

#### Stop Loss (SL) e Take Profit (TP):

![Configurações SL e TP](forex/(EURUSD)%20SQX%20-%20Configuracoes%20SL%20e%20TP.png)
**Stop Loss (SL):**  
O SL é configurado com uma faixa de 30 a 150 pips, correspondendo a uma perda percentual de 0,7% a 1,5% do valor total da conta. Esta faixa de pips foi escolhida para balancear a proteção contra movimentos de mercado adversos com a necessidade de permitir que as operações desenvolvam seu potencial em tendências mais prolongadas, característica comum no swing trading.

**Take Profit (TP):**  
O TP é estabelecido entre 50 a 400 pips, o que traduz-se em um ganho percentual de 0,9% a 3% do valor da conta. A relação risco-recompensa é mantida em um limite de 100% a 300%, procurando assegurar que os lucros sejam significativamente maiores que os riscos assumidos, em linha com as expectativas de ganhos em operações de swing trade, que muitas vezes enfrentam maiores incertezas e períodos de espera.

### Arquivos
- Arquivo de configurações (.cfx): [abrir](https://drive.google.com/file/d/1MPgBxUPxrMpbXqIouMCkYXF-R0A2N9P8/view?usp=drive_link)
- Código Fonte (.mq5): [abrir](https://drive.google.com/file/d/1XCBIPbyaBm_YNniASZnFbtamlTkOPtAA/view?usp=drive_link)
- Código Fonte importado e compilado no MetaEditor do MTQ5: ![Código Importado no MetaEditor](forex/(EURUSD)%20MTQ5%20-%20Codigo%20Importado%20no%20MetaEditor.png)

### Testes
#### Testes no SQX (Backtest)
- Lista de Trades: [abrir](https://docs.google.com/spreadsheets/d/1AzNZIIGaBcVdwiBlLjPT6c42nya-ab8X/edit?usp=drive_link&ouid=104297309265572510054&rtpof=true&sd=true)
- Visão Geral: ![Visao Geral](forex/(EURUSD)%20SQX%20-%20Backtest%20-%20Visao%20Geral.png)
- Gráfico de Capital: ![Grafico de Capital](forex/(EURUSD)%20SQX%20-%20Backtest%20-%20Grafico%20de%20Capital.png)
- Análise de Negociação: ![Analise de Negociacao](forex/(EURUSD)%20SQX%20-%20Backtest%20-%20Analise%20de%20Negociacao.png)

#### Testes no MTQ5
##### Relatórios de Teste MTQ5
- Relatório dos Testes em XLSX: [abrir](https://docs.google.com/spreadsheets/d/1EmXm_6UU4cYK28AssymDLVanGhQUk0q4/edit?usp=drive_link&ouid=104297309265572510054&rtpof=true&sd=true)
- Tela principal: ![Tela Principal](forex/(EURUSD)%20MTQ5%20-%20Tela%20Principal.png)
- Resumo Geral: ![Resumo Geral](forex/(EURUSD)%20MTQ5%20-%20Testes%20-%20Resumo%20Geral.png)

##### Gráficos do Teste MTQ5
- Aba Gráfico: ![Aba Gráfico](forex/(EURUSD)%20MTQ5%20-%20Grafico%20do%20Teste%20-%20Aba%20Grafico.png)
- Entradas: ![Entradas](forex/(EURUSD)%20MTQ5%20-%20Grafico%20do%20Teste%20-%20Entradas.png)
- Tempos: ![Tempos](forex/(EURUSD)%20MTQ5%20-%20Grafico%20do%20Teste%20-%20Tempos.png)

<!-- ############################################################################## -->

## Intraday (Day Trade) - Símbolo escolhido: BTCUSD Crypto
- Relatório da Estratégia no SQX: [abrir](https://docs.google.com/spreadsheets/d/1776oM_xh7pho-Gap0OaiYmhkZmzHdRP4/edit?usp=drive_link&ouid=104297309265572510054&rtpof=true&sd=true)

### Sumário das Configurações no SQX

![Resumo das configuracoes no SQX](crypto/(BTCUSD)%20SQX%20-%20Resumo%20das%20Configuracoes.png)

#### Stop Loss (SL) e Take Profit (TP):

![Configurações SL e TP](crypto/(BTCUSD)%20SQX%20-%20Configuracoes%20SL%20e%20TP.png)
**Stop Loss (SL):**  
Com a quantidade de pips/ticks variando de 10 a 30, o que corresponde a uma perda percentual aproximada de 0,5% a 1,2% do valor total da conta. Esta configuração é projetada para minimizar as perdas em caso de movimentos de mercado contrários às posições abertas, limitando efetivamente o risco em um ambiente de alta volatilidade típico do day trading.

**Take Profit (TP):**  
Com uma variação de 10 a 50 pips/ticks, equivalendo a um ganho percentual de 0,7% a 2,5% do valor da conta. A relação risco-retorno é limitada a 100, o que significa que o EA busca alcançar um retorno que seja pelo menos igual ao risco assumido por operação, mas com potencial para alcançar até 2,5 vezes o valor arriscado.

### Arquivos
- Arquivo de configurações (.cfx): [abrir](https://drive.google.com/file/d/1HX7a5CdKxauK1wYDzXJs1vKD9mer2cIB/view?usp=drive_link)
- Código Fonte (.mq5): [abrir](https://drive.google.com/file/d/1Qng679bpBIb5YgcVjGwC8Sumh2xGrVC8/view?usp=drive_link)
- Código Fonte importado e compilado no MetaEditor do MTQ5: ![Código Importado no MetaEditor](crypto/(BTCUSD)%20MTQ5%20-%20Codigo%20Importado%20no%20MetaEditor.png)

### Testes
#### Testes no SQX (Backtest)
- Lista de Trades: [abrir](https://docs.google.com/spreadsheets/d/1g_4eDAl3MacIrDoHtPCOWQpLhntAaD6X/edit?usp=drive_link&ouid=104297309265572510054&rtpof=true&sd=true)
- Visão Geral: ![Visao Geral](crypto/(BTCUSD)%20SQX%20-%20Backtest%20-%20Visao%20Geral.png)
- Gráfico de Capital: ![Grafico de Capital](crypto/(BTCUSD)%20SQX%20-%20Backtest%20-%20Grafico%20de%20Capital.png)
- Análise de Negociação: ![Analise de Negociacao](crypto/(BTCUSD)%20SQX%20-%20Backtest%20-%20Analise%20de%20Negociacao.png)

#### Testes no MTQ5
##### Relatórios de Teste MTQ5
- Relatório dos Testes em XLSX: [abrir](https://drive.google.com/file/d/1bYgUNhp8WTZH4Mce5QYvMaMHYbE6m6DO/view?usp=drive_link)
- Tela principal: ![Tela Principal](crypto/(BTCUSD)%20MTQ5%20-%20Tela%20Principal.png)
- Resumo Geral: ![Resumo Geral](crypto/(BTCUSD)%20MTQ5%20-%20Testes%20-%20Resumo%20Geral.png)

##### Gráficos do Teste MTQ5
- Aba Gráfico: ![Aba Gráfico](crypto/(BTCUSD)%20MTQ5%20-%20Grafico%20do%20Teste%20-%20Aba%20Grafico.png)
- Entradas: ![Entradas](crypto/(BTCUSD)%20MTQ5%20-%20Grafico%20do%20Teste%20-%20Entradas.png)
- Tempos: ![Tempos](crypto/(BTCUSD)%20MTQ5%20-%20Grafico%20do%20Teste%20-%20Tempos.png)

