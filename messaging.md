# SPA – Správy (Messaging)

## Premenné

Pri vytváraní správy môžete použiť **premenné systému**.  
Pri odoslaní správy systém automaticky nahradí premenné skutočnými údajmi o príjemcovi, programe alebo tréningu.

Príklad:

Dobrý deň {parent_first_name},  
tréning programu {program_title} sa dnes koná o {training_time}.



### Syntax premenných

Premenné zapisujte v zložených zátvorkách: {nazov_premennej}
Príklady: {parent_first_name} , {child_first_name} , {program_title}


#### Dostupné premenné

### Rodič
{parent_name} – celé meno rodiča, {parent_first_name} – krstné meno rodiča, {parent_last_name} – priezvisko rodiča, {parent_email} – email rodiča  

### Dieťa
{child_name} – celé meno dieťaťa, {child_first_name} – krstné meno dieťaťa, {child_last_name} – priezvisko dieťaťa  

### Dospelý účastník (spa_client)
{client_name} – celé meno dospelého účastníka, {client_first_name} – krstné meno dospelého účastníka, {client_last_name} – priezvisko dospelého účastníka, {client_email} – email dospelého účastníka  

### Program a registrácia
{program_title} – názov programu, {registration_id} – interné ID registrácie  

### Tréning
{trainer_name} – meno trénera, {trainer_first_name} – krstné meno trénera, {trainer_last_name} – priezvisko trénera, {training_date} – dátum tréningu, {training_time} – čas tréningu, {place_name} – miesto tréningu  

### Platba
{payment_amount} – suma platby, {payment_due_date} – dátum splatnosti, {vs} – variabilný symbol,

### Systém
{site_name} – názov webu / akadémie, {site_url} – adresa webu  

#### Zmena hesla
{user_first_name} – meno používateľa, {user_email} – prihlasovací email  
{reset_password_wp_url} – štandardný WordPress odkaz na vytvorenie nového hesla (`wp-login.php` s `action=rp`), doplnené o `wp_lang` podľa jazyka používateľa / webu; používa sa v emailovej šablóne pri zmene hesla  

#### Zmena PIN (dieťa)
{child_first_name} – meno dieťaťa, {child_last_name} – priezvisko dieťaťa, {child_pin} – nový PIN kód  

### Príklad správy

Dobrý deň {parent_first_name},

tréning programu **{program_title}** sa bude konať:

dátum: {training_date}  
čas: {training_time}  
miesto: {place_name}

Tešíme sa na vás.

{site_name}

* * * * * *

Systém pri odoslaní správy automaticky nahradí všetky premenné konkrétnymi údajmi príjemcu.