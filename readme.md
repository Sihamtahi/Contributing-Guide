# Contribution & Collaboration des projets Canopée

Ce document détaille et explique les règles des commits et de collaboration sur gitlab.

## Flux des contributions et amélioration des fonctionnalités

Si vous voulez améliorer/corriger une fonctionnalité et/ou corriger un bug qu'un autre membre de l'équipe a developpé, veuillez suivre les étapes suivantes pour proposer votre amélioration :

```
    ┌───────────────────────┐
    │                       │
    │   ouvrir un issue     │
    │  (signaler un bug ou  │
    │  demande de fonction) │
    │                       │
    └───────────────────────┘
               ⇩
    ┌───────────────────────┐
    │                       │
    │  Ouvrir Pull Request  │
    │   (uniquement après   │
    │ validation l'issue )  │
    │                       │
    └───────────────────────┘
               ⇩
    ┌───────────────────────┐
    │                       │
    │   Vos changements     │
    │   vont ête merged     │
    │     après tests       │
    │                       │
    └───────────────────────┘
```

## Commits conventionnels et Format des commits

Chaque fois que vous effectuez un commit, vous enregistrez un instantané de votre projet sur lequel vous pourrez revenir ou comparer ultérieurement. Un message de commit est un texte descriptif qui est ajouté à l'objet par le développeur. Un commit en français est une livraison donc lorsqu'on commit on livre une version/avancement/fonctionnalité/correction du projet. Il comporte une ligne de titre et un corps facultatif.
Les messages d'engagement sont utilisés de nombreuses façons à savoit :

- Aider un futur lecteur à comprendre rapidement ce qui a changé et pourquoi cela a changé.
- Aider à annuler facilement des changements spécifiques
- Préparer des notes de modification ou des versions de substitution pour une version.

Il existe plusieurs “conventions d’écriture” qui visent à harmoniser les manières d’écrire les messages.
Les messages commit nous permettent de dire ce qui a changé et pourquoi. Pour avoir un historique de commit et améliorer la compréhension des commits. Le format des commits à adopter pour nous est le suivant :

```
<type>(<scope>): <subject>
```

### Type :

<type> sont des préfixes inspirés de [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary) specification et de [How to write a good commit message](https://dev.to/chrissiemhrk/git-commit-message-5e21). Ils servent à tagué le commit, ils nous donnent le type du commit en question. Ils peuvent être :

- `fix: ` Une correction de bug .
- `feat: ` Une amélioration d'une fonctionnalité ou une nouvelle fonctionnalité.
- `docs: ` Un changement de documentation.
- `chore: ` Une réogranisation de fichiers ou nettoyage du projet comme les mises à jour des tâches de construction(build tasks), des configurations du gestionnaire de paquets (npm, gulp), etc
- `style: ` Tout ce qui concerne le style couleur, polices de texte, les tailles, etc
- `test: ` tout ce qui concerne les tests .
- `refactor: ` Le préfixe dans le titre indique que le PR est uniquement lié au refactoring du code.
- `ci: ` Modifications des fichiers de configuration et de nos scripts de CI (Intégration Continue)

### Scope :

Le scope est le nom du package npm affecté. Il peut être http, router, forms, etc.
Le scope est optionnel, on le met si on connait le nom du package. Le scope est optionnel. Si on connait pas les packages affectés ou s'il en existe pas, nous rajoutons pas de scope dans le commit.

### Subject :

L'objet contient une description succincte du changement en français :

- utilisez l'impératif, le présent : "change" et non "changé" ou "changement".
- ne mettez pas de majuscule à la première lettre
- pas de point (.) à la fin

N'oubliez pas que le titre doit être clair et descriptif, avec l'utilisation de la forme verbale/impérative inspirée de [imperative mood](https://chris.beams.io/posts/git-commit/#imperative).
Pour trouver la forme verbale, nous pouvons poser les questions suivantes :

En anglais, le message du commit devrait compléter la phrase “If applied, this commit will `le sujet du commit` “.

En français, le message doit compléter la phrase “Ce commit…“. Exemples:

- Ce commit `refactore le sous-système X pour plus de lisibilité`
- Ce commit `met à jour la documentation de démarrage`
- Ce commit `supprime les méthodes obsolètes`
- Ce commit `publie la version 1.0.0`
