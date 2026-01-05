# MarijanBus - Web servis za Marijan BUS d.o.o.

**Link na stranicu:** [https://marijanbus.click/](https://marijanbus.click/)

---

## Napomena o repozitoriju

**Ovaj repozitorij sadrži opis projekta.**  
Zbog rukovanja osjetljivim i privatnim podacima (osobni podaci klijenata, poslovne informacije, sigurnosni ključevi), **originalni radni repozitorij nije javno dostupan**.    
Ovdje se nalazi:  
- Detaljan opis funkcionalnosti
- Dokumentacija arhitekture
- Tehnološki stack
- Upute za lokalni razvoj i deployment

---

## O projektu

**MarijanBus** je kompletan web servis razvijen za potrebe autobusne prijevozničke tvrtke _Marijan BUS d.o.o._  
Sustav omogućava korisnicima pregled voznog reda, online rezervacije, upravljanje korisničkim računima te administratorima potpunu kontrolu nad voznim redovima, rezervacijama i korisnicima. 

Projekt se sastoji od:
- **Frontend** – React (Vite) + Tailwind CSS
- **Backend** – FastAPI + PostgreSQL
- **Deployment** – vlastiti VPS server s Cloudflare Tunnel integracijom

---

## Ključne funkcionalnosti


- Autentikacija i autorizacija korisnika (JWT, RBAC)  
- Administratorska ploča za upravljanje voznim redovima i rezervacijama  
- E-mail notifikacije (potvrde rezervacija, podsjetnici)  
- Responzivan dizajn (desktop, tablet, mobile)  
- Sigurna komunikacija (HTTPS, Cloudflare zaštita)  

---

# Frontend

**MarijanBus Frontend** je korisničko sučelje izrađeno korištenjem **React (Vite)** i **Tailwind CSS**, s ciljem stvaranja modularnog, responzivnog i brzog web sučelja.

## Tehnologije

- **React** – komponentno frontend sučelje
- **Vite** – alat za brzi razvoj i build
- **Tailwind CSS** – utility-first stiliziranje
- **React Router** – za navigaciju po stranicama
- **Axios** – HTTP klijent za slanje zahtjeva prema backendu
- **Heroicons** – moderna SVG ikonografija
- **React Hook Form + Zod** – upravljanje i validacija formi

## Struktura projekta

```
src/
├── assets/              # Slike, logo, ikone
├── components/          # Ponovno iskoristive komponente (HeroSection, PriceCard, ReviewList, ...)
├── pages/               # Stranice (Home.jsx, Cjenik.jsx, Kontakt.jsx, ...)
├── routes/              # Definirane rute aplikacije
├── App.jsx              # Glavna aplikacija
├── main. jsx             # Ulazna točka (Vite)
```


# Backend

**MarijanBus Backend API** je backend sustav temeljen na **FastAPI** frameworku s integriranom **PostgreSQL** bazom, **JWT** autentikacijom, **RBAC** autorizacijom te podrškom za **e-mail notifikacije**.

## Tehnologije

- **FastAPI** – moderan Python web framework
- **SQLAlchemy** – ORM za rad s bazom podataka
- **PostgreSQL** – relacijska baza podataka
- **Alembic** – alat za migracije baze
- **FastAPI Users** – autentikacija i OAuth2 integracija
- **Pydantic** – validacija i parsiranje podataka
- **Nodemailer (SMTP)** – slanje e-mail poruka (preko Gmail-a ili vlastitog SMTP-a)
- **Docker** – kontejnerizacija aplikacije
- **Cloudflare Tunnel** – sigurno izlaganje API-ja bez otvaranja portova

## Struktura projekta

```
backend/
├── app/
│   ├── main.py              # Ulazna točka (FastAPI aplikacija)
│   ├── api/                 # API rute (/auth, /users, /reservations...)
│   ├── models/              # SQLAlchemy modeli baze
│   ├── schemas/             # Pydantic sheme za validaciju
│   ├── services/            # Poslovna logika (notifikacije, rezervacije...)
│   └── core/                # JWT, RBAC, konfiguracija, sigurnost
├── alembic/                 # Migracije baze podataka
├── requirements.txt         # Python dependency lista
└── . env                     # Konfiguracijske varijable (tajni ključevi, DB URL...)
```


## API Dokumentacija

Backend API dokumentacija dostupna je na: 
- **Swagger UI:** [`https://marijanbus.click/docs`](https://marijanbus.click/docs)
- **ReDoc:** [`https://marijanbus.click/redoc`](https://marijanbus.click/redoc)

*(Za lokalnu verziju:  `http://localhost:8000/docs` i `http://localhost:8000/redoc`)*

---

## Deployment

Aplikacija je deployirana na:
- **VPS server** (vlastiti hosting)
- **Cloudflare Tunnel** – za sigurnu i brzu dostavu sadržaja
- **PostgreSQL baza** – hostirana na istom serveru
- **HTTPS** – SSL certifikati kroz Cloudflare

---


## Kontakt

Za pitanja ili suradnju:
- **GitHub:** [@MarkoSokser](https://github.com/MarkoSokser)


