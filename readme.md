/*

Per lavorare on-line
https://sqliteonline.com/

*/


1) Connettersi al DB  -> mysql -h localhost -P 3306 -u root -p 
                                ^host           ^port  ^user  ^password
								
2) Creare un nuvo schema di database (nella finestra degli schemi tasto destro 'nuovo schema')

3) Creare una tabella per lo schema (verificare che lo schema è in neretto e quindi è il default schema)

CREATE TABLE `ordini` (
  `ID` int NOT NULL AUTO_INCREMENT,
  `Invoice` varchar(255) DEFAULT NULL,
  `StockCode` varchar(255) DEFAULT '',
  `Description` varchar(255) DEFAULT '',
  `Quantity` int DEFAULT NULL,
  `InvoiceDate` DATE DEFAULT NULL,
  `Price` double DEFAULT '0',
  `CustomerID` int DEFAULT NULL,
  `Country` varchar(255) DEFAULT '',
  `InvoiceTime` varchar(255) DEFAULT NULL,
  PRIMARY KEY (ID),
  UNIQUE KEY ORDINI_KEY(Invoice,StockCode)
);



CREATE TABLE corsi(
codice int NOT NULL PRIMARY KEY, 
titolo varchar(20) NOT NULL,
cfu int NOT NULL)




Click sul pulsante aggiorna (ICONCINA accanto alla scritta SCHEMAS)

4) Inseriamo un PO' DI record nella tabella

INSERT INTO ordini(Invoice,StockCode,Description,Quantity,InvoiceDate,Price,CustomerID,Country,InvoiceTime) 
VALUES 
('489434','85048','15CM CHRISTMAS GLASS BALL 20 LIGHTS',12,str_to_date("12/01/2009","%d/%m/%Y"),6.95,13085,'United Kingdom','07:45')

,
('489434','79323P','PINK CHERRY LIGHTS',12,str_to_date("01/12/2009","%d/%m/%Y"),6.75,13085,'United Kingdom','07:45'),
('489434','79323W',' WHITE CHERRY LIGHTS',12,str_to_date("01/12/2009","%d/%m/%Y"),6.75,13085,'United Kingdom','07:45'),
('489434','22041','RECORD FRAME 7\" SINGLE SIZE ',48,str_to_date("01/12/2009","%d/%m/%Y"),2.1,13085,'United Kingdom','07:45'),
('489434','21232','STRAWBERRY CERAMIC TRINKET BOX',24,str_to_date("01/12/2009","%d/%m/%Y"),1.25,13085,'United Kingdom','07:45'),
('489434','22064','PINK DOUGHNUT TRINKET POT ',24,str_to_date("01/12/2009","%d/%m/%Y"),1.65,13085,'United Kingdom','07:45'),
('489440','21871','SAVE THE PLANET MUG',24,str_to_date("01/12/2009","%d/%m/%Y"),1.25,13085,'United Kingdom','09:45'),
('489440','21523','FANCY FONT HOME SWEET HOME DOORMAT',10,str_to_date("01/12/2009","%d/%m/%Y"),5.95,13085,'United Kingdom','09:45');

