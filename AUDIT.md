# AUDIT — Merge FoundryTwo + Co-do-va-bu-di

> Fichier temporaire. À supprimer après traitement des corrections.
> Généré le 19 avril 2026 après fusion des deux repos.

---

## 1. Références obsolètes inter-repo

Occurrences de "repo FT", "repo CDV", "Co-do-va-bu-di", "repo compagnon", "tandem", etc. Le repo est désormais unifié — toutes ces références doivent être réécrites.

**34 occurrences détectées.** Liste complète :

| Fichier | Ligne | Extrait |
|---------|-------|---------|
| `distribution/README.md` | 1 | `# Co-do-va-bu-di — Repo distribution-first FoundryTwo` |
| `fabrice/context-from-FT.md` | 206 | `Distribution terrain Reddit = repo CDV. Sur FT, F mentionne Reddit…` |
| `marketing/context.md` | 45 | `…Distribution terrain Reddit/Facebook = repo CDV.` |
| `marketing/context.md` | 57 | `Ce repo gère le funnel Twitter/LinkedIn/IH/PH. Le funnel Reddit/Facebook est dans le repo CDV.` |
| `marketing/context.md` | 113 | `Gérés dans le repo CDV. Voir CDV/romain/ et CDV/fabrice/ pour les détails.` |
| `marketing/context.md` | 279 | `Co-do-va-bu-di (CDV) \| Source de vérité produits…` |
| `marketing/README.md` | 25 | `Co-do-va-bu-di (CDV) \| Repo compagnon…` |
| `context.md` | 12 | `Ce repo fonctionne en tandem avec le repo Co-do-va-bu-di (CDV)…` |
| `context.md` | 65 | `…via le repo CDV (Reddit, Facebook).` |
| `context.md` | 71 | `Sur Reddit/Facebook (repo CDV)…` |
| `context.md` | 191 | `…s'aligner avec le pivot du 03/04/2026 (repo CDV).` |
| `context.md` | 234 | `Co-do-va-bu-di (CDV) \| Repo compagnon…` |
| `la-toile/coordination.md` | 569 | `CDV \| Cadence De Vie — le repo compagnon…` |
| `growth-marketing/context.md` | 306 | `Reddit/Facebook = repo CDV.` |
| `growth-marketing/context.md` | 393 | `Reddit/Facebook : Distribution terrain via repo CDV (séparé)` |
| `growth-marketing/context.md` | 469 | `Co-do-va-bu-di (CDV) \| Repo compagnon…` |
| `growth-marketing/roadmap.md` | 181 | `…le repo FT/CDV, la distribution terrain.` |
| `growth-marketing/roadmap.md` | 243 | `Co-do-va-bu-di (CDV) \| Repo compagnon…` |
| `growth-marketing/README.md` | 5 | `La distribution terrain Reddit/Facebook est dans le repo CDV.` |
| `growth-marketing/README.md` | 177 | `Co-do-va-bu-di (CDV) \| Repo compagnon…` |
| `saas/context.md` | 7 | `…voir repo CDV/produits/).` |
| `saas/context.md` | 21 | `Distribution terrain Reddit/Facebook = repo CDV.` |
| `saas/roadmap.md` | 25 | `…Distribution terrain Reddit/Facebook = repo CDV.` |
| `saas/clientpulse/context.md` | 55 | `Source : CDV (repo compagnon)` |
| `saas/storemd/context.md` | 58 | `Source : CDV (repo compagnon)` |
| `saas/leadquiz/context.md` | 56 | `Source : CDV (repo compagnon)` |
| `saas/creatorsuite/context.md` | 57 | `Source : CDV (repo compagnon)` |
| `saas/adaudit/context.md` | 55 | `Source : CDV (repo compagnon)` |
| `saas/profitpilot/context.md` | 58 | `Source : CDV (repo compagnon)` |
| `romain/publication/claude/context.md` | 90 | `Reddit = repo CDV.` |
| `romain/semaine-2/jour-09-mar-14-04.md` | 18 | `Journée passée sur repo FT.` |
| `romain/context-from-FT.md` | 209 | `Distribution terrain Reddit = repo CDV.` |
| `README.md` | 18 | `Synthèse stratégique (héritée de l'ancien repo FT).` |
| `f2/publication/context.md` | 414 | `…voir le repo CDV (source de vérité produits).` |

