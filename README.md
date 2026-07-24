# Note & configurazioni SAP — e-Invoicing B2B per paese

Portale statico che raccoglie, **paese per paese**, le **Note SAP di implementazione** per l'e-invoicing
B2B **on-premise** (SAP Document and Reporting Compliance / eDocument su S/4HANA on-premise o ECC):

- la **nota centrale** (*Installation / Implementation Overview*);
- **tutte le note da installare** collegate (framework, soluzione, legal change, correzioni);
- la **guida alle attività di customizing** (Configuration Guide allegata alla nota centrale,
  KBA di configurazione/troubleshooting, attività IMG in SPRO, SAP Help Portal).

I dati provengono dal **SAP for Me — Knowledge Base** (Note SAP), verificati manualmente.
Il dataset (`data/countries_sap.json`) è la stessa base del file Excel `SAP_B2B_eInvoicing_Notes.xlsx`.

## Struttura

```
index.html               sito (single page, nessun build step)
data/countries_sap.json  dataset: paesi, nota centrale, guida customizing, note da installare
data/meta.json           metadati (ultima verifica, conteggi)
```

## Avvertenze

- Ambito: **on-premise** (S/4HANA on-prem / ECC). Nelle edizioni **Cloud** non si installano note.
- L'**elenco esatto** da installare, con la sequenza e i prerequisiti, va risolto con **SNOTE**
  in base a release e Support Package del sistema: la nota centrale resta la fonte di verità.
- **Oman** e **Filippine**: SAP non ha ancora rilasciato una soluzione eDocument dedicata.
- Non costituisce consulenza. I numeri delle note sono soggetti ad aggiornamento da parte di SAP.

---
Design coerente con gli altri due portali (E-Invoicing Tracker · eArchiving). Autore: Fabrizio Ticino.
