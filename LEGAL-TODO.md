# LEGAL-TODO — GïDA, kebab artisanal & locavore

> **Ne pas mettre en ligne avant d'avoir traité la section 1.**
> État au 17 juillet 2026. Aucune donnée n'a été inventée : tout ce qui n'a pas pu être
> vérifié à une source est marqué `[à fournir]` ou `[à confirmer]` et apparaît **en
> surbrillance rose sur le site lui-même**, exprès — pour qu'un trou se voie au lieu de se
> combler avec une supposition.
>
> Les deux pages légales existaient déjà, sous forme de **gabarit générique à crochets**
> (`[NOM DE L'ENTREPRISE]`, `[SIRET / NEQ / NUMÉRO D'ENTREPRISE]`, `[FONCTION]`…). Elles ont
> été **remplacées** par les données réelles du registre. Le gabarit contenait aussi deux
> affirmations inventées — voir § 1.3.

---

## 1. Bloquant avant la mise en ligne

### 1.1 L'éditeur du site n'est pas confirmé — le point le plus important

**« GïDA » n'apparaît nulle part au registre national des entreprises : aucune enseigne, aucun
nom commercial, aucune dénomination.**

La société **LES ARROSES** (SARL, SIREN 900 619 917) a été identifiée **uniquement parce
qu'elle exploite un établissement de restauration (APE 56.10A, actif) à l'adresse du
restaurant** : 27 rue La Tour d'Auvergne, 44200 Nantes — SIRET 900 619 917 00033.

**Ce rattachement est un faisceau, pas une preuve.** Il n'a pas été tranché ici, et il ne doit
pas l'être par le prestataire : **désigner le mauvais éditeur dans des mentions légales est la
faute à éviter**. La question à poser à l'exploitant, en une phrase :

> **« Est-ce bien la SARL LES ARROSES qui exploite GïDA et qui édite ce site ? Si non,
> laquelle ? »**

Tant que la réponse n'est pas écrite, le bloc `[à confirmer]` reste affiché sur
`mentions-legales.html` (encadré rose en tête de la section Éditeur) et sur
`politique-confidentialite.html` (responsable du traitement).

### 1.2 Identité de l'éditeur (`mentions-legales.html`)

| Donnée | État |
|---|---|
| Rattachement LES ARROSES → GïDA | **à confirmer** — voir § 1.1 |
| Capital social | **manquant** — obligatoire pour une SARL, ne figure dans aucun registre public |
| RCS | **à confirmer** — « RCS Nantes 900 619 917 » est la forme attendue, non vérifiée à une source |
| Directeur de la publication | **manquant** — la société a **quatre gérants** (Olivier Adriaens, Charlie Coignard, Samy Mokhtari, Benjamin Vives-Bauquin) : **lequel des quatre** assume la fonction ? |
| E-mail | **manquant** — apparaît dans les mentions légales, la confidentialité et le bloc accessibilité |
| Enseigne « GïDA » | **non déclarée** — à déclarer au registre, ou à assumer comme simple nom commercial |

Le téléphone (**09 81 99 31 60**) est repris du site existant : il est déjà renseigné partout.

### 1.3 Deux affirmations inventées ont été retirées du gabarit

Le gabarit précédent affirmait, sans source :

1. **« Hébergeur : Vercel Inc. — 440 N Barranca Avenue #4133, Covina, CA 91723, États-Unis
   *(adresse à vérifier)* »** dans les mentions légales. Une adresse d'hébergeur explicitement
   non vérifiée n'a rien à faire dans une mention obligatoire (art. 6 III-1 LCEN) : elle a été
   remplacée par `[à fournir]`.
2. **« Seul l'éditeur du site et son hébergeur (Vercel Inc.) ont accès à ces données »** dans
   la politique de confidentialité — nommer un sous-traitant non confirmé est une information
   fausse. Remplacé par `[à fournir]`.

