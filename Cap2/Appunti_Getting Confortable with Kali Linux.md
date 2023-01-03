
# Note su Kali

 - Distro Debian based
 - Sviluppata per Penetration Testing e Security Audit
 - Libro di approfondimento suggerito: "Kali Linux Revealed"

# Avvio / Installazione

 - Sul sito kali.org sono disponibili le immagini
 - E' possibile utilizzare Kali su un host dedicato o come VMs
    - E' possibile utilizzare anche il sottosistema WLS di Microsoft Windows per avere una macchina Kali ben integrata nel sistema

 - Esercizio 2.6.3
    - Eseguire il boot di Kali e modificare la password dell'utente kali (che di default è kali)
        - Avviare il sistema ed accedere con utente kali / kali
        - Avviare una shell
        - Utilizzare in comando "passwd", verrà chiedo di inserire la nuova password con relativa conferma

 - Comandi base linux...
    - ls       listing della directory corrente
    - cd       spostamento in una directory
    - pwd      visualizzazione del path corrente
    - mkdir    crea una directory
    - which    visualizza la posizione di un file in un path di sistema
    - locate   cerca file e directory nel filesystem sulla base di locate.db
    - find     cerca file e directory nel filesystem sulla base di una espressione
 
 - Esercizi 2.4.3.4
    - Use man to look at the man page for one of your preferred commands
      - man pwd

    - Use man to look for a keyword related to file compression
      - man zip

    - Use which to locate the pwd command on your Kali virtual machine
      - which pwd

    - Use locate to locate wce32.exe on your Kali virtual machine
      - sudo updatedb && locate wce32.exe

    - Use find to identify any file (not directory) modified in the last day, NOT owned by the root user and execute ls -l on them. Chaining/piping commands is NOT allowed!
      - sudo find {dir} -mtime -1 -exec ls -l {} \; | grep -v root ---> da fare senza grep
      - sudo find {dir} -mtime -1 -type f -not -user root -exec ls -l {} \; ---> secondo tentativo nuscito meglio ;)

    - Risorse:
      https://linux.die.net/man/1/find

 - Gestione dei servizi
    - 