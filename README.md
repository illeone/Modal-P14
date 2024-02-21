
# Fenêtre modale

Une bibliothèque React pour ajouter facilement des modales interactives à votre application. 
Lorsque la modale s'active, elle apparaît au milieu de l'écran. 
Cette modale est accompagnée d'un effet de transition fluide du haut vers le bas, avec un fond légèrement obscurci qui isole la modale du reste de l'interface, captant immédiatement l'attention de l'utilisateur.

Le package est disponible sur npm : [@il_leone/modal-react](https://www.npmjs.com/package/@il_leone/modal-react)

## Prérequis

Pour utiliser cette bibliothèque, vous aurez besoin de :

- Node.js (v12.0.0 ou plus récent)
- npm (v6.0.0 ou plus récent)

## Installation

Pour ajouter cette bibliothèque à votre projet React, exécutez :

```bash
npm install @il_leone/modal-react
```

## Comment l'utiliser

### Importez la Modal dans votre composant React :

```jsx
import React, { useState } from "react";
import { Modal } from '@il_leone/modal-react';
```

### Intégrez la Modal dans votre application :

Voici un exemple d'utilisation simple, déclenchant l'ouverture de la modale via un bouton :

```jsx
const App = () => {
  const [isModalOpen, setIsModalOpen] = useState(false);

  const toggleModal = () => {
    setIsModalOpen(!isModalOpen);
  };

  return (
    <div className="App">
      <button onClick={toggleModal}>Ouvrir la modale</button>
      <Modal
        isOpen={isModalOpen}
        btnOk
        btnOkAction={toggleModal}
        title="Titre de la modale"
        description="Description de la modale"
      />
    </div>
  );
};

export default App;
```

## Propriétés

- `isOpen` (booléen) : Indique si la modale est ouverte ou fermée.
- `btnOk` (booléen) : Affiche un bouton "OK" dans la modale.
- `btnOkAction` (fonction) : Fonction à exécuter lorsqu'on clique sur le bouton "OK".
- `title` (chaîne) : Titre de la modale.
- `description` (chaîne) : Description ou contenu de la modale.
