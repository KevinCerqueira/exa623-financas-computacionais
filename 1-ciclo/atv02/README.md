# EXA623 - FINANÇAS COMPUTACIONAIS
## Atividade 01 – Criação de EA’s e instalação no MT5

**Alunos:**
- Aurelio Barreto (aurelionadjabarreto@gmail.com)
- Kevin Cerqueira Gomes (kevingomes.uefs@gmail.com)

**Instituição:** Engenharia de Computação - Universidade Estadual de Feira de Santana (UEFS)

**Localização:** Caixa Postal 252 e 294 – 44.036-900 – Feira de Santana – BA – Brasil

#### Todos os arquivos que geramos e foram utilizados nesse documento (além de outros que não estão presentes neste documento) estão no drive: [abrir](https://drive.google.com/drive/folders/1y7krsa3FRiPJ-hLfv04jMX30HmyGWBMh?usp=drive_link)

## Diário (Swing Trade) - Símbolo escolhido: EURUSD Forex

### Monte Carlo

- Estratégia 01 (EA1):
![EA1MC](forex/(EURUSD)%20EA1%20-%20Gráfico%20Monte%20Carlo.png)

- Estratégia 02 (EA2):
![EA2MC](forex/(EURUSD)%20EA2%20-%20Gráfico%20Monte%20Carlo.png)

### Relatórios

