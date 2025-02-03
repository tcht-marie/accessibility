### Installation de Pa11y

- npm install -g pa11y

### Lancement de Pa11y

- pa11y http://localhost:3000

### Résultats

```
Welcome to Pa11y

> Running Pa11y on URL http://localhost:3000

Results for URL: http://localhost:3000/

• Error: The html element should have a lang or xml:lang attribute which describes the language of the document.
├── WCAG2AA.Principle3.Guideline3_1.3_1_1.H57.2
├── html
└── <html><head> <title>Site de démo<...</html>

• Error: Img element missing an alt attribute. Use the alt attribute to specify a short text alternative.
├── WCAG2AA.Principle1.Guideline1_1.1_1_1.H37
├── html > body > div:nth-child(1) > img
└── <img src="https://picsum.photos/200">

• Error: This textinput element does not have a name available to an accessibility API. Valid names are: label element, title undefined, aria-label undefined, aria-labelledby undefined.
├── WCAG2AA.Principle4.Guideline4_1.4_1_2.H91.InputText.Name
├── #main > form > input:nth-child(1)
└── <input type="text" name="email">

• Error: This form field should be labelled in some way. Use the label element (either with a "for" attribute or wrapped around the form field), or "title", "aria-label" or "aria-labelledby" attributes as appropriate.
├── WCAG2AA.Principle1.Guideline1_3.1_3_1.F68
├── #main > form > input:nth-child(1)
└── <input type="text" name="email">

• Error: This element has insufficient contrast at this conformance level. Expected a contrast ratio of at least 3:1, but text in this element has a contrast ratio of 2.32:1. Recommendation:  change text colour to #949494.
├── WCAG2AA.Principle1.Guideline1_4.1_4_3.G145.Fail
├── #contact > h3
└── <h3>Nous contacter</h3>

• Error: This element has insufficient contrast at this conformance level. Expected a contrast ratio of at least 4.5:1, but text in this element has a contrast ratio of 2.32:1. Recommendation:  change text colour to #767676.
├── WCAG2AA.Principle1.Guideline1_4.1_4_3.G18.Fail
├── #contact > p
└── <p>Tel: 01 23 45 67 89</p>

6 Errors
```

## Les erreurs d'accessibilités

#### Dans le fichier index.html

- manque le "lang="fr-FR"" dans la balise html
- le chemin du fichier css n'est pas bon = "./style.css"
- manque le alt sur img = alt vide pour une image décorative // s'il y a du texte sur l'image, recopier le texte dans le alt
- manque le label pour l'input email
- mauvais contraste sur le H3 et le #contact
- mauvaise sémantique sur le H3 (puisque aucun H2 n'existe avant)!


- [Text accessibilité avec lighthouse](..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fpd%2Fwrwn0_6951581sxyvmvnbqdr0000gp%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_EXSsCd%2FCapture%20d%E2%80%99%C3%A9cran%202025-02-03%20%C3%A0%2010.29.08.png)