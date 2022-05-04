## Bitgold, Nick Szabo, 29 Dicembre 2005

Un po’ di tempo fa mi sono imbattuto nel concetto di “Bit Gold”. Il
problema, riassunto in poche parole, è che al giorno d’oggi il valore
della nostra moneta dipende strettamente dalla fiducia che riponiamo in
terzi. Come già hanno dimostrato nel corso del 20esimo secolo episodi di
inflazione e di iperinflazione, questa situazione non rappresenta una
condizione ideale. Analizzando il caso di una “private bank note”
(letteralmente una moneta privata), osserviamo come essa possieda
vantaggi e svantaggi ma rimanga comunque fondata su un sentimento di
fiducia verso una terza parte.

Nel passato si ovviava a questo problema attraverso i metalli preziosi o
altri oggetti rari; tuttavia, questi sono scarsi in natura e costosi da
ottenere; oltre a questo è troppo dispendioso sia in termini di denaro
che in termini di tempo verificare l’autenticità dei metalli per ogni
singola transazione. Proprio a causa di questo un terzo, (solitamente
associato con l’esattore che accettava moneta come pagamento) era
indotto a “stampare” moneta con una percentuale di metallo prezioso ben
specifica. Infatti, trasportare grandi carichi di metalli può essere un
affare relativamente insicuro, come hanno già realizzato gli Inglesi in
passato quando tentarono di trasportare dell’oro attraverso l’atlantico
con destinazione il Canada durante la Prima guerra mondiale per
supportare il valore della sterlina. Ad aggravare questa situazione c’è
il fatto che i metalli rari non possono essere utilizzati per i
pagamenti online.

Sarebbe molto vantaggioso se ci fosse un protocollo in grado di creare
dei “Bits” ad un costo pressoché irrilevante con una minima dipendenza
da terzi e vi fosse la possibilità di trasportarli e conservarli con un
minimo livello di fiducia. Bit Gold.

La mia proposta per Bitgold si basa sul calcolo di una stringa di bits a
partire da una stringa di “challenge bits”, usando delle funzioni, tra
cui: funzione puzzle client, funzione proof of work o la funzione secure
benchmark. La stringa di bit risultante è la proof of work. Si
tratterebbe di una funzione unidirezionale, che necessita di un numero
di calcoli proibitivi per risalire alla funzione d’origine.

Di seguito descrivo i passaggi principali per il sistema “Bit Gold” che
ho concepito:

1.  Una stringa di bits, detta “challenge string”, viene creata (vedi
    step 5);

2.  Alice con il suo computer genera la stringa della proof of work a
    partire dai bits della “challenge string” usando una funzione
    benchmark;

3.  La proof of work possiede una data e ora ben definite. Questo metodo
    permette di lavorare anche con servizi di timestamp diversi senza la
    necessità che essi siano basati su fondamenta definite
    precedentemente;

4.  Alice procede quindi aggiungendo la stringa di verifica e la stringa
    proof of work ad un registro decentralizzato per Bit-Gold
    (<https://nakamotoinstitute.org/secure-property-titles/>). Anche in
    questo caso non si fa affidamento ad un singolo server per il
    corretto funzionamento del registro;

5.  L’ultima stringa di Bitgold creata è anche la stringa di verifica
    per la prossima stringa da creare;

6.  Per verificare che Alice sia la proprietaria di una specifica
    stringa di Bitgold, Bob controlla il registro, non falsificabile,
    del Bitgold per verificare che sia la legittima proprietaria;

7.  Per stimare il valore di una stringa di Bitgold Bob può controllare
    e verificare i “challenge bits”, la stringa della proof of work e il
    timestamp.

Osserviamo come il controllo di Alice sui propri Bitgold non dipende
unicamente dalla possessione dei bits ma principalmente dalla sua
posizione “più in alto” nella catena di titoli (catena di firme
digitale) all’interno del registro.

Tutto questo può essere automatizzato da un software. I limiti
principali alla sicurezza di questo sistema sono dovuti a come viene
distribuita la fiducia ai punti (3) e (4), e il problema della “computer
architecture”, ossia, detto brevemente, da come è strutturato il pc, che
verrà però discussa qua sotto.

Hal Finney ha implementato una variante del Bitgold chiamata RPOW
(Reusable Proof of Work). Questa si basa sulla pubblicazione del codice
del computer per la “mint”, che viene eseguita su un pc remoto a prova
di manomissione. L’acquirente del Bitgold può successivamente utilizzare
l’attestazione remota, che Finney definisce “transparent server
technique”, per verificare che un determinato numero di cicli sia stato
effettivamente eseguito.

Il problema principale con tutti questi processi è che la verifica della
proof of work dipende fortemente dalla “computer architecture”, e non su
della matematica posta a priori e su cicli di calcolo astratti. Quindi è
possibile diventare un produttore (miner) anche ad un costo molto
contenuto (di diversi ordini di grandezza) ed essere quindi in grado di
“produrre” moltissimo Bitgold. Tuttavia, poiché il Bitgold possiede un
timestamp, è possibile verificare il tempo richiesto per la creazione e
la difficoltà matematica relativa al processo. A partire da questo si
può quasi sempre dedurre il costo di produzione in quel periodo di
tempo.

A differenza degli atomi d’oro solidi, per gli oggetti da collezione una
grande produzione durante un determinato periodo di tempo farà scendere
il valore di questi oggetti. In questo senso “Bitgold” si comporta
maggiormente come degli oggetti da collezione che come l’oro solido.
Tuttavia, l’incontro tra questo mercato e l’asta di vendita, che
determina il valore iniziale, potrebbe comportare profitti molto
consistenti per i “Bitgold miners” che inventano e sviluppano “computer
architecture” ottimizzate per questi processi.

Pertanto, il Bitgold non sarà fungibile grazie ad una semplice funzione
o alla lunghezza di una stringa. Invece, per creare unità fungibili i
rivenditori devono mettere assieme dei pezzi, anche di valore diverso,
di Bitgold e formare unità più grandi di valore simile. Questo è simile
a quello che fanno molti rivenditori di commodities per rendere questi
mercati possibili. La fiducia è ancora distribuita poiché il valore
stimato di tali pacchetti può essere verificato in modo indipendente da
terze parti in modo del tutto automatizzato.

Riassumendo, tutte le valute che l’umanità ha utilizzato erano, e sono,
insicure in un modo o nell’altro. Questa insicurezza si è manifestata in
molteplici espressioni, dalla contraffazione al furto, ma la più nociva
di tutte è sicuramente l’inflazione. Il Bitgold potrebbe fornirci una
sicurezza senza precedenti da questi pericoli. La possibilità di un
eccesso di supply dovuta ad innovazioni in termini di hardware potrebbe
essere un difetto del Bitgold, o, perlomeno, un’imperfezione che le aste
iniziali e le rivendite ex-post di Bitgold dovranno affrontare.