INSERT INTO ordini(Invoice,StockCode,Description,Quantity,InvoiceDate,Price,CustomerID,Country,InvoiceTime) VALUES 
('491667','22196','SMALL HEART MEASURING SPOONS',1,str_to_date("10/12/2009","%d/%m/%Y"),0.85,15503,'Italy','10:20'),
('491662','21733','RED HANGING HEART T-LIGHT HOLDER',1,str_to_date("10/12/2009","%d/%m/%Y"),2.95,15503,'France','11:45'),
('491662','20697','LITTLE GREEN MONSTER SOFT TOY',1,str_to_date("13/12/2009","%d/%m/%Y"),2.55,15503,'United Kingdom','11:33'),
('491662','20982','12 PENCILS TALL TUBE SKULLS',1,str_to_date("13/12/2009","%d/%m/%Y"),0.85,15503,'United Kingdom','11:33'),
('491662','21544','SKULLS  WATER TRANSFER TATTOOS ',1,str_to_date("13/12/2009","%d/%m/%Y"),0.85,15503,'United Kingdom','11:33'),
('491662','21723','ALPHABET HEARTS STICKER SHEET',1,str_to_date("13/12/2009","%d/%m/%Y"),0.85,15503,'United Kingdom','11:33'),
('491666','17108D','FLOWER FAIRY SUMMER BOUQUET SACHET',48,str_to_date("13/12/2009","%d/%m/%Y"),0.42,13026,'United Kingdom','11:34'),
('491666','35095B','RED VICTORIAN FABRIC OVAL BOX',24,str_to_date("13/12/2009","%d/%m/%Y"),0.42,13026,'France','11:34'),
('491666','72789','BASKET/8 SCENTED LOVE TOKEN CANDLES',12,str_to_date("13/12/2009","%d/%m/%Y"),3.75,13026,'United Kingdom','11:34'),
('491666','84937','KASHMIR FOLKART TUMBLERS',6,str_to_date("13/12/2009","%d/%m/%Y"),2.1,13026,'France','11:34'),
('491666','17003','BROCADE RING PURSE ',36,str_to_date("13/12/2009","%d/%m/%Y"),0.21,13026,'United Kingdom','11:34'),
('491666','21136','PAINTED METAL PEARS ASSORTED',8,str_to_date("13/12/2009","%d/%m/%Y"),1.69,13026,'USA','11:34'),
('491666','22178','VICTORIAN GLASS HANGING T-LIGHT',12,str_to_date("13/12/2009","%d/%m/%Y"),1.25,13026,'United Kingdom','11:34'),
('491666','85178','VICTORIAN SEWING KIT',12,str_to_date("13/12/2009","%d/%m/%Y"),1.25,13026,'United Kingdom','11:34'),
('491666','85224','ASSORTED COLOUR SILK GLASSES CASE',12,'13/12/2009","%d/%m/%Y"),2.1,13026,'United Kingdom','11:34'),
('491666','17090D','VANILLA INCENSE 40 CONES IN TIN',6,str_to_date("13/12/2009","%d/%m/%Y"),1.25,13026,'United Kingdom','11:34'),
('491666','17090A','LAVENDER INCENSE 40 CONES IN TIN',6,str_to_date("13/12/2009","%d/%m/%Y"),1.25,13026,'United Kingdom','11:34'),
('491669','20829','GLITTER HANGING BUTTERFLY STRING',8,str_to_date("13/12/2009","%d/%m/%Y"),2.1,13026,'France','12:31'),
('491669','21114','LAVENDER SCENTED FABRIC HEART',10,str_to_date("13/12/2009","%d/%m/%Y"),1.25,13026,'United Kingdom','12:31');

INSERT INTO ordini(Invoice,StockCode,Description,Quantity,InvoiceDate,Price,CustomerID,Country,InvoiceTime) VALUES 
(491714,'85152','HAND OVER THE CHOCOLATE   SIGN ',2,'13/12/2009',2.1,16409,'United Kingdom','15:38'),
(491714,'22117','METAL SIGN HER DINNER IS SERVED ',1,'13/12/2009',2.95,16409,'United Kingdom','15:38'),
(491714,'82599','FANNY\'S REST STOPMETAL SIGN',1,'13/12/2009',2.1,16409,'United Kingdom','15:38'),
(491714,'21175','GIN + TONIC DIET METAL SIGN',3,'13/12/2009',2.1,16409,'United Kingdom','15:38'),
(491714,'82494L','WOODEN FRAME ANTIQUE WHITE ',1,'13/12/2009',2.95,16409,'United Kingdom','15:38'),
(491714,'84596B','SMALL DOLLY MIX DESIGN ORANGE BOWL',1,'13/12/2009',1.25,16409,'United Kingdom','15:38'),
(491714,'84596B','SMALL DOLLY MIX DESIGN ORANGE BOWL',1,'13/12/2009',1.25,16409,'United Kingdom','15:38'),
(491714,'84596F','SMALL MARSHMALLOWS PINK BOWL',1,'13/12/2009',1.25,16409,'United Kingdom','15:38'),
(491714,'84596F','SMALL MARSHMALLOWS PINK BOWL',1,'13/12/2009',1.25,16409,'United Kingdom','15:38'),
(491714,'84596K','JELLY BABIES YELLOW SMALL BOWL',1,'13/12/2009',1.25,16409,'United Kingdom','15:38'),
(491714,'84879','ASSORTED COLOUR BIRD ORNAMENT',8,'13/12/2009',1.69,16409,'United Kingdom','15:38'),
(491714,'72756','FAIRY CAKE CANDLES',9,'13/12/2009',1.49,16409,'United Kingdom','15:38'),
(491714,'84839','SWEETHEART KEY CABINET',1,'13/12/2009',6.75,16409,'United Kingdom','15:38'),
(491714,'21976','PACK OF 60 MUSHROOM CAKE CASES',2,'13/12/2009',0.55,16409,'United Kingdom','15:38'),
(491714,'21213','PACK OF 72 SKULL CAKE CASES',2,'13/12/2009',0.55,16409,'United Kingdom','15:38'),
(491714,'84989A','75 GREEN FAIRY CAKE CASES',2,'13/12/2009',0.55,16409,'United Kingdom','15:38'),
(491714,'21215',' IVORY PAPER CUP CAKE CASES ',2,'13/12/2009',0.55,16409,'United Kingdom','15:38'),
(491714,'84991','60 TEATIME FAIRY CAKE CASES',2,'13/12/2009',0.55,16409,'United Kingdom','15:38'),
(491714,'21975','PACK OF 60 DINOSAUR CAKE CASES',2,'13/12/2009',0.55,16409,'United Kingdom','15:38'),
(491720,'84992','72 SWEETHEART FAIRY CAKE CASES',2,'13/01/2009',0.55,16409,'United Kingdom','15:42'),
(491720,'21977','PACK OF 60 PINK PAISLEY CAKE CASES',2,'13/01/2010',0.55,16409,'United Kingdom','15:42'),
(491720,'21212','PACK OF 72 RETRO SPOT CAKE CASES',2,'13/01/2010',0.55,16409,'United Kingdom','15:42')
         |
		 V
corr
INSERT INTO ordini(Invoice,StockCode,Description,Quantity,InvoiceDate,Price,CustomerID,Country,InvoiceTime) VALUES 
(491714,'85152','HAND OVER THE CHOCOLATE   SIGN',2,str_to_date("13/12/2009","%d/%m/%Y"),2.1,16409,'United Kingdom','15:38'),
(491714,'22117','METAL SIGN HER DINNER IS SERVED',1,str_to_date("13/12/2009","%d/%m/%Y"),2.95,16409,'United Kingdom','15:38'),
(491714,'82599','FANNY\'S REST STOPMETAL SIGN',1,str_to_date("13/12/2009","%d/%m/%Y"),2.1,16409,'United Kingdom','15:38'),
(491714,'21175','GIN + TONIC DIET METAL SIGN',3,str_to_date("13/12/2009","%d/%m/%Y"),2.1,16409,'United Kingdom','15:38'),
(491714,'82494L','WOODEN FRAME ANTIQUE WHITE',1,str_to_date("13/12/2009","%d/%m/%Y"),2.95,16409,'United Kingdom','15:38'),
(491714,'84596B','SMALL DOLLY MIX DESIGN ORANGE BOWL',1,str_to_date("13/12/2009","%d/%m/%Y"),1.25,16409,'United Kingdom','15:38'),
(491714,'84596F','SMALL MARSHMALLOWS PINK BOWL',1,str_to_date("13/12/2009","%d/%m/%Y"),1.25,16409,'United Kingdom','15:38'),
(491714,'84596K','JELLY BABIES YELLOW SMALL BOWL',1,str_to_date("13/12/2009","%d/%m/%Y"),1.25,16409,'United Kingdom','15:38'),
(491714,'84879','ASSORTED COLOUR BIRD ORNAMENT',8,str_to_date("13/12/2009","%d/%m/%Y"),1.69,16409,'United Kingdom','15:38'),
(491714,'72756','FAIRY CAKE CANDLES',9,str_to_date("13/12/2009","%d/%m/%Y"),1.49,16409,'United Kingdom','15:38'),
(491714,'84839','SWEETHEART KEY CABINET',1,str_to_date("13/12/2009","%d/%m/%Y"),6.75,16409,'United Kingdom','15:38'),
(491714,'21976','PACK OF 60 MUSHROOM CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:38'),
(491714,'21213','PACK OF 72 SKULL CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:38'),
(491714,'84989A','75 GREEN FAIRY CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:38'),
(491714,'21215',' IVORY PAPER CUP CAKE CASES ',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:38'),
(491714,'84991','60 TEATIME FAIRY CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:38'),
(491714,'21975','PACK OF 60 DINOSAUR CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:38'),
(491720,'84992','72 SWEETHEART FAIRY CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:42'),
(491720,'21977','PACK OF 60 PINK PAISLEY CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:42'),
(491720,'21212','PACK OF 72 RETRO SPOT CAKE CASES',2,str_to_date("13/12/2009","%d/%m/%Y"),0.55,16409,'United Kingdom','15:42')

5) Visualizziamo tutti i record della tabella, ma solo alcuni campi

select ID, Invoice, StockCode, Description
from ordini

update
UPDATE ordini SET Quantity = 3 WHERE id=38;
        ^tabella    ^campo    

DESCRIBE ordini; mostra schema tabella ordini

MONTH(campo) = 12 tutti i dati mese = 12		

ESERCIZIO 
Crea una query in cui visualizzi ID, Invoice ed il prezzo non espresso in dollari
ma in euro (tenendo presente per esempio che un euro sono 1,5 dollari)
Suggerimento: nel campo SELECT devi fare una moltiplicazione

SELECT ID,invoice, ROUND(price/1.5,2) as euro from ordini;

ESERCIZIO 
Crea una query in cui visualizzi ID, Invoice ed importo finale
dove l'importo finale è il prezzo per la quantità

SELECT ID,invoice, round(price/1.5,2) as euro,round((price/1.5*Quantity),2)as importo_finale from ordini;


6) Visualizziamo tutti i record della tabella con tutti i campi

