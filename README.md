# DUERP

**Français** · [English](#english)

Un outil libre pour aider les employeurs français à rédiger et tenir à jour leur DUERP (document unique d'évaluation des risques professionnels), simplement, sans consultant, et sans que leurs données quittent leur poste.

> **État : projet en démarrage.** Pas encore de code utilisable. Ce document décrit le but et l'architecture prévue ; le dépôt se remplira au fil du travail.

## Pourquoi

Tout employeur en France, dès le premier salarié, doit évaluer les risques professionnels et les consigner dans un document unique, mis à jour au moins une fois par an dans les entreprises de 11 salariés et plus (Code du travail, articles R4121-1 et suivants). Beaucoup de petites entreprises trouvent l'exercice confus, paient un consultant, ou ne le font pas.

Le risque chimique est souvent la partie la plus difficile : il faut lire les fiches de données de sécurité (FDS) des fournisseurs et en tirer une évaluation.

## Ce que l'outil veut offrir

- **Simple** : un employeur sans formation en prévention doit pouvoir faire son DUERP seul, guidé pas à pas.
- **Adaptable** : chaque entreprise part d'une base par métier et l'ajuste à sa réalité (unités de travail, risques, cotation, mesures), plutôt que de remplir un modèle générique.
- **Confidentiel** : les calculs tournent dans le navigateur ; les données de l'entreprise restent chez elle.
- **Traçable** : chaque changement du document est daté et conservé, pour garder l'historique des versions successives.
- **Ouvert sur les outils publics** : à terme, une intégration avec La Suite numérique, la suite d'outils libres de l'État.
- **Accompagné** : guides et tutoriels pour que des personnes non techniques maîtrisent l'outil.

## Architecture prévue

| Partie | Technologie | Pourquoi |
|---|---|---|
| Cœur : modèle de risque, cotation, historique, lecture des FDS | Rust compilé en WebAssembly | fiabilité d'un document légal, exécution locale dans le navigateur, un seul exécutable pour l'auto-hébergement |
| Interface | TypeScript / React, design de l'État (DSFR) | rapidité de développement, cohérence avec les outils publics |
| Contenu : risques par métier, mesures de prévention | fichiers YAML / CSV | lisibles et modifiables par des préventeurs, sans savoir programmer |

## Contribuer

Le projet aura besoin de deux sortes de contributions :

- **Contenu** (préventeurs, QHSE, services de santé au travail) : catalogues de risques par métier, mesures de prévention, relecture des guides.
- **Code** (Rust, TypeScript).

Les modalités de contribution (dont un accord de contribution) seront publiées avant l'ouverture aux contributions extérieures.

## Responsabilité

L'outil aide à rédiger le DUERP ; il ne remplace pas l'évaluation de l'employeur, qui reste responsable de son document et des risques de son entreprise.

## Licence

Code sous licence [GNU AGPL v3.0 ou ultérieure](LICENSE). Toute personne qui modifie ce logiciel et le distribue, ou le met à disposition en ligne, doit publier ses modifications sous la même licence.

Pour un usage hors des conditions de l'AGPL (licence commerciale), contactez le mainteneur.

La licence porte sur le code, pas sur les noms ni les logos du projet.

---

## English

A free and open-source tool to help French employers write and maintain their DUERP (*document unique d'évaluation des risques professionnels*, the mandatory written workplace risk assessment): simply, without a consultant, and without their data leaving their computer.

> **Status: early stage.** No usable code yet. This document describes the goal and the planned architecture; the repository will grow as work progresses.

### Why

Every employer in France, from the first employee, must assess workplace risks and record them in a single document, updated at least yearly in companies with 11 or more employees (French Labour Code, article R4121-1 and following). Many small businesses find it confusing, pay a consultant, or skip it.

Chemical risk is often the hardest part: it means reading suppliers' Safety Data Sheets (SDS) and turning them into an assessment.

### What the tool aims to offer

- **Simple**: an employer with no health-and-safety training can write their DUERP alone, guided step by step.
- **Adaptable**: each company starts from a trade-specific base and adjusts it to its own situation (work units, risks, scoring, measures), instead of filling in a generic template.
- **Private**: computation runs in the browser; the company's data stays with the company.
- **Traceable**: every change to the document is dated and kept, preserving the history of successive versions.
- **Open to public tools**: eventually, integration with La Suite numérique, the French government's open-source workplace suite.
- **Supported**: guides and tutorials so non-technical people can master the tool.

### Planned architecture

| Part | Technology | Why |
|---|---|---|
| Core: risk model, scoring, history, SDS reading | Rust compiled to WebAssembly | reliability for a legal document, local execution in the browser, single binary for self-hosting |
| Interface | TypeScript / React, French government design system (DSFR) | development speed, consistency with public tools |
| Content: risks by trade, prevention measures | YAML / CSV files | readable and editable by health-and-safety professionals without coding |

### Contributing

The project will need two kinds of contributions:

- **Content** (health-and-safety professionals, occupational health services): risk catalogues by trade, prevention measures, guide reviews.
- **Code** (Rust, TypeScript).

Contribution terms (including a contributor agreement) will be published before the project opens to outside contributions.

### Responsibility

The tool helps write the DUERP; it does not replace the employer's own assessment. The employer remains responsible for the document and for the risks in their business.

### License

Code licensed under the [GNU AGPL v3.0 or later](LICENSE). Anyone who modifies this software and distributes it, or makes it available over a network, must publish their changes under the same license.

For use outside the AGPL terms (commercial license), contact the maintainer.

The license covers the code, not the project's names or logos.