> **Indice, pas preuve :** le dossier contient un `.vercel/project.json` (projet
> `gida-nantes`), ce qui rend Vercel **probable**. Cela ne suffit pas : il faut arrêter
> l'hébergeur définitif, puis recopier **son** identité légale depuis **ses propres** mentions
> légales — nom social exact, adresse, téléphone —, pas depuis une supposition.

### 1.4 Hébergeur (article 6 III-1 LCEN — obligatoire)

Nom, adresse, téléphone et site de l'hébergeur : **les quatre champs sont vides** dans
`mentions-legales.html`, et la durée de conservation des journaux de connexion est vide dans
`politique-confidentialite.html`. Une fois l'hébergeur retenu, vérifier s'il implique un
**transfert hors UE** (section correspondante de `politique-confidentialite.html`) — si c'est
Vercel, la réponse est oui, et elle doit être documentée.

### 1.5 Les photographies : deux problèmes en un

Les **trois photographies** de la page d'accueil sont **chargées à chaud (hotlink) depuis
`bigcitynantes.fr`** — le site d'un média local qui a publié un article sur le restaurant en
octobre 2022 :

```
https://www.bigcitynantes.fr/wp-content/uploads/2022/10/Capture-decran-2022-10-26-a-11.07.03-1044x730.jpg
https://www.bigcitynantes.fr/wp-content/uploads/2022/10/295979992_119631387475523_7321895423250336985_n-edited-1.jpg
https://www.bigcitynantes.fr/wp-content/uploads/2022/10/Capture-decran-2022-10-26-a-10.58.33-1-1160x973.jpg
```

**a) Droit d'auteur — bloquant.** Ces images ne sont ni la propriété du site, ni créditées, ni
accompagnées d'une autorisation. Les afficher revient à publier l'œuvre d'un tiers sans droits
documentés, et à faire supporter la bande passante à ce tiers. **Il faut fournir des
photographies dont la maison détient les droits**, ou obtenir de Big City Nantes (et de
l'auteur des clichés) une autorisation écrite, puis créditer.

**b) Vie privée — à corriger avec (a).** Tant que ces images restent hotlinkées, **chaque
visite de la page d'accueil transmet l'adresse IP du visiteur à un serveur tiers**. Vérifié le
17 juillet 2026 : ce serveur répond `HTTP 200`, `content-type: image/jpeg`, `server:
o2switch-PowerBoost-v3`, et **ne pose aucun cookie** — il n'y a donc rien à consentir au sens
de l'art. 82 LIL, et pas de bannière à poser. Mais la requête tierce existe : elle est
**déclarée honnêtement** dans `politique-confidentialite.html` plutôt que niée.

> Une fois les photos hébergées dans `assets/`, l'encadré correspondant de la politique de
> confidentialité doit être retiré, et le site n'aura **plus aucune requête tierce**.

### 1.6 Les 50 avis clients sont fictifs — bloquant

`index.html` contient un tableau JavaScript `AVIS` de **50 avis inventés** (noms, notes,
dates, textes), affichés par le bouton « Voir plus d'avis ». La page le dit elle-même :
« *Avis d'illustration pour la maquette — à remplacer par les vrais avis Google du
restaurant.* »

**Publier des avis fabriqués est une pratique commerciale trompeuse** (art. L121-2 et L121-4
du code de la consommation, qui vise expressément le fait de diffuser de faux avis de
consommateurs). C'est un risque de sanction, et il porte sur le client, pas sur le
prestataire. Avant mise en ligne, **au choix** :

1. remplacer par de vrais avis Google (avec leur source et leur date réelles) ;
2. supprimer le bloc et le bouton ;
3. ne garder que le lien vers la fiche Google du restaurant.

La mention « **4,6 · 210+ avis Google** » (hero + bandeau) et la citation de presse attribuée
à **Big City Nantes** doivent également être vérifiées et datées : une note qui bouge doit
être ou bien exacte au jour de la publication, ou bien renvoyée à sa source.