- Relatório de desempenho do Backtest da EA1: [abrir](https://drive.google.com/file/d/1gdJTmM_DUPGEEq1ez0mqKZBZWNfVCiLV/view?usp=drive_link)
- Relatório de desempenho do Backtest da EA2: [abrir](https://drive.google.com/file/d/1qU2oj6Ou0HfmxZejAS7mgFq82i_ZPq3U/view?usp=drive_link)
- Arquivo de configuração do SQX: [abrir](https://drive.google.com/file/d/1R46-IULtlkGko3R6j3Ysihr4uWa6JBTR/view?usp=drive_link)
- Arquivo de configuração do Retest do SQX: [abrir](https://drive.google.com/file/d/1iIz-OHVWrbQEC37sYEnkBIkBn4dKzwqM/view?usp=drive_link)
- Codigo-fonte da EA1: [abrir](https://drive.google.com/file/d/1JVBs4HGGERA8nedY3SSZ0jcq1fgf4zSX/view?usp=drive_link)
- Codigo-fonte da EA2: [abrir](https://drive.google.com/file/d/1nW7N1XqwQPla8RoQw7ioXvrI3ZHyIhxA/view?usp=drive_link)

### EAs no MT5 (compilado)
- EA1:
![EA1MT5](forex/(EURUSD)%20MTQ5%20-%20EA1%20-%20Codigo%20Importado%20no%20MetaEditor.png)

- EA2:
![EA2MT5](forex/(EURUSD)%20MTQ5%20-%20EA2%20-%20Codigo%20Importado%20no%20MetaEditor.png)


### Stop Loss (SL) e Take Profit (TP):
**Stop Loss (SL):**
- Base em Pips: entre 30 e 150 pips.
- Base em porcentagem: entre 0.7% e 1.5%.

Isso significa que o Stop Loss pode ser configurado para acionar uma venda (ou compra) quando o preço se mover uma certa quantidade de pips ou uma certa porcentagem em relação ao ponto de entrada do trade.

**Take Profit (TP):** 
- Base em Pips: entre 50 e 400 pips.
- Base em porcentagem: entre 0.9% e 3%.
- Limite da relação risco-retorno: entre 100% e 300%.

Isso significa que o Take Profit pode ser configurado para acionar uma venda (ou compra) quando o preço se mover uma certa quantidade de pips, uma certa porcentagem em relação ao ponto de entrada do trade, ou quando a relação risco-retorno atingir um determinado limite.

### Análise Inicial dos Códigos
Ambos os códigos (EA1 e EA2) incluem bibliotecas padrão do MetaTrader 5 e parecem seguir uma estrutura similar, dada a origem comum do StrategyQuant X. Vamos focar em identificar como são implementadas as estratégias e as configurações de Stop Loss.

#### Primeiros Passos da Análise
- Incluir bibliotecas relevantes: Os códigos importam bibliotecas padrão para criar Experts no MetaTrader 5.
- Estrutura do Expert Advisor: A estrutura inicial inclui propriedades do EA e configurações básicas.

#### Estratégias
A função principal que implementa a lógica de trading é OnTick(). Essa função é chamada a cada tick de preço e contém a lógica para verificar condições de entrada e saída de trades. A função OnTick() está presente em ambos os códigos.

```c
void OnTick() {

   //--- Do we have enough bars to work with?
   if(Bars(_Symbol,_Period) < minBars) {   // if total bars is less than minBars
      Alert(StringFormat("NOT ENOUGH DATA: Less Bars than %d", minBars));
      return;
   }

   //--- Get the details of the latest 2 bars
   if(CopyRates(_Symbol, _Period, 0, 2, mrate) < 2) {
      Alert("Error copying rates/history data - error:", GetLastError(), "!!");
      ResetLastError();
      return;
   }
   
   IndicatorLoadedWithoutError = true;
   ZeroMemory(mrequest);      // Initialization of mrequest structure
 
   if(!timerInitialized) initTimer();

   checkBarOpen();
   
   if(sqDisplayInfoPanel) {
      sqTextFillOpens();
      if(_sqIsBarOpen) {
         sqTextFillTotals();   
      }  
   }
    
   sqManagePositions(MagicNumber);
   
   openingOrdersAllowed = sqHandleTradingOptions();
   
   ulong _ticket;                    
   double openPrice;  
   double sl, pt;
   double size;
   .
   .
   .
```

## Intraday (Day Trade) - Símbolo escolhido: BTCUSD Crypto

### Monte Carlo

- Estratégia 01 (EA1):
![EA1MC](crypto/(BTCUSD)%20EA1%20-%20Gráfico%20Monte%20Carlo.png)

- Estratégia 02 (EA2):
![EA2MC](crypto/(BTCUSD)%20EA2%20-%20Gráfico%20Monte%20Carlo.png)

### Relatórios

- Relatório de desempenho do Backtest da EA1: [abrir](https://docs.google.com/spreadsheets/d/1niWo377gboZSR4gk5ku-tvamajQJCgLp/edit?usp=drive_link&ouid=104297309265572510054&rtpof=true&sd=true)
- Relatório de desempenho do Backtest da EA2: [abrir](https://docs.google.com/spreadsheets/d/17ZOizdeUgOv8qpvnk7oEjvJHew6Z5fgX/edit?usp=drive_link&ouid=104297309265572510054&rtpof=true&sd=true)
- Arquivo de configuração do SQX: [abrir](https://drive.google.com/file/d/1ebzNyXa7wWSc-5Ou2o-3ByhHFYnguUG_/view?usp=drive_link)
- Arquivo de configuração do Retest do SQX: [abrir](https://drive.google.com/file/d/1FuxxPeBixdVAVQKiwVMj6PHCDqtD3noD/view?usp=drive_link)
- Codigo-fonte da EA1: [abrir](https://drive.google.com/file/d/13yzwHW5BJ0ACkl4hW0AKkpE5xEbNlL3R/view?usp=drive_link)
- Codigo-fonte da EA2: [abrir](https://drive.google.com/file/d/1VZDKPNWpPRBRKaougmrbVa9Uxwvst8B1/view?usp=drive_link)

### EAs no MT5 (compilado)
- EA1:
![EA1MT5](crypto/(BTCUSD)%20MTQ5%20-%20EA1%20-%20Código%20importado%20no%20MetaEditor.png)

- EA2:
![EA2MT5](crypto/(BTCUSD)%20MTQ5%20-%20EA2%20-%20Código%20importado%20no%20MetaEditor.png)


### Stop Loss (SL) e Take Profit (TP):
**Stop Loss (SL):**
- Base em Pips/Ticks: entre 30 e 80 pips/ticks.
- Base em porcentagem: entre 0.7% e 1.2%.

**Take Profit (TP):** 
- Base em Pips/Ticks: entre 50 e 180 pips/ticks.
- Base em porcentagem: entre 0.9% e 2.5%.
- Limite da relação risco-retorno: 10.

### Estratégias
Essas estratégias analisam condições específicas, utilizando períodos de indicadores que variam de 5 a 200, e aplicam regras simétricas para entrada e saída de trades. O gerenciamento de risco é feito através de Stop Loss configurados entre 30 e 80 pips/ticks ou 0.7% a 1.2%, e Take Profit entre 50 e 180 pips/ticks ou 0.9% a 2.5%. A função principal OnTick() verifica a suficiência de dados históricos e executa a lógica de trading conforme as condições predefinidas, garantindo operações seguras e estruturadas.

```c
void OnTick() {
   //--- Do we have enough bars to work with?
   if(Bars(_Symbol,_Period) < minBars) {   // if total bars is less than minBars
      Alert(StringFormat("NOT ENOUGH DATA: Less Bars than %d", minBars));
      return;
   }
}
   .
   .
   .
```

