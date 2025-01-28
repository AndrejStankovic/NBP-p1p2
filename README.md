# NBP-p1p2

Tema 2. projekta
Aplikacija koja ce omoguciti pamcenje i izmenu informacija o korisnicima pretplatnickih aplikacija. 
Pamtiti pretplatu koju imaju kod provider-a i mogucnost izmene. 
Cassandra ce se koristiti kao distribuirani servis koji ce cuvati veliki broj zapisa u bazi i kreiranje modela ce biti prema upitima.

Tema 1. projekta
Aplikacija koja ce omoguciti pamcenje i izmenu informacija o korisnicima pretplatnickih aplikacija. 
Pamtiti pretplatu koju imaju kod provider-a i mogucnost izmene. 
Redis ce se koristiti kao distribuirani lock prilikom iznajmljivanja opreme korisnicima.


Cassandra:
Napraviti tabele u cassandra bazi, helperFunctions::generateUsers() ce automatski popuniti podacima. recordCount je postavljen na 100 zapisa.
User i Subscription demonstrirarju rad sa bazom i manipulacijom podacima, pokrivene su sve CRUD operacije u obe tabele.

Redis:
codeList je deljeni resurs izmedju korisnika aplikacije i administratora koji treba generise podatke u listi. 
Zauzeti lockTelekom na 10 sekundi radi simulacije distribuiranog lock-a kada je recimo zauzet od strane drugog korisnika ili administratora.

User - moguce dodavanje, azuriranje, brisanje, citanje automatski unosom jmbg vrednosti.
Subscription - moguce dodavanje, azuriranje, brisanje, citanje automatski unosom jmbg vrednosti. Pribavljanje sifre po principu distribuiranog lock-a, a 
brisanje iz baze znaci da se sifra oslobadja i ona se vraca nazad u bazu. Ova sifra predstavlja sifru uredjaja koji korisnik dobija na koriscenje. Nije je 
moguce rucno uneti. Pokrivena logika unosa, izmena, brisanja ukoliko neki podaci nisu uneseni ili ne postoji korisnik ili neki podatak. Ako postoji unos sifra se
ne pribavlja.

qDebug() nisam brisao jer meni sluzi kao podsetnik
.gitignore nije dodat, prebacujem kompletan projekat