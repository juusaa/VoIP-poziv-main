# VoIP poziv

Studentski projekat iz predmeta **Telekomunikacijski softver inženjering**. Cilj je omogućiti glasovni poziv između dva računara u lokalnoj mreži uz vlastiti tekstualni signalizacijski protokol po uzoru na SIP i vlastitu implementaciju G.711 kodeka.

## Status projekta

Dostupna je projektna dokumentacija. U pripremi je terminalski prototip za demonstraciju signalizacije. Cilj demonstracije je registrovati dva klijenta, uputiti poziv po korisničkom imenu, prikazati zvonjenje, prihvatiti ili odbiti poziv te staviti uspostavljeni poziv na čekanje, nastaviti ga i završiti ga s bilo koje strane. Očekivani ishodi uključuju i zauzetog ili neregistrovanog korisnika.

Prenos govora i integracija G.711 kodeka s klijentom predviđeni su za naredne faze.

## Arhitektura

- **Registrar** evidentira registrovane korisnike i njihove adrese te učestvuje u signalizaciji poziva.
- **Terminalski klijent** omogućava registraciju, upućivanje poziva i upravljanje dolaznim i aktivnim pozivima. Ista aplikacija pokreće se za oba učesnika.
- **Govorni tok** u završnoj verziji prenosit će G.711 pakete direktno između klijenata.

## Pokretanje i provjera

Za prototip je predviđen Python 3.11 ili noviji. U ovoj verziji repozitorija dostupni su projektni dokumenti. Naredbe za pokretanje registrara, dva klijenta i testova bit će dokumentovane uz prototip.

Scenarij demonstracije koristi jedan registrar i dva klijenta u zasebnim terminalima. Nakon registracije, prvi klijent poziva drugi po imenu. Na drugom klijentu provjeravaju se odbijanje i prihvatanje u odvojenim pokušajima. U prihvaćenom pozivu oba klijenta trebaju prikazati promjene pri čekanju, nastavku i završetku poziva.

## Dokumentacija

- [Vizija proizvoda](docs/vizija_proizvoda.pdf)
- [Funkcionalni zahtjevi](docs/funkcionalni_zahtjevi.pdf) ([LaTeX](docs/funkcionalni_zahtjevi.tex))
- [Osnovna arhitektura sistema](docs/osnovna_arhitektura_sistema.pdf)
- [Korisničke priče](docs/korisnicke_price.pdf)
- [Kriteriji prihvatanja](docs/kriteriji_prihvatanja.pdf)

## Razvoj

Zadaci i iteracije prate se na [projektnoj ploči](https://github.com/users/ihadzihasa/projects/1/views/1) (pristup za članove tima). Za korisničku priču koristi se radna grana. Promjene se predaju kroz pull request povezan s odgovarajućim issueom i pregledaju prije spajanja u `main`.
