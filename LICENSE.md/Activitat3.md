1. Indica quins són els motors d’emmagatzematge que pots utilitzar (quins estan actius)? Mostra al comanda utilitzada i el resultat d’aquesta.



Si SUPPORT està en YES vol dir que està actiu i es compatible.

2. Com puc saber quin és el motor d’emmagatzematge per defecte. Mostra com canviar aquest paràmetre de tal manera que les noves taules que creem a la BD per defecte utilitzin el motor MyISAM?


3. Com podem saber quin és el motor d'emmagatzematge per defecte?


4. Explica els passos per instal·lar i activar l'ENGINE MyRocks. MyRocks és un motor d'emmagatzematge per MySQL basat en RocksDB (SGBD incrustat de tipus clau-valor).


Checkpoint: Mostra al professor que està instal·lat i posa un exemple de com funciona.


5. Importa la BD Sakila com a taules MyISAM. Fes els canvis necessaris per importar la BD Sakila perquè totes les taules siguin de tipus MyISAM. 
Mira quins són els fitxers físics que ha creat, quan ocupen i quines són les seves extensions. Mostra'n una captura de pantalla i indica què conté cada fitxer.



Activitat 2. INNODB part I. REALITZA ELS SEGÜENTS APARTATS. (2 punts)


1. Importa la BD Sakila com a taules InnoDB. 


2. Quin/quins són els fitxers de dades? A on es troben i quin és la seva mida?


3. Canvia la configuració del MySQL perqurè:
Canviar la localització dels fitxers del tablespace de sistema per defecte a /discs-mysql/
Tinguem dos fitxers corresponents al tablespace de sistema.
Tots dos han de tenir la mateixa mida inicial (1MB) 
El tablespace ha de creixer de 1MB en 1MB.
Situa aquests fitxers (de manera relativa a la localització per defecte) en una nova localització simulant el següent:
/discs-mysql/disk1/primer fitxer de dades → simularà un disc dur
/discs-mysql/disk2/segon fitxer de dades → simularà un segon disc dur.


4. Checkpoint: Mostra al professor els canvis realitzats i que la BD continua funcionant.


Activitat 3. INNODB part II. REALITZA ELS SEGÜENTS APARTATS. (1 punt)

1. Partint de l'esquema anterior configura el Percona Server perquè cada taula generi el seu propi tablespace en una carpeta anomenada tspaces (aquesta pot estar situada a on vulgueu). 


1. Indica quins són els canvis de configuració que has realitzat.


2. Després del canvi què ha passat amb els fitxers que contenien les dades de la BD de Sakila? Fes les captures necesàries per complementar la resposta.



Activitat 4. INNODB part III. REALITZA ELS SEGÜENTS APARTATS. (1 punts)

1. Crea un tablespace anomenat 'ts1' situat a /discs-mysql/disc1/ i col·loca les taules actor, address i category de la BD Sakila.



2. Crea un altre tablespace anomenat 'ts2' situat a /discs-mysql/disc2/ i col·loca-hi la resta de taules.


3. Comprova que pots realitzar operacions DML a les taules dels dos tablespaces.


4. Quines comandes i configuracions has realitzat per fer els dos apartats anteriors?


5. Checkpoint: Mostra al professor els canvis realitzats i que la BD continua funcionant



Activitat 5. REDOLOG. REALITZA ELS SEGÜENTS APARTATS. (2 punt)

1. Com podem comprovar (Innodb Log Checkpointing):
LSN (Log Sequence Number)
L'últim LSN actualitzat a disc
Quin és l'últim LSN que se li ha fet Checkpoint


2. Proposa un exemple a on es vegi l'ús del redolog


3. Com podem mirar el número de pàgines modificades (dirty pages)? I el número total de pàgines?


4. Checkpoint: Mostra al professor els canvis realitzats i que la BD continua funcionant.


Activitat 6. Implentar BD Distribuïdes. (2 punt)

Com s'ha vist a classe MySQL proporciona el motor d'emmagatzemament FEDERATED que té com a funció permetre l'accés remot a bases de dades MySQL en un servidor local sense utilitzar tècniques de replicació ni clustering.


1. Prepara un Servidor Percona Server amb la BD de Sakila



2. Prepara un segon servidor Percona Server a on hi hauran un conjunt de taules FEDERADES al primer servdor.


3. Per realitzar aquest link entre les dues BD podem fer-ho de dues maneres:


1. Opció1: especificar TOTA la cadena de connexió a CONNECTION 


2. Opció2: especifficar una connexió a un server a CONNECTION que prèviament s'ha creat mitjançant CREATE SERVER


3. Posa un exemple de 2 taules de cada opció. 


Tingues en compte els permisos a nivell de BD i de SO així com temes de seguretat com firewalls, etc...

4. Detalla quines són els passos i comandes que has hagut de realitzar en cada màquina.


4. Checkpoint: Mostra al professor la configuració que has hagut de realitzar i el seu funcionament.



Activitat 7. Storage Engine CSV (1 punt)


1. Documenta i posa exemple de com utilitzar ENGINE CSV.

2. Cal documentar els passos que has hagut de realitzar per preparar l'exemple: configuracions, instruccions DML, DDL, etc....


3. Checkpoint: Mostra al professor la configuració que has hagut de realitzar i el seu funcionament.