**Cas particulier — acceptés (à conserver) :**
- `CLAUDE.md` §8 point 7 : cite explicitement "l'autre repo", "repo FT", "repo CDV" comme termes interdits. C'est légitime.
- `AUDIT.md` (ce fichier) : cite les termes pour le diagnostic.
- `README.md` ligne 18 : mentionne "ancien repo FT" dans une note contextuelle — reformuler ou laisser tel quel selon préférence.

### Références inline aux chemins (CDV/... ou FT/...)

**38 occurrences détectées** de patterns `CDV/produits/`, `CDV/romain/`, etc. Les plus critiques :

- `la-toile/context.md:356` — `CDV/` comme "Repo compagnon"
- `la-toile/README.md:74` — description du repo CDV/
- `la-toile/coordination.md:407` — `Voir CDV/produits/ pour les specs des 6 SaaS.`
- `saas/{clientpulse,storemd,leadquiz,creatorsuite}/context.md:7` — `Specs détaillées : Voir CDV/produits/{NOUVEAUX,MUTATIONS}.md`
- `saas/{clientpulse,storemd,leadquiz,creatorsuite}/README.md:6` — `Specs détaillées : CDV/produits/`
- `saas/context.md:65, 117, 135` — références CDV/produits/
- `saas/roadmap.md:5` — `CDV/produits/STATUS.md` (source de vérité)
- `marketing/context.md:47, 113` — références CDV/produits/, CDV/romain/, CDV/fabrice/

**Action recommandée :** remplacer toutes les occurrences `CDV/` par le chemin direct dans le repo unifié (`produits/`, `romain/`, `fabrice/`, etc.).

---

## 2. Liens markdown cassés

**Aucun lien `[texte](chemin)` détecté dans les fichiers .md du repo.** Les références aux autres fichiers se font par chaînes en backticks (`` `strategie/CONTEXT.md` ``) ou en texte brut. Rien à corriger sur ce front.

---

## 3. Duplications potentielles

### 3.1 Fichiers temporaires à fusionner (HIGH PRIORITY)

| Fichier | Statut |
|---------|--------|
| `romain/context-from-FT.md` | Context FT non fusionné. Doit être consolidé avec `romain/VOIX.md` + `romain/plan-30-jours.md` en un `romain/context.md` unifié. |
| `fabrice/context-from-FT.md` | Idem pour F. |
| `romain/CLAUDE-from-CDV.md` | Copie du CLAUDE.md CDV racine. Probablement redondant avec le CLAUDE.md unifié racine — à supprimer après vérification. |
| `fabrice/CLAUDE-from-CDV.md` | Idem pour F. |

### 3.2 Filenames partagés — pas de contradiction

| Fichier | Occurrences | Note |
|---------|-------------|------|
| `context.md` | 40 | Normal — un par dossier. Héritage strict applique. |
| `roadmap.md` | 16 | Normal — un par scope. |
| `README.md` | 12 | Normal. |
| `plan-hebdo.md`, `progress-semaine.md` | 12 + 10 | Copiés dans archives/ par semaine. Normal. |
| `VOIX.md` | 2 (romain, fabrice) | OK. |
| `CLAUDE.md` | 1 (racine) | OK. |

### 3.3 Distribution/README.md commence par "# Co-do-va-bu-di"

Le fichier `distribution/README.md` est simplement le README original de CDV. Son titre et son contenu font référence au repo CDV comme entité propre. À réécrire entièrement comme README du dossier `distribution/` dans le repo unifié.

---

## 4. Fichiers orphelins

Non traité automatiquement (détection manuelle nécessaire). Pointeurs de détection possible : fichiers non référencés depuis CLAUDE.md, README.md, context.md, ARCH.md. À auditer avec un outil dédié si souhaité.

Candidats visibles à vérifier :
- `growth-marketing/strategie/strategie-expansion-generale.md` — probablement orphelin du repo, pas référencé dans README.md racine.
- `la-toile/LA-TOILE-v3.1-Complete.docx` — fichier binaire, non documenté dans CLAUDE.md/README.md.
- `la-toile/toile-schema-v3.1.png` — image, non liée dans les .md.

---

## 5. Dossiers vides

| Dossier | État | Intentionnel ? |
|---------|------|----------------|
| `archives/` | vide | ✅ Oui — se remplira à chaque archivage dimanche. |
| `romain/ph/` | vide | ✅ Oui — canal PH à documenter (prévu). |
| `fabrice/ph/` | vide | ✅ Oui — idem. |

