# ETM Car-Solution — Proposition C (codes des grands réseaux)

Site vitrine one-page statique. Aucune dépendance, aucun build : `index.html` suffit.
Déploiement : GitHub → Vercel → preset **Other** → Deploy.

## D'où vient cette structure
Analyse des sites de référence du secteur : **BR-Performance**, **Digiservices** (30+ centres, leader français),
**Motortech**, **France-Reprog**, et **ECU-Repar** — qui est basé à Toulouse, donc concurrent direct du client.

Ce qu'ils ont tous et que les deux maquettes précédentes n'avaient pas :

| Élément repris | Vu chez |
|---|---|
| Simulateur de gains marque → modèle → motorisation | France-Reprog, AutoTrade, Motortech |
| Barres comparatives origine vs Stage 1 (ch et Nm) | France-Reprog, Digiservices |
| Méthode en 4 étapes (pré-diagnostic → sauvegarde → intervention → contrôle) | Digiservices |
| Bloc d'engagements (réversible, tolérances constructeur, backup) | BR-Performance |
| Explication pédagogique « qu'est-ce qu'un calculateur / Stage 1 vs Stage 2 » | BR-Performance, Digiservices |
| FAQ | BR-Performance, Motortech |
| Horaires d'atelier + zone d'intervention | BR-Performance, ECU-Repar |
| Formulaire avec véhicule et kilométrage | BR-Performance |
| Barre de statut en haut (ouvert / zone) | ECU-Repar |

## ⚠️ À faire valider par le client avant mise en ligne

1. **Les chiffres du simulateur** (`const DATA` dans `index.html`) sont des estimations indicatives de Stage 1
   pour les modèles les plus courants en France. Le client doit les corriger avec ses propres relevés :
   ce sont les chiffres qu'on lui opposera si un client conteste.
2. **Les horaires** (Lun-Ven 9h-19h, Sam 9h-17h) sont un exemple — à confirmer.
3. **Aucun avis client n'a été inventé.** Les concurrents affichent tous une note Google (BR-Performance : 4,8/5
   sur 551 avis). Quand le client aura sa fiche Google Business avec de vrais avis, on branchera un widget :
   c'est le levier de conversion numéro un sur ce marché.
4. **Photos** : visuels de démonstration issus de templates open source, incrustés en base64 dans `index.html`
   et disponibles en WebP dans `assets/photos/`. À remplacer par les vraies photos de l'atelier.
5. **Logo** : `assets/logo/` — reconstitutions vectorielles d'après la carte de visite et le flyer.

## Formulaire
Les demandes partent vers **etm.carsolution@gmail.com** via FormSubmit.
Au premier envoi, FormSubmit envoie un mail d'activation à cette adresse : cliquer le lien **une seule fois**.
