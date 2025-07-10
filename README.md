# Portfolio Tracker - SPY & QQQM

Un'applicazione web per monitorare in tempo reale il tuo portfolio di ETF con supporto per trading con leva.

## 📋 Caratteristiche

- **Monitoraggio in tempo reale** dei prezzi di SPY e QQQM
- **Calcolo automatico** di profitti e perdite (P&L)
- **Supporto leva x2** con visualizzazione del capitale effettivamente investito
- **Interfaccia dark mode** moderna e responsive
- **Aggiornamento manuale** dei prezzi con un click
- **Visualizzazione dettagliata** per ogni ETF nel portfolio

## 🚀 Come Utilizzare

1. **Apertura**: Apri il file `index.html` in qualsiasi browser moderno
2. **Caricamento automatico**: I prezzi vengono caricati automaticamente all'apertura
3. **Aggiornamento manuale**: Clicca sul pulsante "🔄 Aggiorna Prezzi" per aggiornare i dati

## 📊 Portfolio Configurato

Il portfolio include:

### SPY (SPDR S&P 500 ETF)
- **Azioni**: 8
- **Prezzo di acquisto**: $620.75
- **Capitale investito**: $2,483.00 (con leva x2)

### QQQM (Invesco NASDAQ 100 ETF)
- **Azioni**: 20
- **Prezzo di acquisto**: $227.25
- **Capitale investito**: $2,272.50 (con leva x2)

## 🔧 Configurazione

### API Key
L'applicazione utilizza Alpha Vantage per ottenere i prezzi in tempo reale. La API key è già configurata nel codice:
```javascript
const API_KEY = '38BQV3E3454Q2ITF';
```

⚠️ **Nota**: La versione gratuita di Alpha Vantage ha un limite di 5 chiamate API al minuto.

### Modifica del Portfolio
Per modificare le posizioni, edita l'oggetto `portfolio` nel codice JavaScript:

```javascript
const portfolio = {
    SPY: {
        shares: 8,          // Numero di azioni
        buyPrice: 620.75,   // Prezzo di acquisto
        // ... altri campi calcolati automaticamente
    },
    QQQM: {
        shares: 20,
        buyPrice: 227.25,
        // ...
    }
};
```

## 📱 Responsive Design

L'interfaccia si adatta automaticamente a:
- Desktop
- Tablet
- Smartphone (ottimizzata per schermi < 480px)

## 🎨 Interfaccia Utente

### Riepilogo Portfolio
- **Capitale Investito**: Mostra il capitale effettivo con indicazione della leva x2
- **Valore Totale**: Valore corrente di mercato del portfolio
- **P&L Totale**: Profitti/perdite con percentuale

### Card ETF
Ogni ETF mostra:
- Simbolo e valore attuale
- Numero di azioni possedute
- Prezzo di acquisto e prezzo corrente
- Capitale investito (con leva x2)
- P&L individuale con percentuale

### Indicatori Visivi
- **Verde** (#4ade80): Profitti
- **Rosso** (#f87171): Perdite
- **Blu** (#60a5fa): Informazioni leva e simboli ETF

## ⚡ Performance

- Delay di 1 secondo tra le chiamate API per evitare rate limiting
- Gestione errori per limiti API e connessione
- Caricamento asincrono dei dati

## 🛠️ Tecnologie Utilizzate

- **HTML5**: Struttura semantica
- **CSS3**: Styling moderno con gradients e animazioni
- **JavaScript ES6+**: Async/await, template literals
- **Alpha Vantage API**: Dati di mercato in tempo reale

## 📝 Note Importanti

1. **Leva x2**: Il capitale mostrato è la metà del valore totale della posizione
2. **Orari di mercato**: I prezzi si aggiornano solo durante gli orari di apertura del mercato USA
3. **Limite API**: Massimo 5 richieste al minuto con l'account gratuito
4. **Browser supportati**: Chrome, Firefox, Safari, Edge (versioni recenti)

## 🔒 Privacy e Sicurezza

- Nessun dato viene salvato o trasmesso a server esterni
- Tutti i calcoli avvengono localmente nel browser
- L'API key è utilizzata solo per recuperare i prezzi pubblici degli ETF

## 📄 Licenza

Questo progetto è fornito "così com'è" per uso personale. Sentiti libero di modificarlo secondo le tue esigenze.

## 🤝 Contributi

Per suggerimenti o miglioramenti, sentiti libero di modificare il codice secondo le tue necessità.
