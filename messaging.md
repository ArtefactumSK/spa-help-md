# SPA – Správy (Messaging)

## Premenné

Pri tvorbe správ (email aj interné správy v SPA portáli) môžete použiť premenné,
ktoré sa pri odoslaní automaticky nahradia reálnymi údajmi o používateľovi,
registrácii, programe alebo platbe.

Premenné môžete zapisovať dvoma spôsobmi:

- `"{parent_first_name}"` – nový preferovaný zápis
- `"{{parent_first_name}}"` – pôvodný zápis, stále podporovaný kvôli spätnej kompatibilite

Odporúčame používať nový zápis s jednou sadou zložených zátvoriek (`{variable}`).

### Osobné údaje – rodič a dieťa

- **`{parent_name}`** – celé meno rodiča (ak je k dispozícii)
- **`{child_name}`** – celé meno dieťaťa (klienta)
- **`{parent_first_name}`** – krstné meno rodiča
- **`{parent_last_name}`** – priezvisko rodiča
- **`{child_first_name}`** – krstné meno dieťaťa
- **`{child_last_name}`** – priezvisko dieťaťa
- **`{parent_email}`** – email rodiča použitý pri registrácii

### Registrácia a program

- **`{registration_id}`** – interné ID registrácie
- **`{program_title}`** – názov programu (napr. „Karate Malacky – začiatočníci“)

### Tréning a miesto

- **`{trainer_name}`** – meno trénera (ak je dostupné v kontexte)
- **`{training_date}`** – dátum tréningu (napr. „12.3.2026“)
- **`{training_time}`** – čas tréningu (od–do, napr. „17:00 – 18:00“)
- **`{place_name}`** – názov miesta tréningu (telocvičňa, hala a pod.)

### Platby

- **`{payment_amount}`** – suma platby (napr. „59 €“)
- **`{payment_due_date}`** – dátum splatnosti platby
- **`{vs}`** – variabilný symbol platby (VS)

### Systémové údaje

- **`{site_name}`** – názov webu / akadémie
- **`{site_url}`** – URL webu

## Príklady použitia

### Príklad predmetu správy

```text
{program_title} – dôležité upozornenie pre rodičov
```

### Príklad textu emailu

```text
Dobrý deň {parent_first_name},

tréning programu {program_title}, ktorý sa koná dňa {training_date} v čase {training_time}
na mieste {place_name}, je dnes z organizačných dôvodov zrušený.

Ďakujeme za pochopenie.
Tím {site_name}
```

Pri odoslaní správy systém automaticky doplní konkrétne údaje za každú premennú,
tak aby rodič či klient dostal personalizovanú a zrozumiteľnú informáciu.

