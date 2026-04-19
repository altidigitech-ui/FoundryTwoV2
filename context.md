# CONTEXT — Repo Growth Marketing FoundryTwo

**Dernière mise à jour :** 04 avril 2026
**Ce fichier est :** la source de vérité du repo. Il synthétise l'architecture, les principes, les rôles, et les décisions stratégiques. Tout fichier du repo hérite de celui-ci.

---

## 1. CE QU'EST CE REPO

Ce repo est la **documentation opérationnelle de growth marketing** de FoundryTwo. Il contient tout ce qu'il faut pour exécuter la stratégie marketing du studio au quotidien : qui publie quoi, où, quand, comment, avec quels outils, dans quelle voix, sur quelles plateformes, avec quel contenu, et comment tout se coordonne.

Ce repo fonctionne en tandem avec le repo **Co-do-va-bu-di (CDV)** qui gère la distribution terrain (Reddit, Facebook) et les spécifications produits. FT gère le brand building sur Twitter, LinkedIn, IndieHackers et Product Hunt.

**CDV est la source de vérité pour les produits** (features, pricing, concurrents, données marché). FT référence CDV pour les détails produits, ne les duplique jamais.

Ce repo n'est PAS le repo produit (code, architecture, déploiement) — chaque SaaS a son propre repo technique. Ce repo couvre le marketing, la communication, la construction de communauté, et l'exécution opérationnelle associée.

---

## 2. QUI ON EST

### Le studio

**FoundryTwo** est un studio SaaS créé par deux builders autodidactes basés à Marseille, France. Le studio construit et lance des outils SaaS propulsés par l'IA à une cadence cible de 3 SaaS par mois organisés par vertical (e-commerce, agences/freelancers, content creators). Tout est construit en public — les vrais chiffres, les vrais échecs, le vrai parcours.

### Les fondateurs

| | Romain (R) | Fabrice (F) |
|---|---|---|
| **Rôle** | Co-fondateur Growth/CRO | Co-fondateur CTO/Builder |
| **Twitter** | @delgado_ro72224 | @FabGangi |
| **Angle** | Growth, conversion, acquisition pour e-com et agences | Technique, automatisation, workflow pour e-com et creators |
| **Voix** | Provocateur, direct, data-driven, humour sec | Technique, concret, passionné, honnête sur les galères |
| **Temps** | 7-10h/jour full-time. 30 interactions/jour minimum. 1 post/jour (7/sem). | 7-10h/jour full-time. 30 interactions/jour minimum. 1 post/jour (5/sem). |
| **Pronom** | "I" (jamais "we" sauf référence F2) | "I" (jamais "we" sauf référence F2) |

### Le compte studio

**@foundrytwo** — Le hub central. Publie le contenu studio (build in public, data, milestones). Reçoit le cross-engagement de R et F. Ne fait JAMAIS de cold outreach ni d'engagement proactif. Géré par R. Voix : "we", neutre, data-driven.

### Structure corporate (invisible au public)

```
Altistone (Holding)
└── Alti DigiTech (SASU opérationnelle)
    └── FoundryTwo (Studio / marque publique)
        ├── Leak Detector (ACTIF, en mutation vers StoreMD)
        ├── StoreMD (E-commerce — Mois 1, avril)
        ├── ProfitPilot (E-commerce — Mois 1)
        ├── ClientPulse (Agences/Freelancers — Mois 2, mai)
        ├── AdAudit (Agences — Mois 2)
        ├── CreatorSuite (Creators — Mois 3, juin)
        ├── LeadQuiz (E-com + Coaches — Mois 3)
        └── Wildcard (À déterminer — Mois 3)
```

Le public ne voit que FoundryTwo et les produits. Altistone et Alti DigiTech restent invisibles.

---

## 3. MODÈLE OPÉRATIONNEL

### Modèle usine

F code les SaaS pendant que R distribue sur Twitter/LinkedIn et gère les lancements IH/PH. En parallèle, les deux font du warming et de la distribution terrain via le repo CDV (Reddit, Facebook).

