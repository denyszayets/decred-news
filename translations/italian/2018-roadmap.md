# Roadmap di Decred per il 2018
È finalmente giunto il momento di pubblicare la roadmap di Decred per il 2018.

Il 2017 è stato un anno piuttosto movimentato sia per Decred che per l’intero panorama crypto, con tassi di cambio in aumento ed un crescente interesse da parte del settore finanziario tradizionale.

Decred ha continuato con il suo approccio alla ‘generare risultati prima di pubblicizzarli’, nonostante molti altri progetti simili nel settore continuassero a creare hype molto prima di aver ottenuto risultati concreti.

Abbiamo migliorato di gran lunga il nostro marketing negli ultimi mesi e ci aspettiamo di continuare su questo fronte per tutto il 2018.

Ecco un riassunto di ciò che abbiamo in serbo per il resto del 2018 e l’inizio del 2019:

* Supporto SPV Wallet — Invece di adottare il tipico approccio al servizio di wallet in cui i wallet si connettono ad un server centralizzato, abbiamo aggiunto il supporto per un meccanismo SPV appropriato che utilizza filtri compatti e funziona sulla rete P2P.
* Votazione Politeia — Il nostro sistema di proposte è in fase di completamento e consentirà agli utenti e agli stakeholder di avanzare proposte, dare pareri su ciò che viene o non viene finanziato e partecipare al processo decisionale a livello di progetto.
* Lightning Network — La maggior parte del lavoro di ‘porting’ di Lightning Labs’ lnd a Decred è stata completata e verrà rilasciata a breve.
* Rilascio della privacy iniziale — Il lavoro sulla privacy è iniziato sul serio e faremo una versione incrementale della privacy in cui rilasceremo il codice di lavoro e forniremo ulteriori informazioni sui nostri piani e approccio.
* Controllo decentralizzato dei fondi — Mentre la votazione Politeia sarà utilizzata per controllare il flusso dei fondi delle organizzazioni di sviluppo, creeremo nel frattempo uno smart contract che decentralizzerà completamente il controllo del fondo per lo sviluppo del progetto.
* Entità autonome decentralizzate — Usando un metodo simile a quello utilizzato per decentralizzare il controllo del fondo per lo sviluppo del progetto, consentiremo la creazione di DAEs su Decred chain.
* Ottimizzazioni della scalabilità: una varietà di modifiche, alcune delle quali sono modifiche del consenso, saranno necessarie per migliorare la scalabilità di Decred: es. un nuovo algoritmo di firma, supporto di sincronizzazione ‘multi-peer’ e impegni ‘header’.
* Integrazioni Decrediton — La GUI — graphical user interface, interfaccia grafica in italiano — Decrediton aggiungerà nuove integrazioni per supportare SPV, mobile, votazione Politeia e Lightning Network.
* Scambio decentralizzato: elaboreremo una proposta per uno scambio decentralizzato solo per criptovalute e la condivideremo pubblicamente.
* Marketing Growth — Decred ha presenziato a molte delle principali fiere sulle criptovalute e per il resto del 2018 continuerà con il proprio progetto di crescita marketing.
---
Discuteremo di seguito più in dettaglio gli aspetti della roadmap appena trattati:

## Timeline
Negli aggiornamenti precedenti della roadmap, abbiamo tentato di gestire le aspettative degli utenti fornendo stime rispetto alle date di completamento di ogni milestone, ad es. Q1 2018 succederà tal cosa. Ciò che è accaduto a seguito di questo tentativo è che una minoranza di utenti si lamentava costantemente e che utilizzava queste stime approssimative come pretesto e motivo per screditare il progetto. Se osserviamo come altre criptovalute e altri progetti software gestiscono le loro milestones, di norma notiamo che non viene inclusa una data specifica, ma piuttosto si ha una lista di milestones ancora da raggiungere. Dopo aver sperimentato le ‘ire’ di questi utenti in diverse occasioni, riteniamo che l’adozione di un approccio simile sia ideale, per cui le milestones sono elencate e sono contrassegnate come completati man mano che il lavoro viene eseguito.

## Supporto del portafoglio SPV
Molti progetti crypto non hanno puntato sulla creazione di un vero e proprio wallet SPV e al contrario hanno optato invece per wallet che fanno uso di un servizio centralizzato per ricevere le notifiche di pagamento. C’è certamente un livello di praticità che viene fornito con certo tipo di servizio, ma ci sono spesso conseguenze sottili, ad es. caricando un pubkey (public key) esteso al servizio, questo può conoscere tutti i tuoi indirizzi.