select *
from ordini

7) Selezioniamo/visualizziamo solo un sottoinsieme di ordini, quelli in cui il prezzo è maggiore di 3

select *
from ordini
where Price >= 3

select *
from ordini
where Price >=3 AND Price<7


ESERCIZIO
Selezionare tutti gli ordini avvenuti il 13/12/2009
Selezionare tutti gli ordini avvenuti il 13/12/2009 e (AND) il cui prezzo > 3  ->  SELECT * FROM ordini WHERE price > 3 AND InvoiceDate = 13/12/2009;
Selezionare tutti gli ordini avvenuti il 10/12/2009 oppure (OR) il 13/12/2009  ->  SELECT * FROM ordini WHERE InvoiceDate = 10/12/2009 AND InvoiceDate = 13/12/2009;


8) Visualizziamo gli ordini in cui la data è dicembre (mese = 12)

select *
from ordini
where mid(InvoiceDate,4,2)='12' 
^come stringa

oppure (query alternativa che fa la stessa cosa)


SELECT *
from ordini
where MONTH(str_to_date(InvoiceDate,"%d/%m/%Y"))=12 and DAY(str_to_date(InvoiceDate,"%d/%m/%Y"))=13
^come data

Osserva le due query. Le due query sono due modi diversi di ottenere lo stesso risultato. 
Nel primo caso lavoriamo
sulle stringhe. InvoiceData è una stringa. Nel secondo caso trasformiamo InvoiceData in una
data (una variabile di tipo Date) e poi lavoriamo con delle funzioni sulle date (es. MONTH)


