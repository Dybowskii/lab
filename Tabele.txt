Create Table Klient
(	id_klienta int auto_increment primary key not null,
    imie        varchar(20),
    nazwisko    varchar(40),
    data_urodzenia    date,
    e_mail varchar(40),
    haslo varchar (30),
	numer_karty varchar (16),
    ulica        varchar(50),
    numer_domu    varchar (4),
    numer_mieszkania varchar(4),
    kod_pocztowy    varchar(6),
    miasto        varchar(30)
    );
Create Table Zamowienie
(id_zamowienia int primary key auto_increment not Null ,
id_klienta int,
id_subskrypcji int,
data_wykupienia_subskrypcji date,
data_wygasniecia_subskrypcji date
);
Create Table Subskrypcja
(id_subskrypcji int primary key auto_increment not Null ,
rodzaj_subskrypcji varchar(40),
Cena_subskrypcji int,
Maksymalna_jakosc varchar(40),
Maksymalna_ilosc_urzadzen int(1)
);
Create Table Film
(id_filmu int primary key auto_increment not Null ,
id_subskrypcji int not null,
Tytul varchar(40),
Rezyser varchar (60),
Gatunek varchar(30),
Czas_trwania_min int (3),
Jezyk varchar(30),
Polskie_napisy varchar(3),
Polski_lektor varchar(3),
rok_produkcji varchar(4),
data_dodania date
);
Create Table Serial
(id_serialu int primary key auto_increment not Null ,
id_subskrypcji int not null,
Tytul varchar(40),
Rezyser varchar (60),
Gatunek varchar(30),
liczba_sezonow int(2),
liczba_odcinkow_w_sezonie int(2),
rok_produkcji varchar (4),
zakonczony varchar(3),
Jezyk varchar(30),
Polskie_napisy varchar(3),
Polski_lektor varchar(3)
);