Con Decred, abbiamo optato per aggiungere il supporto SPV a dcrwallet integrando i filtri compatti: questo è un livello superiore di SPV che mantiene la privacy dell’utente riducendo al minimo la quantità di dati da scaricare prima che di poter utilizzare il wallet. L’idea dei filtri compatti proviene dalle discussioni nate sulla [mailing list dei bitcoin-dev](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2017-June/014474.html), inizialmente proposti da Alex Akselrod e Olaoluwa Osuntokun di Lightning Labs. A partire dalla fine di febbraio 2018, una copia completa della Decred chain utilizza 2,1 GB di spazio di archiviazione, rispetto ai 66 MB di spazio di archiviazione per gli header e i filtri compatti richiesti dal wallet SPV. Gli utenti interessati a seguire più da vicino gli sviluppi sull’SPV possono farlo a [questo link](https://github.com/decred/dcrwallet/issues/1000).

## Votazione Politeia
Il cuore del nostro sistema di proposte, [Politeia](https://github.com/decred/politeia/), è stato recentemente completato e stiamo aggiungendo il supporto per il voto. Politeia può essere descritta in breve come una cartella di registro su GitHub impressa nella Decred chain che utilizza l’attribuzione crittografica per creare un senso di responsabilità di tutti i partecipanti — utenti e amministratori allo stesso modo. Avere responsabilità superiori significa che le proposte, i commenti, i voti e le azioni amministrative in Politeia non risentiranno della censura che è diventata sempre più comune tra molte importanti società tech e i loro website.

Una volta completato il supporto al voto, Politeia verrà testato su testnet e quindi distribuito su mainnet. Successivamente, Politeia sarà utilizzata per discutere e finanziare nuove proposte, stabilire budget e effettuare pagamenti in corso con l’approvazione degli stakeholder. E’ importante far notare che le votazioni su Politeia saranno possibili solo per gli stakeholder i cui ticket sono ‘attivi’ nel ticket pool nel momento in cui viene richiesto un voto su una determinata proposta.

## Lightning Network
La maggior parte del lavoro di trasferimento di Lightning Labs’ lnd a Decred è terminata e il lavoro rimanente è momentaneamente in fase di completamento.

Decred è un fork di Bitcoin, ma manca di molti dei cambiamenti che sono stati raggruppati nel changeset “segregated witness” di Bitcoin e questo ha reso il trasferimento una vera sfida. Ci sono alcuni problemi in sospeso con le firme per le transazioni che devono essere ancora risolti; una volta risolto questi problemi, sarà possibile inizare il test su testnet.

## Release iniziale della privacy
A causa della concorrenza nel sotto-dominio della privacy, siamo stati prudenti nell’esporre i nostri piani per la privacy di Decred. Diversi mesi fa, i lavori di sviluppo sono iniziati in modo serio e costante e sono stati fatti progressi verso un prototipo che può essere pubblicato come parte della nostra versione iniziale della privacy. Questa versione iniziale comprenderà un codice di lavoro e una sintesi dei nostri piani per diversi ulteriori miglioramenti ad essa connessi.

## Controllo decentralizzato dei fondi
Il passaggio finale per la definitiva decentralizzazione della organizzazione decentralizzata sarà il controllo decentralizzato dei suoi fondi. Prima che il controllo formale sia decentralizzato, le erogazioni di fondi saranno soggette a un processo decisionale “soft” tramite Politeia. Piuttosto che adottare l’approccio utilizzato in Ethereum, che comprende centinaia o migliaia di righe di codice Solidity, creeremo uno smart contract che consenta agli stakeholder di Decred di votare sulle erogazioni di denaro sulla chain e rilasciare di conseguenza i fondi.

## Entità Autonome Decentrate
Il metodo per decentralizzare il controllo dei fondi della organizzazione decentralizzata sarà generalizzato per supportare entità create dagli utenti dette anche Entità Autonome Decentralizzate o Decentralized Autonomous Entities in inlgese (“DAE”). Poiché il principale punto distintivo di un’entità aziendale rispetto ad un individuo è la proprietà ed il controllo dei fondi e degli asset, utilizzeremo il controllo decentrato dei fondi come base per le DAE all’interno di Decred.

Ci concentreremo meno sulla componente speculativa della tokenizzazione e più sulla meccanica fondamentale per farlo funzionare, poiché la tokenizzazione crea diversi problemi di scalabilità, che hanno portato alla congestione chain di Ethereum. In breve, una DAE sarà composta da un semplice smart contract on-chain che delega il controllo dei fondi nel contratto a un gruppo di persone.

## Ottimizzazioni della scalabilità
Per fare in modo che Decred funzioni senza intoppi, è necessario eseguire costantemente una miriade di ottimizzazioni.

Poiché l’ottimizzazione del software spesso richiede molti dettagli, ecco un elenco delle principali ottimizzazioni pianificate:

* [nuovo algoritmo della firma](https://github.com/decred/dcrd/issues/950) — La modifica dell’algoritmo delle firme SigHashAllValue corregge il problema di scalabilità quadratica di Decred ereditato da Bitcoin, velocizzando incredibilmente il supporto di verifica delle firme.
* multi-peer sync support — Attualmente, dcrd può sincronizzare la sua chain solo da un singolo peer alla volta, il che porta a tempi di sincronizzazione iniziali lunghi, specialmente quando si connette a un peer lento, mentre la sincronizzazione da più peer contemporaneamente eviterebbe l’impasse.
* [header commitments](https://github.com/decred/dcrd/issues/971) — I block header di Decred possono essere modificati per supportare una varietà di impegni, ad esempio per i filtri compatti, gli output di transazione non spesi e l’inserimento dei ticket, che consente ai client SPV di operare in sicurezza, pulizia sicura della blockchain e tracciamento dello stato del ticket con un SPV client.
* Firme di schnorr — Le firme di più chiavi private possono essere aggregate in un’unica firma, garantendo considerevoli risparmi sulla rete e sull’archiviazione per i nodi Decred.

## Integrazioni con i file
Per molti utenti, le funzionalità che non sono disponibili con una bella interfaccia grafica non esistono.

Decrediton, il nostro wallet GUIcross-platform, integrerà il supporto per molti dei nostri sottoprogetti che sono in via di completamento: supporto SPV, piattaforme mobili, voto Politeia e Lightning Network.

I progressi su queste integrazioni possono procedere in parallelo e dovrebbero essere molto più di routine rispetto al lavoro richiesto per completare le componenti di backend.

## Exchange decentralizzato
Abbiamo rilasciato i tools [atomicswap](https://github.com/decred/atomicswap/) nel settembre 2017 come componente autonomo di un progetto più ampio, un Exchange decentralizzato. Molti progetti hanno fatto della decentralizzazione del processo di scambio sull exchange la loro e hanno una varietà di modelli di profitto diversi.

La nostra proposta per un Exchange decentralizzato sarà basata sui principi prima dei profitti ed sarà concepita come uno sforzo che speriamo coinvolgerà altri progetti crypto oltre a Decred. La proposta iniziale per questo sistema sarà il prossimo post di blog Decred e diventerà una proposta formale all’interno di Politeia una volta che sarà attiva su mainnet.

## Crescita del marketing
Un notevole lavoro è stato fatto sul fronte marketing negli ultimi 6 mesi. Decred ha stand e speaking sessions prenotate per molti dei maggiori eventi crypto e blockchain per i prossimi mesi e ha partecipato a diverse altre conferenze nei mesi scorsi. I test iniziali sono stati effettuati su annunci pubblicitari a pagamento tramite diversi servizi di marketing digitale, ad es. Facebook, Twitter e Google. Aumenteremo in modo sostanziale il digital marketing mentre stiamo continuando a stabilire metriche sull’efficacia dei vari approcci. Ad oggi, la nostra presenza è stata la più forte negli eventi degli Stati Uniti, e ci impegneremo ad ampliare la nostra presenza per includere altri paesi nel 2018.

## Conclusioni
Ci sono molti dei deliverables elencate in questa roadmap e faremo uno sforzo per raggiungerne il più possibile nel 2018. Personalmente, non vedo l’ora che Politeia voti andando in diretta su mainnet dato che metterà a disposizione dei fondi dell’organizzazione nelle mani degli stakeholder — circa 515.000 DCR, o 49,000,000 USD al tasso di cambio corrente.

Mentre non possiamo sapere con precisione cosa succederà quando questi fondi saranno diretti dai nostri stakeholder, siamo tutti qui per la convinzione che il processo decisionale decentralizzato -una forma di intelligenza collettiva- sia un modello di sovranità promettente. Costruire l’infrastruttura intorno a un nuovo modello di sovranità porta naturalmente a nuove applicazioni di tale sovranità, ad es. Politeia, DAEs e il concetto di stato digitale.

Siamo sempre alla ricerca di nuovi collaboratori, quindi se questo progetto ti affascina o hai in mente qualcosa che potrebbe essere migliorato, ti incoraggiamo a metterti in contatto, lavorare con noi, creare nuovi contenuti ed essere pagati in decred, ovviamente.

Ci puoi trovare sul nostro [Rocket.Chat](https://rocketchat.decred.org/home), [Matrix](https://riot.im/app/#/room/), [Discord](https://discordapp.com/invite/GJ2GXfz), [Slack](https://decred.slack.com/messages/DB0MNLGTD/team/UB1Q74U7R/), [IRC](https://webchat.freenode.net/?channels=decred&uio=d4), [Telegram](https://t.me/decred), [Reddit](https://www.reddit.com/r/decred/) o su [Forum](https://forum.decred.org/). Nota bene: gli inviti Slack devono essere richiesti manualmente tramite una delle altre reti di chat prima che possa essere concesso l’accesso.

***** [Articolo Originale](https://blog.decred.org/2018/02/28/2018-Decred-Roadmap/) pubblicato da Jake Yocom-Piatt [@behindtext](https://twitter.com/behindtext)
[www.decred.org](https://www.decred.org) | [Decred](https://medium.com/@decred) | [@decredproject](https://twitter.com/decredproject)