9) Selezioniamo le date presenti nella tabella ordini

SELECT distinct InvoiceDate
from ordini 


ESERCIZIO
Selezionare i diverse paesi (Country) della tabella

ESERCIZIO
Selezionare le diverse coppie (Data, Paese) presenti nella tabella

ESERCIZIO
Selezionare ordini che provengono dal regno unito fatti la mattina (07 -> 12)

select * from ordini WHERE country = 'United Kingdom' AND  TIME_TO_SEC(InvoiceTime) > TIME_TO_SEC("07:00") AND TIME_TO_SEC(InvoiceTime) > TIME_TO_SEC("12:00");


10) Visualizziamo per ogni ordine una stringa che contiene la data dell'ordine stesso

select concat('Data ordine: ',InvoiceDate,' - Ora ordine: ',InvoiceTime)
from ordini
where MONTH(str_to_date(InvoiceDate,"%d/%m/%Y"))=12 and DAY(str_to_date(InvoiceDate,"%d/%m/%Y"))=13

Quindi: la where definisce i record selezionati. LA select definisce cosa viene mostrato di questi records.

11) Tutti gli ordini in cui nella descrizione è presente la parola WHITE (attenzione al casting maiuscole/minuscole)
select *
from ordini
where Description LIKE '%WHITE%'

alternativa NOT LIKE  = diverso

'%WHITE%' significa %=qualunque cosa   (qualunque cosa prima)WHITE(qualunque cosa)
 _ = carattere jolly 
 
 select * from ordini WHERE country IN ('Italy','France'); IN() prende solo i valori selezionati 


"""
ESERCIZIO: scrivere una query che seleziona tutti i record relativi ad ordine del giorno 13 che contengono la 
           parola RED   (USARE OPERATORE 'AND' NELLA WHERE)
"""


"""
ESERCIZIO: scrivere una query che seleziona tutti i record relativi ad ordine del giorno 13 che contengono la 
           parola RED oppure la parola WHITE  (USARE OPERATORE OR NELLA WHERE)
"""



