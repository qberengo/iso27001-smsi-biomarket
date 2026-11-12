# SMSI ISO 27001 — BioMarket

Mise en place d'un **Système de Management de la Sécurité de l'Information (SMSI)** conforme à l'**ISO/IEC 27001:2022** pour une enseigne de distribution qui lance sa plateforme e-commerce : analyse du contexte, PSSI, analyse de risques EBIOS RM, plan de continuité d'activité et plan d'actions de sécurité chiffré.

Projet réalisé pour la certification en cybersécurité de Datascientest (septembre 2026). Cas d'étude fictif.

📄 **[Rapport principal (41 pages)](Rapport%20-%20SMSI%20BioMarket.pdf)** · 📁 **[Annexes](annexes/)**

## Contexte

BioMarket distribue des produits biologiques dans plus de 50 magasins du Nord de la France et de Belgique. L'entreprise lance une plateforme e-commerce, développée par un prestataire sur une infrastructure PaaS, qui expose de nouvelles données personnelles (clients, commandes, paiements) sur Internet. La DSI veut intégrer la sécurité dès la conception et préparer une certification ISO 27001.

## Démarche et livrables

| Étape | Contenu | Annexe |
| --- | --- | --- |
| Analyse du contexte | PESTEL, SWOT, parties prenantes, besoins de sécurité, veille, OSINT, cartographie du SI | A |
| Plan projet de certification | Organisation, jalons, Gantt, budget prévisionnel (315 k€ HT) | B |
| PSSI | Politique de sécurité et 8 documents de gouvernance (ci-dessous) | C, C1 à C8 |
| Analyse de risques | Méthode **EBIOS Risk Manager** : événements redoutés, scénarios, traitement | D |
| Plan de continuité d'activité | BIA, activités critiques, scénarios de crise, stratégie de reprise | E |
| Plan d'actions de sécurité | 11 actions priorisées (195 k€ HT), architecture cible, planning | F |

Documents de gouvernance rédigés : matrice RACI, procédure de gestion des incidents, procédure de gestion des changements, **procédure de gestion des habilitations**, classification des informations, programme de sensibilisation, charte informatique, lettre d'engagement de la Direction.

## Principaux constats

- Comptes non désactivés après le départ des collaborateurs, pratiques de mots de passe faibles, MFA limité à certains comptes.
- Données sensibles stockées en clair, gouvernance de la sécurité peu formalisée.
- Risques majeurs : compromission de l'Active Directory, rançongiciel, vol de données personnelles, indisponibilité de la plateforme.

## Mesures recommandées

| Priorité | Actions |
| --- | --- |
| P1 – Critique | MFA généralisé, revue semestrielle des habilitations (moindre privilège), politique de mots de passe, EDR, segmentation et isolation des serveurs critiques |
| P2 – Haute | Chiffrement des postes (BitLocker) et des sauvegardes, SIEM, sensibilisation, encadrement des accès prestataires |
| P3 – Moyenne | Formalisation de la gestion des changements |

Architecture cible : segmentation par VLAN (serveurs critiques, sauvegardes isolées), DMZ pour l'application e-commerce, filtrage inter-zones par pare-feu UTM, VPN SSL avec MFA, EDR et SIEM.

## Référentiels utilisés

ISO/IEC 27001:2022 · ISO/IEC 27002 · EBIOS Risk Manager (ANSSI) · RGPD · recommandations ANSSI · NIST · OWASP · MITRE ATT&CK · ENISA

## Compétences mises en œuvre

Gouvernance SSI · analyse de risques · rédaction de politiques et procédures · gestion des identités et des habilitations · continuité d'activité · conformité RGPD · architecture de sécurité · chiffrage et priorisation budgétaire

Projet lié : **[Audit et sécurisation d'Iron4Software](https://github.com/qberengo/pentest-hardening-iron4software)**, le prestataire qui développe la plateforme e-commerce.
