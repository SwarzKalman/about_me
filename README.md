# Mobilra optimalizált kapcsolat oldal

Ez a repository egy letisztult, **GitHub Pages kompatibilis** statikus weboldalt tartalmaz, amely kifejezetten kapcsolatfelvételre készült.

## Többnyelvűség

Az oldal beépített nyelvváltót tartalmaz:

- magyar (HU)
- angol (EN)
- francia (FR)

A nyelvválasztás kliensoldali JavaScriptből történik, külön build lépés nélkül, ezért GitHub Pages-en közvetlenül működik.

## Fájlok

- `index.html` – oldal tartalma
- `styles.css` – mobil-first stílusok

## Testreszabás

Szerkeszd az `index.html` fájlban az alábbi adatokat:

- e-mail cím (`mailto:` link + megjelenített szöveg)
- telefonszám (`tel:` link + megjelenített szöveg)
- közösségi profil linkek (LinkedIn, GitHub, Telegram)
- név / brand a címben és a láblécben

## GitHub Pages deploy

1. Pushold a repositoryt GitHubra.
2. A GitHubon menj a **Settings → Pages** menüpontra.
3. Source-nál válaszd:
   - **Deploy from a branch**
   - Branch: `main` (vagy amelyiket használod)
   - Folder: `/ (root)`
4. Mentsd el, majd várj 1-2 percet.
5. Az oldal elérhető lesz itt:
   - `https://<felhasznalonev>.github.io/<repository-nev>/`

## Saját domain (DNS) beállítás

Ha saját domaint szeretnél:

1. Hozz létre egy `CNAME` fájlt a repository gyökerében, tartalma legyen a domained, pl.:

   ```
   kapcsolat.pelda.hu
   ```

2. GitHubon a **Settings → Pages** alatt add meg a **Custom domain** mezőben ugyanezt.

3. A DNS szolgáltatónál állítsd be:
   - aldomainhez: `CNAME` rekord → `<felhasznalonev>.github.io`
   - fődomainhez (apex): `A` rekordok GitHub Pages IP-kre (GitHub dokumentáció szerint)

4. Kapcsold be a **Enforce HTTPS** opciót, amint elérhető.

## Tipp

A jelenlegi megoldás statikus, gyors és minimális karbantartást igényel, ezért ideális személyes contact landing oldalnak.
