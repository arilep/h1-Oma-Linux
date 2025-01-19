# Tehtävä x) Raportin kirjoittaminen

- Raportin tulisi olla selkeä ja raportin pohjalta tulisi olla mahdollista päästä samaan lopputulokseen toisen käyttäjän seuraamana.
- Raportissa tulisi selvitä minkälaisessa ympäristössä työ on toteutettu (millainen tietokone, specsit, verkko, ajankohdat).
- Raportissa on tärkeää ilmoittaa vaihe-vaiheelta, mitä kussakin työvaiheessa on tehty. Myös erinäiset vikailmoitukset/ongelmat tulisi mainita raportissa ja kuinka ne on ratkaistu ja mistä vian arvellaan johtuneen.
- Raportti tulisi esittää menneessä aikamuodossa.
- Raportin helppolukuisuutta voi parantaa monin tavoin, esim. Väliotsikointi ja raportin loppuun ns. TLDR (“Too long didn’t read) josta selviää raportti tiivistettynä muutamaan lauseeseen.
- Lähdeviittaukset kuuluvat hyvään raporttiin.
- Raportissa plagiointi, luvaton kuvien käyttö ja ns. “sepittäminen” (työvaiheet joita väitetysti tehty, vaikka näin ei ole) ovat vilppiä.
- Raportti voi sisältää hyviä vakiotekstejä, jotka kertovat esimerkiksi luvasta kopioida ja muokata dokumenttia ( > Lisenssit).

### Lähteet:
Karvinen, T. 4.6.2006. Raportin kirjoittaminen. Luettavissa: https://terokarvinen.com/2006/raportin-kirjoittaminen-4/. Luettu 18.1.2025.

# Tehtävä x) Free Software Foundation – What is Free Software?

- Tiivistettynä Free Softwarella (suom. Vapaa Ohjelmisto) tarkoitetaan ohjelmistoja, joita käyttäjät voivat vapaasti käyttää, kopioida, jakaa/levittää, opiskella ja muokata tarpeensa mukaan.
- Termillä “Free” ei viitata ohjelmiston hintaan, vaan yllä oleviin oikeuksiin.
- Ohjelmistoa voidaan kutsua Free Softwareksi, mikäli se täyttää seuraavat neljä olennaista vapautta:
1. Käyttäjällä on vapaus käyttää ohjelmistoa kuten haluaa, mihin tahansa käyttötarkoitukseen.
2. Vapautta tutkia ja opiskella, miten ohjelmisto toimii ja muokata sitä halutessaan. Pääsy lähdekoodiin on edellytys tälle.
3. Vapaus levittää kopioita ohjelmistosta ja täten auttaa muita käyttäjiä.
4. Vapaus levittää muokkaamiasi kopioita ohjelmistosta ja täten hyödyttää muita käyttäjiä. Pääsy lähdekoodiin on edellytys myös tälle.
- Free Software voi olla kaupallista (kaupallinen käyttö, kehitys ja jakelu).

### Lähteet:
Free Software Foundation. What is Free Software? Luettavissa: https://www.gnu.org/philosophy/free-sw.html. Luettu 18.1.2025.

# Tehtävä a) Linuxin asennus virtuaalikoneeseen

### Ympäristö

- Käyttöjärjestelmä: Windows 11 Home 64-bit
- Suoritin: AMD Ryzen 7 5800X 8-Core Processor
- Muisti: 32GB RAM
- Näytönohjain: NVIDIA GeForce RTX 3080

### Internet yhteys

- DNA Netti 400M (Download 400Mbps / Upload 200Mbps)


Oracle VM VirtualBox oli jo valmiiksi asennettuna koneelleni. VirtualBoxin voi ladata osoitteesta https://www.virtualbox.org/

Debian Iso-tiedoston latasin osoitteesta:
https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/
> Sivulta valitsin: debian-live-12.9.0-amd64-cinnamon.iso koko 3.2G.
Tiedoston lataamisessa meni ~3 minuuttia.

![image](https://github.com/user-attachments/assets/489852e1-093c-4cc7-a7f8-5ed14cdadc05)

Asennuksen aloitus Machine > New…

### Name and Operating System
- Annoin nimeksi: DebianAp
- Valitsin aiemmin ladatun debianin iso -tiedoston ISO-Image alasvetovalikosta.
- Valitsin Version > Debian (64-bit). Oletuksena oli 32-bit versio.

### Unattended Install
- Syötin käyttäjätunnuksen ja salasanan sekä Hostnamen ja Domain Namen.

### Harware
- Määritin Base Memory: 8000MB ja Prosessorien määräksi 4.

### Hard Disk
- Virtuaalikovalevylle määritin kooksi 60GB.

Aloitin asennustyöt 18.35, samalla raporttia kirjoittaen.
Heti alkuun sain ilmoituksen “The virtual machine failed to boot”. Kiva juttu. Valitsin tässä kohtaa ISO-tiedoston uudelleen “Mount and Retry Boot”.

Selvisin onneksi säikähdyksellä. Pääsin jatkamaan eteenpäin ja pääsin aloitusnäkymään (Boot menu). Jatkoin ensimmäisellä vaihtoehdolla: Live system (amd64).

18.37 Mustan ruudun jälkeen pääsin sisään työpöydälle. Työpöydällä oli vain yksi kuvake “Install Debian”, josta pääsin aloittamaan asennuksen.

### Debian GNU/Linux Installer

Welcome ikkunasta jatkoin oletuksilla (American English) ja Next.

Location -kohdasta valitsin Region: Europe ja Zone: Helsinki.

Keyboard kohdassa valitsin Keyboard Model: Generic 105-key PC, Finnish ja Default. Testasin “Type here to test your keyboard” -kohdassa että näppäimistö pelittää ja jatkoin Next.

Partitions kohdasta täppä kohtaan Erase disk. Encrypt system -täpän jätin pois. Valitsin Boot loader location: Master Boot Record ja Next.

Users kohdassa syötin nimi, käyttäjätunnus ja salasanatiedot. “Log in automatically…” -täppä jäi pois.

Aika tarkistaa Summary -ikkunassa että syötetyt tiedot ovat oikein. Tämän jälkeen jatkoin “Install”.

![image](https://github.com/user-attachments/assets/e3365a19-91c7-4dfa-ac0d-ad931f83484c)

Asennuksen aloitin 18.48 ja valmista tuli 18.54 eli vei noin kuutisen minuuttia. Finish -ikkunasta täppä Restart now ja Done.

![image](https://github.com/user-attachments/assets/a81fd152-9ff4-4de2-930c-5df6c4cb8fa6)

Lopputulos.

### Lähteet:
Karvinen, T. Install Debian on VirtualBox – Updated 2024. Luettavissa: https://terokarvinen.com/2021/install-debian-on-virtualbox/?fromSearch=install%20debian. Luettu 18.1.2025.