> Le contenu éditorial n'a **pas** été modifié : c'est un arbitrage du client, pas du
> prestataire. Il est signalé, pas corrigé.

### 1.7 Les allégations « locavore » doivent être justifiables

Le site affirme, en clair et à plusieurs endroits :

| Affirmation | Où |
|---|---|
| « produits **100 % régionaux** » | `<meta name="description">` |
| « Le kebab qui **pousse ici**, se mange ici » | hero |
| « **circuit court, vraiment** » · « Chaque ingrédient a une adresse » | section provenance |
| « Pain pide : **Rezé, 4 km** », cuit par une boulangerie turque de Rezé | section provenance |
| « Poulet **élevé en Loire-Atlantique** » | section provenance |
| « Bières, vins, glaces : **brasseurs, vignerons et glaciers du coin** » | section provenance |
| stickers « **100 % fait maison** » · « **produits d'ici** » | hero |
| « **écolo** » | chapô |

Ce sont des **allégations d'origine et de circuit court**. Elles relèvent de l'article
**L121-2 du code de la consommation** (pratiques commerciales trompeuses) : une allégation de
ce type doit être **exacte et justifiable sur demande**, notamment de la DGCCRF. En
particulier :

- « **100 % régionaux** » est un absolu : il tombe dès qu'**un seul** ingrédient courant
  (huile, épices, boisson industrielle, cheddar, sauces achetées…) ne l'est pas ;
- « **fait maison** » a une **définition réglementaire** (art. D121-13-1 code de la
  consommation) : plat cuisiné sur place à partir de produits bruts ;
- « **halal** » (mentionné sur la carte) suppose une **certification** vérifiable ;
- « **écolo** » est une allégation environnementale générale, à éviter ou à étayer.

**Action côté client :** confirmer chaque allégation, ou faire adoucir la formulation
(« majoritairement régional », « au maximum de saison »…). **Le contenu éditorial n'a pas été
modifié** — c'est une décision de la maison.

### 1.8 Vérifier avant publication

```bash
grep -rn "à fournir\|à confirmer" *.html    # ne doit plus rien renvoyer
```

---

## 2. Ce qui a été vérifié (et n'est donc pas à redemander)

Relevé le **17 juillet 2026** au registre national des entreprises via l'API publique
`recherche-entreprises.api.gouv.fr` :

- Dénomination : **LES ARROSES** — *aucun sigle, aucune enseigne déclarée*
- Forme : **SARL** (code INSEE 5499 — société à responsabilité limitée)
- Siège social : **5 rue Emmanuel Lebert, 44400 Rezé**
- SIREN : **900 619 917** · SIRET siège : **900 619 917 00017**
- TVA : **FR35900619917**
- APE : **56.10A — Restauration traditionnelle**
- Immatriculation : **18 juin 2021**
- Gérants (**quatre**) : **Olivier Adriaens**, **Charlie Coignard**, **Samy Mokhtari**,
  **Benjamin Vives-Bauquin**
- État administratif : **actif**
- Greffe probable : **Nantes**

### Le siège n'est pas le restaurant

C'est le piège de ce dossier, et il est traité explicitement sur la page :

| | Adresse |
|---|---|
| **Siège social** (l'éditeur, la personne morale) | 5 rue Emmanuel Lebert, **44400 Rezé** |
| **Établissement** (le restaurant, le lieu) | 27 rue La Tour d'Auvergne, **44200 Nantes** — SIRET 900 619 917 00033, **actif** |

**Ne jamais écrire que le siège est le restaurant.** Les deux adresses figurent côte à côte
dans la fiche d'identité, et un paragraphe dédié (« Le siège n'est pas le restaurant »)
explique la différence au lecteur.

> **Variante d'écriture à noter :** le registre écrit « 27 rue **La** Tour d'Auvergne », le
> site du client écrit « 27 rue **de la** Tour d'Auvergne ». Les pages reprennent la forme du
> client (c'est celle de l'usage et de la voie nantaise). Sans conséquence juridique, signalé
> pour mémoire.

