# Apuntes-Xavi-Sancho

Sistemes de fitxers

FAT (File Allocation Table):
Compatible amb gairebé tots els sistemes operatius.
Utilitzat per a l'intercanvi de dades en entorns multiarranc.
Comú en targetes de memòria i dispositius similars.
Limitacions: tamany màxim de fitxers i discos, i fragmentació que alenteix les operacions.
FAT32:
Sistema creat per superar les limitacions de FAT, mantenint la compatibilitat amb MS-DOS.
Encara insuficient per a aplicacions com captura i edició de vídeo.
NTFS (New Technology File System):
Sistema d'arxius dissenyat per Windows NT, amb més seguretat i eficiència.
Adequat per particions grans en estacions de treball i servidors.
La conversió de FAT32 a NTFS no és reversible.
ExFAT (Extensible File Allocation Table):
Sistema que permet fitxers grans i augmenta la velocitat d'escriptura i lectura.
Ideal per a dispositius externs com discos durs portàtils i pendrives.



Sistemes de fitxers a Linux

EXT 2 (Second Extended File System):
Sistema d'arxius avançat amb suport per a la correcció i detecció d'errors.
Ofereix compressió d'arxius i major tolerància a la fragmentació.
Millora en temps de resposta, encara que requereix més memòria.
Comú en sistemes operatius Linux (Red Hat, Fedora, Debian) i Unix.
EXT 3 i EXT 4:
Sistemes de fitxers amb registre diari (journaling) que milloren la recuperació en cas de fallades.
Protocol·litzen processos d'escriptura per restablir ràpidament el sistema.
Eficients per gestionar grans quantitats d'arxius petits.
Utilitzats en sistemes operatius Linux i Unix.
Altres:.
Existeixen altres sistemes de fitxers per a Linux com ReiserFS, XFS, JFS, però són menys comuns.

Journaling file system:

Journaling és una tècnica utilitzada en alguns sistemes de fitxers per millorar la seguretat i fiabilitat de les dades. Consisteix en registrar en un diari o "journal" les operacions que es faran abans d'escriure-les efectivament al disc. Això permet recuperar el sistema ràpidament en cas d'una fallada, ja que es poden revisar les operacions incompletes o pendents i corregir-les.

Aquesta tècnica redueix el risc de corrupció de dades després d'un tall d'energia o una caiguda del sistema, assegurant que el sistema de fitxers es mantingui en un estat consistent.








Taules de partició

Models de taules de partició:
Actualment, els dos models generals són MBR i GPT.
MBR (Master Boot Record):
Utilitzat per identificar el bloc d'arrencada i iniciar el sistema operatiu en ordinadors amb BIOS.
Té limitacions, com la incapacitat de gestionar particions de més de 2TB i un màxim de 4 particions primàries.
GPT (GUID Partition Table):
Sistema de taula de particions que substitueix MBR i requereix UEFI per arrencar el sistema operatiu.
Permet direccions de disc de 64 bits, amb una mida màxima de disc de 9,4 ZB (Zettabytes).
Admet fins a 128 particions per disc, amb una mida màxima de 18 Exabytes cadascuna.

Particions (MBR)

Particions (MBR):
Un disc dur es pot dividir en compartiments anomenats particions, cadascuna amb un sistema de fitxers (NTFS, FAT32, etc.).
Tipus de particions:
Primària:
Fins a 4 particions primàries per disc, o 3 primàries i 1 estesa.
Generalment, on s'instal·la el sistema operatiu.
Estesa:
Permet superar la limitació de 4 particions primàries.
Només pot haver una partició estesa per disc i conté particions lògiques.
Lògica:
Es creen dins d'una partició estesa.
S'utilitzen per emmagatzemar informació o aplicacions, no el sistema operatiu.
A Windows, hi ha un límit de 23 particions lògiques; a Linux, el límit total és de 15 particions de tots els tipus.
Volums
Volums:
Indiquen al sistema operatiu les unitats d'emmagatzematge disponibles, incloent el seu nom, lletra d'accés i tipus de sistema de fitxers.
Composició d'un volum:
Pot estar format per una part d'un disc dur, diverses parts del mateix disc o parts de diferents discos durs.
Això permet que un volum pugui ser més gran que qualsevol dels discos que el formen.
Tipus de volums:
El tipus més habitual en un disc dur d'usuari és el Volum simple, que és una part del disc que opera com una unitat física independent.

Còpies de seguretat

Una de les coses més importants d'un sistema operatiu és tenir fiabilitat en la informació del sistema, per això és molt important que la informació estigui resguardada, una de les maneres d'aconseguir-ho és fent còpies de seguretat (també anomenades backups).

Tipus de còpies de seguretat

Còpia completa:
Desa tota la informació del servidor.
Consumeix molt de temps i espai d'emmagatzematge, poc viable per a moltes empreses.
Còpia incremental:
Guarda només les dades que han canviat des de la darrera còpia.
La recuperació és lenta i pot ser inexacta si falla alguna còpia.
Còpia diferencial:
Desa les dades canviades des de la darrera còpia completa.
Ocupa més espai que l'incremental, però és més ràpida de recuperar.

