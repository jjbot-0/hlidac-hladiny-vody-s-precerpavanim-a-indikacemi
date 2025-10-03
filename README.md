# hlidac-hladiny-vody-s-precerpavanim-a-indikacemi
Hlídač hladiny vody s automatickým přečerpáváním, generátorem a indikacemi

# Hlídač hladiny vody s automatickým přečerpáváním, generátorem a indikacemi

**Autor: Filip Salač**

---

## 📝 Stručný popis projektu

Cílem projektu je vytvořit funkční model zařízení, které sleduje hladinu vody v nádrži, automaticky spíná čerpadlo při překročení nastavené meze, a zároveň umožňuje vizualizaci stavu systému na displeji i v mobilním zařízení. Součástí je i demonstrace výroby elektrické energie z vody pomocí lopatkového kola nebo turbíny.

---

## 🔧 Hlavní funkce systému

- Měření hladiny vody a automatické spínání čerpadla při překročení meze
- Ochrana proti běhu čerpadla naprázdno (senzor nebo sledování proudu)
- Generátor poháněný vodou (lopatkové kolo / turbína)
- Zobrazení údajů na displeji: hladina, čerpadlo, napětí, teploty
- Reakce na pohyb (např. rozsvícení světla před domem)
- Webové rozhraní přístupné z mobilu/PC
- Napájení z baterie (12VDC olověný akumulátor,2,6 Ah)

---

## 💡 Použité technologie

- **Mikrokontrolér:** ESP32 s Wi-Fi a analogovými vstupy
- **Vývoj:** Arduino IDE
- **Senzory:** hladiny vody, teploty (1-Wire), pohybu (PIR)
- **Výstupy:** DC čerpadlo, OLED displej, světlo
- **Generátor:** DC motor poháněný vodou
- **Webový server:** běžící na ESP32

---

## 📆 Etapy projektu

### 0) Backend
Základ systému – napájení (2× Li-ion), řízení pomocí ESP32, DC-DC měniče pro 3,3V, 5V, 12V.

### 1) Řízení vody
Měření hladiny (vodivostní/ultrazvuk), spínání čerpadla, ochrana proti běhu nasucho.

### 2) Výroba energie
Padání vody z výšky (~1 m) přes kolo nebo turbínu → generátor → měření napětí/výkonu.

### 3) Displej
OLED/TFT displej cyklicky zobrazuje hladinu, teploty, napětí, stav čerpadla, výkon generátoru.

### 4) Interakce
PIR čidlo pro světlo, teplotní čidla DS18B20, možnost tlačítek nebo indikátorů.

### 5) Webové rozhraní
ESP32 jako web server pro zobrazení a případné ovládání přes mobilní zařízení.

---

<pre>
## 📁 Struktura repozitáře
<code>
├── code/              # Kód pro ESP32
├── fritzing/          # Schémata a návrhy zapojení
├── photos/            # Fotodokumentace projektu
├── docs/              # Technická dokumentace
├── partslist.md       # Seznam komponent
└── README.md          # Tento soubor
</code>
</pre>
