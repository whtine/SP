# 🚀 Návod: GitHub krok za krokem

Tento návod tě provede vším od založení účtu až po web, který běží na internetu. Kroky 1–7 uděláš **jednou** na začátku. Pak už jen upravuješ soubory a ukládáš změny (viz [Každodenní práce](#-každodenní-práce)).

**Budeš potřebovat:**
- e-mail, ke kterému máš přístup
- **VS Code** (v něm píšeš kód a ukládáš verze)
- **Git Bash** (ve škole je nainstalovaný, doma si ho stáhneš z [git-scm.com](https://git-scm.com/))

---

## 1. Založ si účet na GitHubu

1. Jdi na [github.com/signup](https://github.com/signup).
2. Vyplň e-mail, heslo a **uživatelské jméno**.
   - Uživatelské jméno bude součástí adresy tvého webu (`jmeno.github.io`), tak ho vyber s rozmyslem.
   - Nemusí to být tvoje celé jméno. Bude veřejně vidět.
3. Potvrď e-mail kódem, který ti přijde.
4. GitHub tě může požádat o **dvoufázové ověření** (kód z aplikace v mobilu nebo SMS). Nastav ho a **ulož si záložní kódy**, jinak se při ztrátě mobilu nepřihlásíš.

> 💡 Doporučení: v **Settings → Emails** zaškrtni **Keep my email addresses private**. Kousek níž uvidíš adresu ve tvaru `12345678+jmeno@users.noreply.github.com`. Tu použiješ v dalším kroku.

---

## 2. Řekni Gitu, kdo jsi

Git u každé uložené verze zapisuje, kdo ji vytvořil. Musíš mu to jednou říct.

1. Otevři **Git Bash**.
2. Napiš tyto dva příkazy (každý potvrď Enterem), jen místo ukázky dej svoje údaje:
   ```bash
   git config --global user.name "Jan Novák"
   git config --global user.email "12345678+jmeno@users.noreply.github.com"
   ```
3. Kontrola:
   ```bash
   git config --global --list
   ```
   Měl bys vidět svoje jméno a e-mail.

> 🏠 Tohle musíš udělat na **každém počítači**, kde budeš pracovat (ve škole i doma).

---

## 3. Vytvoř repozitář ze šablony

Repozitář je složka s tvým projektem, kterou GitHub hlídá a pamatuje si všechny její verze. Nezačínáš s prázdným, ale se **šablonou od vyučujícího**. V ní už je zadání a checklisty, které si budeš odškrtávat.

1. Otevři šablonu: **_odkaz doplní vyučující_**
2. Klikni na zelené tlačítko **Use this template** → **Create a new repository**.
3. Vyplň:
   - **Repository name:** `muj-web` (bez diakritiky a mezer)
   - **Public** (musí být veřejný, jinak GitHub Pages nefungují zdarma)
4. Klikni na **Create repository**.

Teď máš vlastní kopii, ve které můžeš dělat, co chceš. Šablona vyučujícího zůstane beze změny.

---

## 4. Stáhni repozitář do počítače (clone)

1. Na stránce svého repozitáře klikni na zelené tlačítko **Code** a zkopíruj adresu (končí na `.git`).
2. Ve VS Code stiskni **Ctrl + Shift + P**, napiš `Git: Clone` a potvrď.
3. Vlož zkopírovanou adresu a potvrď Enterem.
4. Vyber, kam se má složka uložit (třeba Dokumenty). Zapamatuj si to.
5. VS Code se zeptá, jestli chceš repozitář otevřít. Klikni na **Open**.

Teď máš v počítači složku `muj-web`, propojenou s GitHubem.

<details>
<summary>Alternativa: přes Git Bash</summary>

```bash
cd ~/Documents
git clone https://github.com/tvoje-jmeno/muj-web.git
```
Pak ve VS Code otevři složku přes **File → Open Folder**.
</details>

---

## 5. Vytvoř první stránku

1. Ve VS Code vytvoř soubor `index.html` a napiš do něj základní strukturu stránky.
2. Ulož (**Ctrl + S**).

Struktura složky by měla vypadat zhruba takto:
```
muj-web/
├── index.html
├── o-nas.html
├── img/
│   └── logo.png
├── media/
│   └── trailer.mp4
├── README.md
└── 01-html-zaklad.md
```

---

## 6. Ulož změny a pošli je na GitHub (commit a push)

1. Ve VS Code klikni vlevo na ikonu **Source Control** (větvička) nebo stiskni **Ctrl + Shift + G**. Uvidíš seznam změněných souborů.
2. Do pole **Message** nahoře napiš, co jsi udělal, třeba `Přidána úvodní stránka`.
3. Klikni na **✓ Commit**.
   - Když se VS Code zeptá, jestli má uložit všechny změny (*stage all changes*), klikni na **Yes** (nebo **Always**).
4. Klikni na **Sync Changes** (nebo **Publish Branch**). Tím pošleš verzi na GitHub.
5. Napoprvé se otevře prohlížeč a GitHub tě požádá o **přihlášení**. Přihlas se a povol přístup.

> ❗ Dokud neklikneš na **Sync Changes**, změny jsou jen u tebe v počítači. Na GitHubu je nikdo neuvidí.

> ⚠️ **Na školním počítači:** po přihlášení si Windows tvůj GitHub účet zapamatuje. Pokud se k počítači dostane někdo jiný, mohl by posílat změny pod tvým jménem. Postup, jak se odhlásit, najdeš [níže](#-odhlášení-na-cizím-počítači).

---

## 7. Zapni GitHub Pages (web na internetu)

1. Na GitHubu otevři svůj repozitář `muj-web`.
2. Klikni na **Settings** → vlevo **Pages**.
3. V části **Build and deployment** nastav:
   - **Source:** Deploy from a branch
   - **Branch:** `main` a složka `/ (root)`
4. Klikni na **Save**.
5. Počkej 1–2 minuty a obnov stránku. Nahoře se objeví adresa tvého webu:
   ```
   https://tvoje-jmeno.github.io/muj-web/
   ```

Tuhle adresu i odkaz na repozitář **pošli vyučujícímu**.

> 💡 Po každém pushi se web na internetu aktualizuje sám, jen to trvá asi minutu.

---

## 🔁 Každodenní práce

Tohle budeš dělat pořád dokola:

1. **Než začneš:** v Source Control klikni na **⋯** → **Pull**. Stáhneš si nejnovější verzi z GitHubu.
2. Uprav soubory a ulož je (**Ctrl + S**).
3. Napiš zprávu → **✓ Commit**.
4. **Sync Changes**.

**Pracuješ ve škole i doma?** Krok 1 nevynechávej. Bez něj budeš pracovat se starou verzí a při odesílání ti Git ohlásí chybu.

<details>
<summary>Totéž v Git Bash</summary>

```bash
git pull
git add .
git commit -m "Přidána tabulka s menu"
git push
```
</details>

---

## 🏷️ Označení verze tagem (konec milníku)

Na konci milníku označíš poslední commit štítkem (`v1`, `v2`…). Nevzniká tím nový commit, jen se na ten existující „nalepí“ jméno.

1. Nejdřív se ujisti, že máš vše commitnuté a pushnuté.
2. Ve VS Code stiskni **Ctrl + Shift + P**, napiš `Git: Create Tag` a potvrď.
3. Napiš `v1`, potvrď. Popis (message) můžeš nechat prázdný.
4. Znovu **Ctrl + Shift + P**, napiš `Git: Push Tags` a potvrď.

Nebo v Git Bash (ve složce `muj-web`):
```bash
git tag v1
git push origin v1
```

Kontrola: na GitHubu v repozitáři klikni na **Tags**. Měl bys tam vidět `v1`.

---

## 🚪 Odhlášení na cizím počítači

Na školním nebo cizím počítači se po práci odhlas:

1. Ve Windows otevři **Správce pověření** (*Credential Manager*), najdeš ho přes Start.
2. Klikni na **Přihlašovací údaje systému Windows**.
3. Najdi položku `git:https://github.com` a klikni na **Odebrat**.
4. Ve VS Code klikni vlevo dole na ikonu účtu a odhlas se z GitHubu, pokud tam jsi přihlášený.

---

## 🆘 Něco nefunguje

| Problém | Řešení |
|---|---|
| Web hlásí **404** | Hlavní stránka se musí jmenovat přesně `index.html`. Po zapnutí Pages počkej pár minut. |
| Obrázek se zobrazí u mě, ale na webu ne | Zkontroluj velká a malá písmena v názvu (`Logo.PNG` ≠ `logo.png`) a že je obrázek commitnutý a pushnutý. |
| Změny nejsou na webu vidět | Dal jsi **Sync Changes**? Pak počkej minutu a obnov stránku (**Ctrl + F5**). |
| Při odesílání chyba *rejected* / *fetch first* | Nejdřív **Pull**, pak znovu **Sync Changes**. |
| Commit hlásí *Please tell me who you are* | Neudělal jsi [krok 2](#2-řekni-gitu-kdo-jsi) na tomto počítači. |
| Source Control ukazuje „no source control providers“ | Nemáš otevřenou složku `muj-web`. Otevři ji přes **File → Open Folder**. |
| Zapomněl jsem heslo | Na přihlašovací stránce GitHubu klikni na **Forgot password?** |

Pokud nic z toho nepomůže, ozvi se vyučujícímu.