### Modèle funnel

R + F = **portes d'entrée** (cold outreach, engagement, conversations). F2 = **hub central** (publication, build in public, milestones). Les gens entrent par R ou F, suivent F2, achètent les produits.

Sur Twitter/LinkedIn (ce repo) : R et F créent du contenu et engagent les communautés e-com, agences, creators. Sur Reddit/Facebook (repo CDV) : R et F font du warming et de la distribution directe dans les communautés verticales.

### Mindset : Build My Community

Chaque action dans ce repo — cold outreach, engagement, publication, cross-engagement — a un double objectif : **convertir** (vendre les SaaS) et **construire la communauté** (créer un groupe de personnes qui suivent FoundryTwo, font confiance au studio, et reviennent à chaque lancement). Le moat de FoundryTwo n'est pas technologique — c'est la communauté.

Les produits ciblent des **NON-devs** : merchants Shopify, freelancers marketing, content creators. Le contenu brand building reflète cette cible.

### 3 projets Claude rédaction

| Projet | System prompt | Fichiers de connaissance | Gère |
|--------|-------------|------------------------|------|
| **FoundryTwo** | `f2/publication/prompt.md` | `f2/publication/context.md` + pipeline 6 SaaS (référence CDV) | Posts @foundrytwo (Twitter, IH, PH, LinkedIn) |
| **Romain** | `romain/system-prompt.md` | Identité + activités + algos + produit | Cold outreach R, engagement R, publication R, publication F2 |
| **Fabrice** | `fabrice/system-prompt.md` | Identité + activités + algos + produit | Cold outreach F, engagement F, publication F |

R rédige ses propres posts R + les posts F2 (studio). F rédige ses propres posts F. Chacun utilise son projet Claude.

### Rôle de Grok

Grok = recherche et filtrage sur Twitter. Pas de rédaction. Les prompts Grok sont dans les sous-dossiers `grok/` de chaque activité (cold, engagement, publication) pour R et F. 1 prompt par vertical : `ECOM-prompt.md` (R lead), `AGENCY-prompt.md` (R lead), `CREATOR-prompt.md` (F lead).

---

## 4. ARCHITECTURE DU REPO

### 4.1 Dossiers de premier niveau

| Dossier | Rôle |
|---------|------|
| `f2/` | Opérations du compte studio @foundrytwo : context, roadmap, playbook, plan-hebdo, progress, publication (Claude + pas de Grok). |
| `romain/` | Opérations des comptes perso de R : context, system-prompt, roadmap, playbook, plan-hebdo, progress + 3 activités (cold, engagement, publication) × 2 outils (Claude, Grok). |
| `fabrice/` | Opérations des comptes perso de F : même structure que romain/ (même volume que R, angle technique/automatisation, full-time). |
| `growth-marketing/` | Stratégie par plateforme : Twitter, LinkedIn, IH, PH, TikTok. Chaque plateforme a un algo.md, un context.md, et des sous-dossiers par compte (romain/, fabrice/, f2/). |
| `saas/` | Contexte produit par SaaS. Pipeline, métriques, positionnement. Référence CDV pour les détails features. |
| `marketing/` | Source de vérité macro : structure corporate, pipeline SaaS, funnel, comptes, cold outreach process, décisions stratégiques. |
| `la-toile/` | Architecture de visibilité de l'écosystème. La Toile = le réseau de nœuds interconnectés (comptes, sites, produits). |
| `asset-brand/` | Identité de marque : brand bible, logo guidelines, assets visuels. |
| `tracking/` | Infrastructure de suivi : Growth Tracker, conventions UTM, process de revue vendredi. |
| `archives/` | Fichiers archivés (plan-hebdo et progress-semaine des semaines passées). |

### 4.2 Principe d'héritage (no-duplication)

