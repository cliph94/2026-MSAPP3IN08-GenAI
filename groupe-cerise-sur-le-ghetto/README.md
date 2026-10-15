# Cerise sur le ghetto — Réécriture contrôlée par attributs

## Groupe

| Membre | Contribution principale |
|---|---|
| @cliph94 | Porteur du fork ; préparation initiale avec assistance déclarée |
| Second compte à ajouter | Binôme G15 du classeur ; inscription personnelle en cours |

## Sujet

- **Identifiant du catalogue :** A6 — Réécriture contrôlée par attributs.
- **Réservation :** [demande #7](https://github.com/jsboigeEPF/2026-MSAPP3IN08-GenAI/issues/7), en attente de confirmation de l'enseignant.
- **Problématique :** une IA peut-elle modifier la longueur, le registre, le niveau de lecture et le ton d'un texte tout en conservant son sens et ses faits ?
- **MVP prévu :** corpus de 40 textes publics ou synthétiques, quatre contraintes réévaluables, pipeline de réécriture et mesures automatiques complétées par une vérification factuelle annotée.

## Architecture

Architecture prévue : textes et contraintes → construction du prompt → modèle texte autorisé par le cours → réécriture → contrôles de contraintes et de conservation des faits → rapport comparatif. Le premier commit initialise uniquement le dossier depuis `template-groupe/` ; aucune application n'est encore livrée.

## Installation

Pas d'installation applicative à cette étape : le sujet doit être confirmé. Le fichier `.env.example` reprend les seuls noms des variables du gabarit ; aucun secret n'est présent.

Figez les versions dans un fichier de dépendances ou un lockfile adapté à votre écosystème. Copiez `.env.example` vers `.env`, puis renseignez localement les valeurs. Ne commitez jamais `.env`.

## Utilisation

Aucune commande d'exécution pour l'instant. Les commandes reproductibles seront ajoutées avec le premier démonstrateur.

## Tests

Aucun test applicatif à cette étape documentaire. Les tests prévus couvriront le texte vide, les contraintes incompatibles, les faits modifiés, la réponse invalide et l'indisponibilité du fournisseur.

Aucun résultat technique revendiqué à ce stade.

## Résultats et évaluation

Baseline prévue : consigne simple de réécriture. Comparaison : prompt structuré nommant les contraintes et les faits à préserver. Un petit pilote permettra de figer le protocole avant l'essai sur les 40 textes. Mesures : écart de longueur, respect du registre/ton/niveau de lecture, similarité sémantique, dérive factuelle, coût et latence. Les cas défavorables seront conservés. Aucun taux de réussite n'est encore disponible.

## Limites et plan B

Le service d'embeddings du module est annoncé indisponible : prévoir une mesure locale et documenter la méthode. Une similarité élevée ne garantit pas la conservation des faits. Les mesures de style nécessitent une grille explicite ; nous distinguerons contrôles automatiques et annotations humaines. Budget cible du catalogue : moins de 8 €. Plan B : réécritures pré-générées avec annotations, sans présenter une sortie enregistrée comme un appel en direct.

## Répartition du travail

La répartition humaine reste à convenir à deux ; aucune contribution du second membre n'est revendiquée. Le groupe relira les corrections et chacun devra expliquer architecture, mesures et limites. Commits progressifs et PR brouillon à utiliser pour rendre l'avancement visible.

## Assistance IA

Initialisation et rédaction préparées avec assistance de ChatGPT/Codex, déclarée conformément à `AGENTS.md`. Cette étape ne constitue pas un projet terminé ni une validation du sujet.

## Licence et références

Gabarit issu du dépôt du cours (MIT). Corpus et modèles restent à sélectionner avec leurs licences. Ressources de départ : [fiche A6](https://github.com/jsboigeEPF/2026-MSAPP3IN08-GenAI/blob/main/docs/CATALOGUE.md#a6--réécriture-contrôlée-par-attributs), notebooks CoursIA `02_PromptEngineering.ipynb`, `03_Structured_Outputs.ipynb` et `22_Evaluating_Generated_Text.ipynb`.
