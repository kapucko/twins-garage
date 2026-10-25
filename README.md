# Twins garage – web (Jekyll, SK/EN)

Markup je len raz v `_layouts/default.html`. Jazyky sa líšia iba textami.

```
_config.yml           údaje firmy (telefón, e-mail, IČO…) – spoločné pre oba jazyky
_data/sk.yml          slovenské texty
_data/en.yml          anglické texty (rovnaká štruktúra ako sk.yml)
_layouts/default.html celá stránka (HTML šablóna)
_includes/icon.html   ikony výhod
index.html            SK stránka  -> /      (len front matter lang: sk)
en/index.html         EN stránka  -> /en/   (len front matter lang: en)
assets/               CSS, JS, obrázky
```

- **Dizajn / štruktúra** → `_layouts/default.html` a `assets/css/style.css`
- **Texty** → `_data/sk.yml` a `_data/en.yml`
- **Kontakt, IČO** → `_config.yml`
- Nová služba / výhoda / štatistika = nová položka v zozname v oboch `.yml`

## Lokálne spustenie

Potrebuješ Ruby 3.x (na macOS `brew install ruby`, systémové Ruby je staré):

```
bundle install
bundle exec jekyll serve
```
a otvor http://localhost:4000

## Nasadenie

- **GitHub Pages:** pushni repo, Settings → Pages → Deploy from branch. Jekyll zostaví web sám.
- **Iný hosting:** `bundle exec jekyll build` a nahraj obsah priečinka `_site/`.
- Ak web pobeží v podpriečinku, nastav `baseurl` v `_config.yml`.

## Treba doplniť

- telefón a e-mail v `_config.yml`
- otváracie hodiny v `_data/*.yml`
- sekcia „O nás“ a štatistiky (2023, „1 deň“, „15 min“) – overiť
- zoznam služieb podľa reality
- fotka dielne `assets/img/hero.jpg` (návod je v komentári v layoute)
- logo `assets/img/logo.svg` je zástupné
