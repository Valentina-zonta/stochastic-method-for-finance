# Metodi Stocastici per la Finanza: Report e Analisi

Questo repository contiene una raccolta di report e analisi su temi fondamentali della finanza quantitativa. Ogni report affronta un problema specifico, dall'option pricing alla gestione del rischio, applicando modelli teorici e confrontandoli con dati di mercato reali.

## 📚 Sommario dei Report

Ecco una breve descrizione del contenuto di ciascun report:

### Report 1: One-Period Binomial Model
* **Obiettivo:** Prezzare una call option sull'asset Supermicro (SMCI) usando il modello binomiale a un periodo.
* **Metodologia:** Il modello viene applicato a opzioni con scadenza a 3 e 6 mesi. La volatilità storica viene calcolata e usata per trovare il prezzo teorico, che viene poi confrontato con il prezzo di mercato.
* **Risultato:** L'analisi evidenzia i limiti di un modello così semplice, mostrando un errore significativo (23-24%) rispetto ai prezzi reali.

### Report 2: Calcolo dei Dividendi (Box-Spread & Put-Call Parity)
* **Obiettivo:** Tentare di calcolare i dividendi impliciti nelle opzioni di Morgan Stanley (MS).
* **Metodologia:** Vengono applicate due tecniche: la strategia **Box-Spread** e la **Put-Call Parity**.
* **Risultato:** I risultati sono inaspettati (es. dividendi negativi). Questo report dimostra un'importante lezione pratica: i modelli teorici (validi per opzioni Europee) falliscono se applicati erroneamente a opzioni Americane, come quelle usate nell'analisi.

### Report 3: Convergenza dei Modelli di Pricing
* **Obiettivo:** Confrontare la velocità di convergenza di diversi modelli di pricing discreto rispetto alla formula analitica di Black-Scholes.
* **Metodologia:** Vengono messi a confronto il **Modello Binomiale N-step** e il **Modello Leisen-Reimer (L-R)**.
* **Risultato:** Entrambi i modelli convergono al prezzo di Black-Scholes all'aumentare del numero di passi (N). Tuttavia, si dimostra che il modello Leisen-Reimer è molto più efficiente, convergendo più rapidamente e con maggiore precisione.

### Report 4: Analisi delle "Greche"
* **Obiettivo:** Calcolare, visualizzare e analizzare le "Greche" (Delta, Gamma, Vega, Theta, Rho), ovvero le sensibilità del prezzo di un'opzione.
* **Metodologia:**
    1.  **Teoria:** Vengono generate superfici 3D per ogni Greca usando le formule di Black-Scholes (tramite VBA).
    2.  **Pratica:** Si analizzano i dati di mercato reali (da Refinitiv) per l'asset Adyen NV (ADYEN.AS), mostrando il fenomeno dell'"implied volatility smile".
* **Risultato:** I valori teorici calcolati vengono confrontati con i dati di mercato, analizzando le differenze.

### Report 5: Metodi Monte Carlo per l'Option Pricing
* **Obiettivo:** Utilizzare metodi di simulazione Monte Carlo (MC) per prezzare diverse tipologie di opzioni.
* **Metodologia:** Sfruttando simulazioni basate sul Moto Browniano Geometrico (GBM), vengono prezzate:
    * **Opzioni Vanilla:** Confrontando il risultato MC con Black-Scholes.
    * **Opzioni Esotiche (Path-Dependent):** Opzioni Asiatiche e Opzioni Lookback.
    * **Certificati:** Viene prezzato un certificato "Worst-Of" su un paniere di 3 asset (NVDA, MSFT, GOOGL).

### Report 6: Analisi del Value at Risk (VaR)
* **Obiettivo:** Calcolare e confrontare diverse metodologie per la stima del Value at Risk (VaR).
* **Portafoglio:** Un portafoglio bilanciato composto da McDonald's (MCD) e Yum! Brands (YUM).
* **Metodologia:** Il VaR viene calcolato utilizzando 5 approcci distinti:
    1.  Parametrico Normale (sigma flat)
    2.  Parametrico Normale (con volatilità EWMA)
    3.  Simulazione Monte Carlo
    4.  VaR Storico
    5.  Simulazione Storica
* **Risultato:** Oltre al confronto, l'analisi investiga la **subadditività**, dimostrando come il VaR del portafoglio non sia sempre inferiore alla somma dei VaR individuali, evidenziando un limite noto di questa metrica di rischio.

## 🛠️ Strumenti Utilizzati

* **VBA (Visual Basic for Applications)** per l'implementazione dei modelli in Excel.
* **Python** (probabilmente con `pandas`, `numpy`, `matplotlib`) per le analisi VaR e la generazione dei grafici.
* **Refinitiv Eikon** come fonte per i dati di mercato.
