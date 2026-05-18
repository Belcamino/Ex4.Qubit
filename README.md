# Dal libro Arithmós 
*Tempo · Relatività · Quanti · Intelligenze
Dai pitagorici alla coscienza artificiale*

- [MondadoriStore](https://www.mondadoristore.it/arithmos-tempo-relativita-quanti-intelligenze-dai-pitagorici-alla-coscienza-artificiale-libro-luigi-belcamino/p/9791224076780 "MondadoriStore")
- [Amazon](https://amzn.eu/d/0gmjyQnW "Amazon")
- [Youcanprint Store](https://store.youcanprint.it/arithmos-tempo-relativita-quanti-intelligenze-dai-pitagorici-alla-coscienza-artificiale/b/d4089bb3-c7ba-5343-921f-9c353ddee1ff "Youcanprint Store")
 

## Esercitazione Ex4.qubit
Il seguente codice  *Python* mostra come utilizzare la libreria *qiskit*  per creare uno stato di Bell, un esempio fondamentale di entanglement quantistico tra due qubit. 
Preliminarmente si installano le librerie necessarie, con i comandi seguenti:
``
pip install qiskit-aer
``
``
pip install qiskit
``

Uno stato di Bell è uno dei quattro stati entangled: qui creiamo lo stato``1/√2(|00⟩+|11⟩)``.
Per farlo, definiamo un circuito quantistico con due qubit posti inizialmente a zero e due bit classici che servono per memorizzare l'esito della misura dei due qbit.
Applichiamo la porta di Hadamard (H) al primo qubit per posizionarlo nello stato di sovrapposizione``1/√2(|0⟩+|1⟩)``.

Usiamo il primo qubit come variabile di controllo di una porta CNOT (X) che esegue il flip della variabile di ingresso, se la variabile di controllo ha valore 1, altrimenti, ripropone in uscita il valore dell’ingresso.
Con questo procedimento, i due qubit risultano essere in entanglement, come è possibile verificare direttamente osservando quanto riportato in Figura 47:![](https://raw.githubusercontent.com/Belcamino/Ex4.Qubit/refs/heads/master/Figura47.png "Figura 47.")
I due qubit sono inizializzati allo stato``|0⟩``. 
Nel punto "h”, il qbit 0 è nello stato di sovrapposizione ``1/√2(|0⟩+|1⟩``, in quanto ha attraversato la porta quantistica H; 
nel punto “x”, il qubit 1 è ``|0⟩``, se il qubit 0 è ``|0⟩`` (in quanto in questo stato la porta NOT ripropone in output il suo input), mentre è ``|1⟩`` se il qubit 0 è ``|1⟩ ⟩`` (in quanto in questo stato la porta NOT inverte in output il suo input).

In questo modo i due qubit risultano entangled nello stato di Bell desiderato ``1/√2(|00⟩+|11⟩)``.

Poi eseguiamo la misura di entrambi i qubit su un certo numero di prove e scopriamo che la probabilità della combinazione “00” è la medesima di quella “11” come atteso.
