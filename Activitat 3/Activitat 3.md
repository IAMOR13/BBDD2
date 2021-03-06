1. Indica quins són els motors d’emmagatzematge que pots utilitzar (quins estan actius)? Mostra al comanda utilitzada i el resultat d’aquesta.

 <img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex1.PNG"/>
 
 <img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/2Ex1.PNG"/>
 
 <img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/3Ex1.PNG"/>
 
 Comanda: SHOW ENGINES\G

Si SUPPORT està en YES vol dir que està actiu i es compatible.

2. Com puc saber quin és el motor d’emmagatzematge per defecte. Mostra com canviar aquest paràmetre de tal manera que les noves taules que creem a la BD per defecte utilitzin el motor MyISAM?

El motor d'emmagatzematge per defecte es en el que SUPPORT esta en DEFAULT

 <img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex1.PNG"/>
 
 Per cambiar el motor d'emmagatzemarge per defecte utilitzar: SET default_storage_engine=MRG_MYISAM;
 
 <img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/4Ex1.PNG"/>

3. Com podem saber quin és el motor d'emmagatzematge per defecte?

El motor d'emmagatzematge per defecte es el que en SHOW ENGINES\G posa DEFAULT

4. Explica els passos per instal·lar i activar l'ENGINE MyRocks. MyRocks és un motor d'emmagatzematge per MySQL basat en RocksDB (SGBD incrustat de tipus clau-valor).

Activar en el arxiu:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/5Ex1.PNG"/>

[percona-testing-$basearch]
[percona-testing-noarch]
[percona-experimental-$basearch]
[percona-experimental-noarch]

en 1 per activar els repositoris experimentals

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/6Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/7Ex1.PNG"/>

Comanda per instalar MyRocks

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/8Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/9Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/10Ex1.PNG"/>

Activar els permisos per el engine

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/11Ex1.PNG"/>

Engines activats

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/12Ex1.PNG"/>

Checkpoint: Mostra al professor que està instal·lat i posa un exemple de com funciona.


5. Importa la BD Sakila com a taules MyISAM. Fes els canvis necessaris per importar la BD Sakila perquè totes les taules siguin de tipus MyISAM. 
Mira quins són els fitxers físics que ha creat, quan ocupen i quines són les seves extensions. Mostra'n una captura de pantalla i indica què conté cada fitxer.

Canviar la configuració de mysql per posar el Engine amb MyIsam com engine per defecte:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/13Ex1.PNG"/>

Canviar del arxiu sql tots els Engine i o borrar-lo o cambiar-lo per MyISAM:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/14Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/15Ex1.PNG"/>

Carregar la BD a Mysql

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/16Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/17Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/18Ex1.PNG"/>

Per llistar els fitxers fisics de la BD es troben a var/lib/mysql/nomdelabasededades

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/19Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/20Ex1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/21Ex1.PNG"/>

frm: Guarda la definició de l'estructura de la taula

MYD: Guarda el contingut de la taula

MYI: Guarda els index de la taula

opt: Guarda els jocs de caràcters de la base de dades

TRN: Guarda els tipus de trigger

TRG: Guarda els triggers


Activitat 2. INNODB part I. REALITZA ELS SEGÜENTS APARTATS. (2 punts)


1. Importa la BD Sakila com a taules InnoDB.

Esorrar l'anterior base de dades:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex2.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/2Ex2.PNG"/>

Canviar la configuració de mysql per posar el Engine amb InnoDB com engine per defecte:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/3Ex2.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/4Ex2.PNG"/>

Carregar la base de dades sakila

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/5Ex2.PNG"/>

Les taules estan en InnoDB:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/6Ex2.PNG"/>



2. Quin/quins són els fitxers de dades? A on es troben i quin és la seva mida?

Els fitxers de dades es troben a var/lib/mysql/nomdelabasededades

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/7Ex2.PNG"/>


3. Canvia la configuració del MySQL perqurè:


Canviar la localització dels fitxers del tablespace de sistema per defecte a /discs-mysql/

Tinguem dos fitxers corresponents al tablespace de sistema.

Tots dos han de tenir la mateixa mida inicial (1MB) 

El tablespace ha de creixer de 1MB en 1MB.


Primer tenim que desactivar la tablespace del sistema per defecte en el fitxer de configuració my.cnf amb:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/8Ex2.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/9Ex2.PNG"/>


Situa aquests fitxers (de manera relativa a la localització per defecte) en una nova localització simulant el següent:

/discs-mysql/disk1/primer fitxer de dades → simularà un disc dur

/discs-mysql/disk2/segon fitxer de dades → simularà un segon disc dur.


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/10Ex2.PNG"/>


PREGUNTAR EN MY.CNF NO TENGO SECCION ([mysqld] innodb_file_per_table=1)
4. Checkpoint: Mostra al professor els canvis realitzats i que la BD continua funcionant.


Activitat 3. INNODB part II. REALITZA ELS SEGÜENTS APARTATS. (1 punt)

