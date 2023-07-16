# ESP32_RTOS_21_Esempio_Deadlock_tempo_limite

## FreeRTOS Esercizio 21: concorrenza tra due task e deadlock - tempo limite.

Due task devono accedere in modo concorrente alla stessa risorsa; per guadagnare l'accesso, i task devono acquisire due mutex (mutex_1 e mutex_2).

Il Task A ha priorità alta; il Task B ha priorità bassa.

La soluzione qui proposta impone un limite di tempo per attendere l'acquisizione del mutex.

Se scade il tempo massimo di attesa, si gestisce l'eccezione rilasciando l'eventuale mutex già acquisito e si ricomincia il task. 