Andiamo ora a vedere alcuni esercizio sulla GROUP BY. 

12) Visualizziamo una tabella con la data e il numero di ordini per quella data

select InvoiceDate, count(*) as NumeroOrdini
from ordini
group by InvoiceDate
 
Da notare 'as' nella SELECT  che ci permette di stabilire il nome di un campo in visualizzazione.

I record della query (che in questo esempio sono tutti i records) sono raggruppati in base a InvoiceDate
e su ciascun gruppo è applicata una funzione (in questo esempio count  cioè il conteggio)


13) Stessa query della precedente solo che, sugli ordini di ciascun giorno, oltre a contarli, calcoliamo 
    anche il prezzo medio

select InvoiceDate, count(*) as NumeroOrdini, avg(Price) as PrezzoMedio
from ordini
group by InvoiceDate

avg sta per average ed indica la media. 


"""
Esercizio 
Esegui le stesse due query precedenti, solo che invece che raggruppare per data, raggruppa per Ora della 
giornata. Es. tutti gli ordini fatti alle 9 di qualunque giorno.
"""

"""
Esercizio 
Esegui le stesse due query precedenti, solo che invece che raggruppare per data, raggruppa per Ora della 
giornata. Es. tutti gli ordini fatti alle 9 di qualunque giorno. Attenzione perchè due ordini
fatti alle 11:33 il primo e alle 11:34 il secondo devono essere raggruppati. 

Questo significa che non devi fare GROUP BY InvoiceTime ma GROUP BY LEFT(InvoiceTime,2).

Alternativamente puoi trasformare InvoiceTime in una variabile di tipo time e ricavare l'ora. 
Abbiamo fatto un esercizio che faceva questo per le date.
"""

"""
Esercizio 
Esegui le stesse due query 12 e 13, solo che invece di riportare il numero di ordini (COUNT) riportare
per ciascuna data, il numero di prodotti venduti (Quantity) ma questa volta i numeri di Quantity devono
essere sommati (sum).

"""




ESERCIZIO

Supponiamo di essere AMAZON e di avere la tabella ORDINI con milioni di record. Nella tabella
ci sono tutti gli ordini di AMAZON di questi ultimi 5 anni. Quindi milioni di record.

AMAZON mette a disposizione dei suoi agenti di marketing una dashboard con la quale è possibile vedere
l'andamento degli ordini. 


Per esempio un tasto permette di visualizzare tutti gli ordini dell'ora corrente. Se adesso
è il 3 aprile 2019 e sono le 14:20, premendo quel tasto vedi tutti gli ordini del 3 aprile 2019 
nella fascia oraria 14 e quindi dalle 14:00 alle 14:20.

Quale query viene fatta per ottenere quei dati? Prova a scriverla. Tieni conto che nella WHERE devi
usare una funzione che ti restituisce l'ora corrente. Per provare la tua query inserisci 5 records della
tabella ordini, METTENDO LA DATA E L'ORA AI VALORI CORRENTI. Poi
esegui la query e verifichi se ottieni proprio quei 5 record come risultato.
(La query è questa qui sotto. Devi solo MODIFICARE le date e le ore)

INSERT INTO ordini(Invoice,StockCode,Description,Quantity,InvoiceDate,Price,CustomerID,Country,InvoiceTime) VALUES 
(509434,'85048','15CM CHRISTMAS GLASS BALL 20 LIGHTS',12,'03/04/2019',6.95,13085,'United Kingdom','11:05'),
(509434,'79323P','PINK CHERRY LIGHTS',12,'03/04/2019',6.75,13085,'United Kingdom','11:45'),
(509435,'79323W',' WHITE CHERRY LIGHTS',12,'03/04/2019',6.75,13085,'United Kingdom','11:45'),
(509435,'22041','RECORD FRAME 7\" SINGLE SIZE ',48,'03/04/2019',2.1,13085,'United Kingdom','11:45'),
(509435,'21232','STRAWBERRY CERAMIC TRINKET BOX',24,'03/04/2019',1.25,13085,'United Kingdom','11:45')

ATTENZIONE: la query è unica ed è valida per tutti i giorni della vita. Questo significa che nella
query non vi devono essere delle date, per esempio la data di oggi. 
Deve essere usata una funzione che da come valore di ritorno la data di oggi (es. CURDATE()).
La stessa cosa vale per l'ora (curtime())



Se non ci riesci visualizza la query nel file esercizio1_1.txt. Osserva
com'è fatta la query. Eseguila e verifica che funziona.
