# Ex4.qubit
Il seguente codice  Python mostra come utilizzare la libreria qiskit  per creare uno stato di Bell, un esempio fondamentale di entanglement quantistico tra due qubit. 
Preliminarmente si installano le librerie necessarie, con i comandi seguenti:
pip install qiskit-aer
pip install qiskit
Uno stato di Bell è uno dei quattro stati entangled: qui creiamo lo stato 1/√2(|00⟩+|11⟩). 
Per farlo definiamo un circuito quantistico con due qubit posti inizialmente a zero e due bit classici che servono per memorizzare l’esito della misura dei due qbit.
Applichiamo la porta di Hadamard (H) al primo qubit per posizionarlo nello stato di sovrapposizione 1/√2(|0⟩+|1⟩). 
Usiamo il primo qubit come variabile di controllo di una porta CNOT (X) che esegue il flip della variabile di ingresso se la variabile di controllo ha valore 1, altrimenti, ripropone in uscita il valore dell’ingresso.
Con questo procedimento, i due qubit risultano essere in entanglement, come è possibile verificare direttamente osservando quanto riportato in Figura 47.
 

I due qubit sono inizializzati allo stato |0⟩. 
Nel punto “h”, il qbit 0 è nello stato di sovrapposizione 1/√2(|0⟩+|1⟩ in quanto ha attraversato la porta quantistica H; nel punto “x”, il qubit 1 è |0⟩ se il qubit 0 è |0⟩ (in quanto in questo stato la porta NOT ripropone in output il suo input), mentre è |1⟩  se il qubit 0 è |1⟩ ⟩ (in quanto in questo stato la porta NOT inverte in output il suo input).
In questo modo i due qubit risultano entangled nello stato di Bell desiderato: 1/√2(|00⟩+|11⟩). 
Poi eseguiamo la misura di entrambi i qubit su un certo numero di prove e scopriamo che la probabilità della combinazione “00” è la medesima di quella “11” come atteso.


Il codice Python seguente mostra come utilizzare la libreria qiskit  per creare uno stato di Bell, un esempio fondamentale di entanglement quantistico tra due qubit. 
Preliminarmente con i comandi seguenti si installano le librerie necessarie:
pip install qiskit-aer
pip install qiskit
Uno stato di Bell, come abbiamo visto in Qubit, può essere uno dei quattro stati massimamente entangled: qui creeremo lo stato 1/√2(|00⟩+|11⟩). Per farlo basterà creare un circuito quantistico con due qubit e due bit classici; applicando la porta di Hadamard (H) al primo qubit, questo è messo in uno stato di sovrapposizione 1/√2(|0⟩+|1⟩). Poi applichiamo una porta CNOT con il qubit 0 come controllo e il qubit 1 come target: se il qubit 0 è |0>, il qubit 1 rimane |0>, mentre se il qubit 0 è |1>, il qubit 1 diventa |1>; in questo modo i due qubit risultano entangled. 
Il sistema composto dalle due porte crea, quindi lo stato di Bell richiesto. Poi eseguiamo la misura di entrambi i qubit, mappiamo i risultati sui bit classici e ci aspettiamo di vedere solo i risultati '00' e '11', ciascuno con circa il 50% di probabilità, ed è esattamente quel che succede nella simulazione.
