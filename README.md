# Inferno 1.1 - Penetration Testing


<img src="images/inferno-dante.png" alt="Inferno" width="1000" />


## Descrizione

Questo progetto documenta un'attività completa di penetration testing condotta sull’asset *Inferno 1.1*, una macchina virtuale vulnerabile by-design, disponibile su [VulnHub](https://www.vulnhub.com/entry/inferno-11,603/). L’obiettivo è stato riprodurre fedelmente un approccio di ethical hacking, descrivendo in dettaglio ogni fase dell’analisi e dell’attacco.

---

## Contenuti del progetto

- **Documento di replicabilità**: descrizione dettagliata di tutte le fasi del penetration test, con i comandi eseguiti, gli strumenti utilizzati e i risultati ottenuti.
- **Penetration Testing Report**: report strutturato secondo le best practice, contenente executive summary, regole di ingaggio, vulnerability report, remediation report, findings summary e detailed summary.
- **Report e output** delle scansioni con strumenti automatici (Nessus, OpenVAS, Nikto, ZAP, ecc.).
- **Script** utilizzato per la fase di exploitation.

---

## Ambiente di lavoro

- Virtualizzazione: Oracle VM VirtualBox 7.1.6 con rete NAT personalizzata (`10.0.2.0/24`).
- Macchina attaccante: Kali Linux 2025.2.
- Target: macchina virtuale Inferno 1.1 

---

## Strumenti principali utilizzati

- **Nmap**, **arp-scan** e **unicornscan** per discovery e port scanning.
- **Nessus** e **OpenVAS** per vulnerability scanning automatizzato.
- **Nikto**, **OWASP ZAP**, **WhatWeb**, **DIRB**, **DirBuster**, **GoBuster**, **Dirsearch**, **WafW00f** per analisi della web application.
- **Metasploit** e **Armitage** per tentativi automatici di exploitation.
- **Hydra** per attacco brute-force su autenticazione HTTP Basic.
- Exploit manuale per la vulnerabilità **CVE-2018-14009** su Codiad.

---

## Fasi del penetration testing

1. **Target Scoping** 
   Definizione del perimetro dell’analisi e degli obiettivi del test.
   
2. **Information Gathering**  
   Raccolta dati preliminare tramite OSINT.

3. **Target Discovery**  
   Identificazione degli host attivi nella rete.

4. **Port Scanning e Service Enumeration**  
   Identificazione porte TCP/UDP aperte e servizi attivi, con riconoscimento versioni.

5. **Vulnerability Mapping**  
   Individuazione di vulnerabilità note tramite scanner automatici e analisi manuale.

6. **Exploitation**  
   Tentativi di compromissione automatici falliti, seguiti da exploitation manuale tramite brute-force su autenticazione HTTP e sfruttamento di vulnerabilità note.

7. **Post-Exploitation**  
   Escalation privilegi, esplorazione filesystem, recupero credenziali, accesso SSH, e stabilizzazione dell’accesso tramite backdoor persistente.

---

## Come replicare

- Clonare questo repository.
- Configurare ambiente VirtualBox con rete NAT personalizzata.
- Avviare Kali Linux e Inferno 1.1 nella rete configurata.
- Seguire la documentazione dettagliata nel file *Documento di replicabilità* per eseguire le scansioni, l’enumerazione, l’exploit e le attività post-compromissione.
- Consultare i report automatici disponibili nella cartella `Report` per i risultati dettagliati.

---

## Licenza

Questo progetto è sviluppato a scopo didattico nell’ambito del corso di Penetration Testing e Ethical Hacking (PTEH) A.A. 2024/2025, Università degli Studi di Salerno.