Aucun autre dossier vide détecté.

---

## 6. Contradictions de règles

### 6.1 Volume interactions pour F (critique)

Deux chiffres coexistent :
- **CDV/CLAUDE.md (pivot) :** `F : 15 interactions/jour`
- **FT (post-pivot) :** `F : 30 interactions/jour (15 Twitter + 15 LinkedIn)` — dans `fabrice/twitter/context.md:168`, `fabrice/roadmap.md:36, 57, 76, 91, 123`, `fabrice/playbook-semaine.md:8, 151`, `fabrice/engagement/grok/context.md:102`, `fabrice/engagement/claude/context.md:34-38`, `fabrice/linkedin/context.md:285`, `fabrice/archives/semaine-4-…/plan-hebdo.md:63`, `fabrice/daily-checklist.md:54`, `fabrice/plan-hebdo.md:58`.

**CLAUDE.md unifié (nouveau) suit CDV : F = 15/jour.** Les 13+ références à "F : 30 interactions/jour" dans fabrice/ contredisent directement la règle #3. Action : trancher (F = 15 ou 30 ?) puis corriger en masse.

### 6.2 Cadence SaaS (contradictions multiples)

- `CLAUDE.md` unifié + `tracking/decisions-log.md:7` + prompt de fusion → **3–4 SaaS/mois**.
- `context.md:24` + `marketing/context.md:45, 303` + `growth-marketing/roadmap.md:7` + `fabrice/roadmap.md:6` + `fabrice/system-prompt.md:330` + `fabrice/context-from-FT.md:246` + `saas/roadmap.md` (implicite) + `la-toile/*` → **3 SaaS/mois par vertical** (soit jusqu'à 9/mois).
- `la-toile/roadmap.md:24` → **2 SaaS par mois par vertical**.
- `saas/context.md:13` → **2 SaaS/mois** (pas par vertical).

**4 valeurs différentes.** Trancher puis corriger partout.

### 6.3 Référence "ce repo" ambiguë

De multiples fichiers (`context.md`, `marketing/context.md`, `growth-marketing/*`, `saas/*`, `f2/publication/context.md`) parlent encore de "ce repo" comme si FT et CDV étaient deux repos. Avec la fusion, "ce repo" = le repo unifié. À reformuler systématiquement.

---

## 7. Décisions à valider (emplacements incertains)

| Fichier | Emplacement choisi | À valider |
|---------|-------------------|-----------|
| `context.md` (racine) | Racine | Source héritée de FT. Fusionner avec `strategie/CONTEXT.md` ou garder les deux ? |
| `romain/context-from-FT.md` / `fabrice/context-from-FT.md` | `romain/` / `fabrice/` | À fusionner en `context.md` unique ou à supprimer (redondant avec VOIX.md + plan-30-jours.md) ? |
| `romain/CLAUDE-from-CDV.md` / `fabrice/CLAUDE-from-CDV.md` | `romain/` / `fabrice/` | Supprimer — le CLAUDE.md racine suffit. |
| `growth-marketing/strategie/` | Conservé | À fusionner avec `strategie/` racine ? Ou garder les deux scopes séparés ? |
| `distribution/README.md` | `distribution/` | Réécrire complètement — actuellement c'est le README original de CDV. |
| Fichiers `saas/*/context.md` mentionnant "Source : CDV" | Conservés | Réécrire pour pointer vers `produits/` (même repo). |

---

## Recommandations d'ordre

1. **Supprimer** `romain/CLAUDE-from-CDV.md` et `fabrice/CLAUDE-from-CDV.md` (redondants avec CLAUDE.md racine).
2. **Trancher** sur le volume F (15 ou 30 int./jour) et sur la cadence SaaS (2, 3, 3–4 ?) — une seule valeur autorisée.
3. **Réécrire** `distribution/README.md` (actuellement c'est le README de l'ex-repo CDV).
4. **Corriger en batch** les 34 références "repo CDV / repo FT / repo compagnon" + les 38 chemins `CDV/...`.
5. **Fusionner ou supprimer** les deux `context-from-FT.md` dans `romain/` et `fabrice/`.
6. **Reformuler** les "ce repo" ambigus pour refléter l'unification.