1. Partint de l'esquema anterior configura el Percona Server perquè cada taula generi el seu propi tablespace en una carpeta anomenada tspaces (aquesta pot estar situada a on vulgueu).

Primer cal activar l'opció de innodb_file_per_table amb:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex3.PNG"/>

Ara ja està activat:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/2Ex3.PNG"/>

Y ara afegim una nova taula amb Data Directory per indicar-li que on volem que es generi el tablespace

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/3Ex3.PNG"/>

1. Indica quins són els canvis de configuració que has realitzat.

Com per que es generi un tablespace fa falta indicar-lo amb DATA DIRECTORY = "/tspaces"; , tendriem que cambiar totes les taules de la base de dades sakila per indicar-li el nou Data Directory.

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/4Ex3.PNG"/>



2. Després del canvi què ha passat amb els fitxers que contenien les dades de la BD de Sakila? Fes les captures necesàries per complementar la resposta.

Al afegir el tablespace a la taula, es crearia un arxiu idb per cada taula en el directori indicat, en aquest cas, /tspaces.

Mysql també crea arxius isl que contenen el nom de la ruta per a cada taula.

PREGUNTAR HE VUELTO A CARGAR LA BD sakila Y LOS ARCHIVOS FISICOS TABLA ACTOR QUE CAMBIE CON DATA DIRECTORY = "/tspaces" NO ESTA EN var/lib/mysql/sakila NI EN tspaces!!

Activitat 4. INNODB part III. REALITZA ELS SEGÜENTS APARTATS. (1 punts)

1. Crea un tablespace anomenat 'ts1' situat a /discs-mysql/disc1/ i col·loca les taules actor, address i category de la BD Sakila.



2. Crea un altre tablespace anomenat 'ts2' situat a /discs-mysql/disc2/ i col·loca-hi la resta de taules.


3. Comprova que pots realitzar operacions DML a les taules dels dos tablespaces.


4. Quines comandes i configuracions has realitzat per fer els dos apartats anteriors?


5. Checkpoint: Mostra al professor els canvis realitzats i que la BD continua funcionant



Activitat 5. REDOLOG. REALITZA ELS SEGÜENTS APARTATS. (2 punt)

1. Com podem comprovar (Innodb Log Checkpointing):
LSN (Log Sequence Number)

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/2Ex5.PNG"/>

L'últim LSN actualitzat a disc

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/3Ex5.PNG"/>


Quin és l'últim LSN que se li ha fet Checkpoint

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/4Ex5.PNG"/>

Per veure els LSN utilitzar la comanda:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex5.PNG"/>


3. Com podem mirar el número de pàgines modificades (dirty pages)? I el número total de pàgines?

Amb la comanda SHOW ENGINE INNODB STATUS

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/5Ex5.PNG"/>

Número total de pàgines

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/6Ex5.PNG"/>

Número de pàgines modificades

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/7Ex5.PNG"/>

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

Primer comprobar la conexió entre hosts:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex6.PNG"/>


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/2Ex6.PNG"/>

A continuació, habilitar la configuració remota del hosts en my.cnf
i comentar la linea skip-networking i bind-address=0.0.0.0
En els dos servidors percona.


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/3Ex6.PNG"/>


Ara, cal habilitar els usuaris que es conectaran a mysql:


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/4Ex6.PNG"/>

També tenim que afegir la linea Federated a my.cnf:


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/5Ex6.PNG"/>

OPCIÓ1:

1- Afegim dades o utilitzem les ja creades en el servidor remot

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-1.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-2.PNG"/>

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-3.PNG"/>

2- Fem la conexió en el servidor remot amb grant select on sakila.* to 'root'@'10.0.2.16' identified by 'patata';

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-4.PNG"/>

3- En el client, afegim a la taula o creem una nova al final de la creació d'aquesta: CONNECTION='mysql://root:patata@10.0.2.16:3306/sakila/provafederated';

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-5.PNG"/>

4- Comprovem que el client té les taules amb les dades del servidor remot amb select * from provafederated

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-6.PNG"/>


OPCIÓ2:

Creem el nom de server i el conectem amb només el nom del server i la taula:


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-7.PNG"/>


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/Fed-8.PNG"/>


4. Checkpoint: Mostra al professor la configuració que has hagut de realitzar i el seu funcionament.



Activitat 7. Storage Engine CSV (1 punt)


1. Documenta i posa exemple de com utilitzar ENGINE CSV.

Per utilitzar CSV engine només fa falta utilitzar ENGINE = CSV en una nova taula:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex7.PNG"/>

2. Cal documentar els passos que has hagut de realitzar per preparar l'exemple: configuracions, instruccions DML, DDL, etc....

Instruccions DDL:

<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/1Ex7.PNG"/>


Instruccions DML:


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/2Ex7.PNG"/>


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/3Ex7.PNG"/>

Els arxius físics de la base de dades sakila creats amb engine csv:


<img src="https://github.com/IAMOR13/BBDD2/blob/master/Activitat%203/IMG/4Ex7.PNG"/>


3. Checkpoint: Mostra al professor la configuració que has hagut de realitzar i el seu funcionament.