```
context.md (ce fichier — source de vérité repo)
│
├── marketing/context.md (funnel, comptes, pipeline, cold outreach process)
│
├── growth-marketing/context.md (Build My Community, piliers contenu, 
│   │                             provocation, personas, cross-plateforme)
│   │
│   ├── growth-marketing/roadmap.md (coordination cross-plateforme)
│   │
│   ├── twitter/ ── algo.md + context.md ── romain/ fabrice/ f2/
│   ├── linkedin/ ── algo.md + context.md ── romain/ fabrice/ f2/
│   ├── ih/ ── algo.md + context.md ── f2/
│   ├── ph/ ── algo.md + context.md ── f2/
│   └── tiktok/ (⏳ TODO)
│
├── f2/ ── context.md ── publication/ ── playbook/roadmap/plan-hebdo/progress
│
├── romain/ ── context.md ── cold/ engagement/ publication/ ── playbook/roadmap/...
│
├── fabrice/ ── context.md ── cold/ engagement/ publication/ ── playbook/roadmap/...
│
├── saas/ ── context.md ── leak-detector/ + sous-dossiers 6 SaaS (référencent CDV)
│
├── tracking/ ── context.md
│
└── la-toile/ ── context.md
```

**Règle absolue :** chaque fichier enfant hérite de son parent et ne duplique JAMAIS le contenu du parent. Les additions vont au niveau le plus bas approprié (généralement le parent, pas chaque enfant). Si une règle est dans `growth-marketing/context.md`, elle n'est pas répétée dans `twitter/context.md`.

### 4.3 Convention de nommage