### Établissement fermé — à ne pas citer

Un établissement antérieur, au **48 bd de la Prairie au Duc**, est **fermé**. Il n'est
mentionné nulle part sur le site, et ne doit pas l'être : seule l'adresse du 27 rue de la Tour
d'Auvergne est active.

---

## 3. Pages légales : ce qui a été créé, et ce qui ne l'a pas été

### Refaites (noms de fichiers existants conservés)

| Page | Pourquoi |
|---|---|
| `mentions-legales.html` | Obligatoire (art. 6 III LCEN) pour tout site édité par une société. Le gabarit à crochets a été remplacé par les données du registre. |
| `politique-confidentialite.html` | Transparence RGPD sur les journaux de l'hébergeur, les liens sortants et les images tierces. Contient la section cookies (ancre **`#cookies`**, ajoutée). |

> Le nom de fichier `politique-confidentialite.html` est celui du site (et non
> `confidentialite.html` comme sur d'autres projets) : il a été **conservé** pour ne casser
> aucun lien existant.

### Volontairement non créées

| Page | Pourquoi pas |
|---|---|
| **CGV** | Ce site ne vend rien et n'encaisse rien : les commandes se font par téléphone, sur place, ou sur les plateformes de livraison (Uber Eats, Naofood) qui encaissent sur leurs propres services. Une CGV serait un document sans objet. **Si la maison encaisse en réalité depuis ce site, ou possède déjà des CGV ailleurs, le signaler : la conclusion change.** |
| **CGU** | Aucun compte, aucun contenu déposé par l'utilisateur, aucun service interactif. Sans objet. |
| **Droit de rétractation** | Pas de vente à distance depuis ce site. |
| **Bannière de consentement cookies** | Voir § 4 : aucun cookie déposé, rien à consentir. |
| **`sitemap.xml`** | **Aucun domaine n'est déclaré nulle part** dans le projet : ni `<link rel="canonical">`, ni `sitemap.xml`, ni `robots.txt`, ni URL absolue dans les pages. Un sitemap exige des URL absolues — l'inventer aurait été inventer le domaine. **À créer une fois le domaine arrêté**, avec les deux pages légales en `priority` 0.2 et `lastmod` 2026-07-17. |

### Médiation de la consommation — à trancher avec le comptable

Tout professionnel vendant à des consommateurs doit relever d'un médiateur de la consommation
(art. L612-1 du code de la consommation). L'obligation vise **l'activité du restaurant**, pas
ce site vitrine — c'est pourquoi aucune section n'a été ajoutée. Si un médiateur est déjà
désigné, ses coordonnées ont vocation à figurer dans les mentions légales.

### Licence de débit de boissons

Le site annonce des **bières et des vins** (« Bières, vins, glaces — brasseurs, vignerons et
glaciers du coin »), ce qui a justifié l'ajout de la section **« Vente d'alcool »**
(art. L3342-1 code de la santé publique + modération) dans `mentions-legales.html`. La
**licence de débit de boissons** correspondante et l'affichage obligatoire de la protection des
mineurs relèvent de l'établissement : à vérifier côté maison, non traité ici.

---

## 4. Cookies, traceurs, données

### Ce que le site fait réellement — vérifié le 17 juillet 2026

| | |
|---|---|
| Cookies déposés | **aucun** |
| Stockage local | **aucun** — aucun `localStorage`, aucun `sessionStorage` dans le code |
| Mesure d'audience | **aucune** — ni Google Analytics, ni Matomo, ni pixel |
| Formulaires | **aucun** |
| Comptes utilisateurs | **aucun** |
| Newsletter | **aucune** |
| Paiement | **aucun** |
| Iframes / widgets | **aucun** — Google Maps est un **lien sortant**, pas une carte intégrée |
| Google Fonts | **supprimé le 17 juillet 2026** — voir ci-dessous |
| Requêtes vers des tiers | **⚠ trois** — les photos hotlinkées depuis `bigcitynantes.fr`, voir § 1.5 |

**Le seul point noir est celui des images.** Il n'est pas passé sous silence : il est écrit sur
la page de confidentialité, dans un encadré, avec ce qu'il implique (IP transmise) et ce qui a
été mesuré (aucun cookie en retour).

### Pourquoi il n'y a pas de bannière

L'article 82 de la loi Informatique et Libertés impose le consentement **avant tout dépôt de
cookie non strictement nécessaire**. Aucun cookie n'étant déposé — y compris par le serveur
tiers des images, vérifié — il n'y a rien à consentir. Une bannière serait une gêne sans objet.
C'est un choix argumenté, pas un oubli.

**Ce qui déclencherait l'obligation d'en poser une :**

- ajouter Google Analytics, Matomo (en mode non exempté), un pixel Meta ou tout traceur ;
- **intégrer une carte Google Maps en `<iframe>`** (aujourd'hui l'itinéraire est un simple lien
  sortant, exprès) ;
- intégrer un module de commande Uber Eats / Naofood dans les pages (aujourd'hui ce sont de
  simples mentions) ;
- intégrer une vidéo, un widget Instagram ou Facebook ;
- **recharger les polices depuis Google Fonts** — voir ci-dessous.

### Polices — ce qui a changé le 17 juillet 2026

Les trois pages chargeaient **Bricolage Grotesque, Caveat et Marcellus depuis
`fonts.googleapis.com` et `fonts.gstatic.com`** (avec `preconnect`). Chaque visite transmettait
donc l'adresse IP du visiteur à Google, sans consentement — le point précis sur lequel la CNIL
et plusieurs autorités européennes ont sanctionné des éditeurs.

Les trois familles sont désormais **auto-hébergées** dans `assets/font/` :

| Famille | Fichiers | Type | Poids |
|---|---|---|---|
| Bricolage Grotesque | latin + latin-ext | **variable** — `wght` 200–800, `opsz` 12–96 | 107 Ko |
| Caveat | latin + latin-ext | statique, weight 600 | 71 Ko |
| Marcellus | latin + latin-ext | statique, weight 400 | 23 Ko |

Total **~208 Ko**, 6 fichiers, licence **SIL Open Font License 1.1** (citée dans les mentions
légales). Les `<link>` Google et les `preconnect` ont été retirés des **trois** pages, les
`@font-face` ajoutés en tête de chaque `<style>` (le site n'a pas de CSS externe), et deux
`preload` ajoutés par page.

**Test de non-régression :**

```bash
grep -rn 'googleapis\|gstatic' . --include='*.html' --include='*.css'   # doit être vide
```

---

## 5. À vérifier après la mise en ligne

- [ ] **Confirmer que LES ARROSES est bien l'éditeur** (§ 1.1) — avant tout le reste
- [ ] `grep -rn "à fournir\|à confirmer" *.html` ne renvoie plus rien
- [ ] Les photos sont hébergées par le site, avec leurs droits réglés et leur crédit (§ 1.5)
- [ ] Les 50 avis fictifs sont remplacés ou retirés (§ 1.6)
- [ ] La note « 4,6 · 210+ avis Google » correspond à la fiche Google du jour
- [ ] Les allégations locavore sont confirmées par la maison (§ 1.7)
- [ ] `robots.txt` et `sitemap.xml` créés, pointant le vrai domaine (§ 3)
- [ ] Le `<meta name="robots" content="noindex">` des pages légales passe à `index, follow`
      une fois le domaine public arrêté (il est conservé tant que le site est une maquette)
- [ ] Le site est déclaré dans Google Search Console
- [ ] La fiche Google Business est cohérente avec les horaires du site
- [ ] Aucune requête tierce dans l'onglet Réseau
- [ ] `document.cookie` est vide