| Type de fichier | Nom | Rôle |
|----------------|-----|------|
| **context.md** | Stratégie, règles, positionnement | Le "qui/quoi/pourquoi" |
| **roadmap.md** | Progression par phases avec milestones | Le "quand/combien" |
| **playbook-semaine.md** | Process d'exécution fixe (ne change pas d'une semaine à l'autre) | Le "comment" |
| **plan-hebdo.md** | Plan de CETTE semaine (rempli au batch, archivé le dimanche) | Le "quoi cette semaine" |
| **progress-semaine.md** | Carnet de bord de CETTE semaine (rempli au fil de l'eau + vendredi) | Le "qu'est-ce qui s'est passé" |
| **system-prompt.md** | System prompt collé dans le projet Claude | Synthèse des règles pour Claude |
| **prompt.md** | Guide d'utilisation du projet Claude (templates de demande) | Comment parler à Claude |
| **algo.md** | Mécanique algorithmique d'une plateforme (données factuelles) | Le "pourquoi les règles existent" |
| **README.md** | Navigation d'un dossier | La carte |

### 4.4 Convention Grok

| Activité | Fichiers Grok | Convention |
|----------|--------------|-----------|
| cold/ | 1 context + 1 prompt PER VERTICAL | `ECOM-context.md`, `ECOM-prompt.md`, `AGENCY-context.md`, `AGENCY-prompt.md`, `CREATOR-context.md`, `CREATOR-prompt.md` |
| engagement/ | 1 context universel + 1 prompt PER VERTICAL | `context.md`, `ECOM-prompt.md`, `AGENCY-prompt.md`, `CREATOR-prompt.md` |
| publication/ | 1 context universel + 1 prompt PER VERTICAL | `context.md`, `ECOM-prompt.md`, `AGENCY-prompt.md`, `CREATOR-prompt.md` |

---

## 5. RÈGLES TRANSVERSALES

| Règle | Détail |
|-------|--------|
| **Langue** | Toute communication publique en anglais. Marché cible international (US/EU). Documents internes (ce repo) en anglais. |
| **Zéro faux témoignage** | Les scores, les chiffres, les témoignages — tout est réel. Jamais de données inventées. |
| **Données réelles uniquement** | Claude ne produit JAMAIS de contenu sans données réelles fournies par R ou F. Pas de "many users" ou "great results". |
| **Multi-produit** | FoundryTwo est un studio, pas un produit unique. Chaque fichier est conçu pour scaler avec les SaaS suivants sans réécriture. |
| **Vocabulaire séparé** | Vocabulaire forge (forged, anvil, shipped from the forge) = F2 uniquement. R = vocabulaire growth/acquisition. F = vocabulaire technique/automatisation. Produits = vocabulaire CRO standard. |
| **No-duplication** | Aucune règle n'est répétée entre parent et enfant. Héritage strict. |
| **Dossier complet** | Ouvrir un dossier, le compléter à 100%, puis passer au suivant. Ne jamais laisser un dossier à moitié fait. |
| **Validation avant modification** | Aucun fichier n'est créé ou modifié sans validation explicite. |
| **Cible non-dev** | Les produits FoundryTwo ciblent des non-devs (merchants Shopify, freelancers marketing, content creators). Le contenu brand building sur Twitter/LinkedIn montre le build technique MAIS le produit résout un problème business pour des non-devs. |
| **Agent IA + PWA** | Chaque SaaS FoundryTwo est un agent IA (pas un outil) et une PWA. Voir CDV pour les détails techniques. |
| **Synchronisation FT ↔ CDV** | CDV = source de vérité produits. FT = source de vérité brand building. Les voix R et F sont cohérentes entre les 2 repos. |
| **Chacun rédige** | R rédige ses posts R + les posts F2. F rédige ses posts F. Chacun utilise son projet Claude. |
| **Volumes** | 30 interactions/jour par personne sur Twitter/LinkedIn. 10 cold outreach/jour. 1 post/jour. |

---

## 6. ÉTAT DU REPO

Ce repo est en cours de refonte pour s'aligner avec le pivot du 03/04/2026 (repo CDV).

### Complet ✅

| Dossier | Fichiers | Statut |
|---------|---------|--------|
| f2/ | 7 fichiers | ✅ |
| romain/ | 18 fichiers | ✅ |
| fabrice/ | 18 fichiers | ✅ |
| growth-marketing/ | 31 fichiers | ✅ |
| marketing/ | 3 fichiers | ✅ |
| la-toile/ | 5 fichiers | ✅ |
| asset-brand/ | 2 fichiers | ✅ |
| saas/leak-detector/ | 3 fichiers | ✅ |
| saas/ (parent) | 2 fichiers (context + roadmap) | ✅ |
| tracking/ | 1 fichier (context) | ✅ |
| Racine | ARCH.md | ✅ |

### TODO

| Fichier | Raison |
|---------|--------|
| saas/[6 SaaS]/ | Sous-dossiers à créer pour chaque SaaS du pipeline (référencent CDV). |
| growth-marketing/tiktok/ (3 fichiers) | Explicitement différé. Reprend quand social proof et données réelles disponibles. |
| Refonte fichiers activité R + F | Adapter cold/engagement/publication aux verticals et au pivot. |

---

## 7. DOCUMENTS DE RÉFÉRENCE

| Document | Emplacement | Rôle |
|----------|-------------|------|
| context.md | Racine (ce fichier) | Source de vérité repo |
| claude.md | Racine | Règles pour Claude Code sur ce repo |
| README.md | Racine | Navigation complète du repo |
| ARCH.md | Racine | Arbre ASCII de la structure des fichiers |
| marketing/context.md | marketing/ | Source de vérité marketing macro |
| growth-marketing/context.md | growth-marketing/ | Stratégie engagement, Build My Community |
| growth-marketing/README.md | growth-marketing/ | Navigation + arbre d'héritage growth-marketing/ |
| la-toile/context.md | la-toile/ | Architecture de visibilité de l'écosystème |
| asset-brand/FOUNDRYTWO-BRAND-BIBLE.md | asset-brand/ | Identité de marque, storytelling |
| saas/context.md | saas/ | Conventions portefeuille SaaS |
| tracking/context.md | tracking/ | Infrastructure de suivi, UTM |
| **Co-do-va-bu-di (CDV)** | Repo compagnon | **Source de vérité produits** (features, pricing, concurrents, données marché, distribution terrain) |
