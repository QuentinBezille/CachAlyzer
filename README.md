# 🧭 Dashboard Geocaching Master Pro

**Dashboard Geocaching Master Pro** est une application web puissante, 100% locale et sans serveur, conçue pour les géocacheurs exigeants. Elle permet d'analyser vos fichiers de découvertes (`.gpx` et `.txt`) pour générer des statistiques interactives, traquer vos challenges (Fizzy, Jasmer, 366, 360°) et retrouver intelligemment vos FTF oubliés.

---

## ✨ Fonctionnalités Principales

### 📊 1. Statistiques et Habitudes
*   **KPIs Dynamiques :** Total des caches, répartition physiques/labs, plus longues séries (streaks), et périodes creuses (slumps).
*   **Graphiques Avancés :** Découvertes mensuelles/cumulées, répartition par types et tailles (via *Chart.js*).
*   **Radars d'habitudes :** Analyse de vos jours de la semaine et mois de l'année les plus prolifiques.

### 🗓️ 2. Calendrier Interactif
*   Agenda complet (via *FullCalendar*) affichant vos trouvailles au jour le jour.
*   Barre de recherche rapide pour sauter directement à une date spécifique.
*   Classement interactif du "Top 50" de vos meilleures journées de géocaching.

### 🎯 3. Suivi des Challenges Internationaux
*   **Matrice D/T (Fizzy 81) :** Grille interactive avec calcul de la difficulté/terrain moyenne.
*   **Calendrier 366 Jours :** Remplissez chaque jour de l'année.
*   **Challenge Jasmer :** Grille chronologique (de l'an 2000 à aujourd'hui) basée sur la date de pose des caches. Onglets de filtrage par type inclus !
*   **Challenge 360° (Premium) :** Radar azimutal calculant vos découvertes autour de vos coordonnées de domicile, avec vue sur carte interactive.

### 🏆 4. Moteur FTF & Paliers (Exclusivité)
*   **Liste des FTF :** Détection automatique via vos tags (`{*FTF*}`, `[FTF]`, etc.).
*   **Moteur d'Oublis Hybride V5 :** Croise un GPX de zone avec vos logs Project-GC pour calculer une probabilité (de 0 à 100%) d'avoir fait un FTF non taggué, grâce à une analyse sémantique (détection d'aveux d'échec, STF, mots-clés).
*   **Paliers & Premières fois :** Liste de vos jalons (100, 500, 1000...) et de vos "premières" par pays, région et type de cache.

### 🗺️ 5. Cartographie Dynamique
*   Cartes du monde, d'Europe et choroplèthes par régions (France, Belgique, USA, etc.) générées dynamiquement.
*   Système de repli intelligent utilisant *Leaflet* et des GeoJSON externes pour un affichage net et détaillé.

### 🛠️ 6. Outils Créateurs
*   **Générateur de script Lua :** Créez facilement le code nécessaire pour configurer un Checker Project-GC personnalisé (basé sur le type, la taille, la difficulté, le mot-clé, etc.).

---

## 🚀 Installation & Lancement

L'application est **entièrement locale** (Client-Side). Aucune base de données ni serveur (PHP/Node) n'est requis. Vos données ne quittent jamais votre ordinateur.

1. Clonez ou téléchargez ce dépôt sur votre machine.
2. Assurez-vous d'avoir les 3 fichiers de base dans le même dossier :
   * `index.html` (Structure)
   * `style.css` (Design & Mode Sombre)
   * `script.js` (Moteur d'analyse)
3. Ouvrez simplement **`index.html`** avec n'importe quel navigateur web moderne (Chrome, Firefox, Edge, Safari).

---

## 📂 Comment importer ses données ?

Pour profiter pleinement du Dashboard, vous devez fournir vos données officielles :

### 1. Fichier Principal (GPX)
*   Allez sur [Geocaching.com > Pocket Queries](https://www.geocaching.com/pocket/).
*   Dans l'onglet "My Finds", cliquez sur **Ajouter à la liste d'attente**.
*   Téléchargez le fichier ZIP, extrayez le fichier `.gpx`, et chargez-le dans la zone **"1. DONNÉES PRINCIPALES"**.

### 2. Lab Caches (TXT)
*   Allez sur votre profil [Project-GC](https://project-gc.com/).
*   Accédez à vos Lab Caches trouvées.
*   Copiez tout le tableau (Ctrl+A / Ctrl+C) et collez-le (Ctrl+V) dans un fichier texte brut (`labs.txt`).
*   Chargez-le dans l'outil.

### 3. Outil FTF Oubliés (Hybride)
*   **TXT Patron :** Exportez vos "My Finds Logs" depuis Project-GC.
*   **GPX Zone :** Générez une Pocket Query englobant vos caches récentes pour avoir l'historique complet des logs concurrents.

---

## 🎨 Interface & Ergonomie
*   **Mode Sombre / Clair :** Thème entièrement dynamique géré via CSS variables. Les graphiques et cartes s'adaptent instantanément.
*   **Sauvegarde Locale :** Votre pseudo, domicile, réglages de thème et exclusions FTF sont mémorisés dans le `localStorage` de votre navigateur.
*   **Design Responsive :** Interface propre, barres de défilement (scrollbars) personnalisées transparentes et fenêtres modales "pop-up" esthétiques.

---

## 💻 Technologies Utilisées

*   **HTML5 / CSS3** (Vanilla, CSS Grid, Flexbox)
*   **JavaScript (ES6+)** (Vanilla, DOMParser)
*   **[Chart.js](https://www.chartjs.org/)** (Graphiques radar, barres, polaires)
*   **[FullCalendar](https://fullcalendar.io/)** (Agenda interactif)
*   **[Leaflet](https://leafletjs.com/)** (Cartographie interactive et tracés géo-spatiaux)

---

## 🔒 Confidentialité des données
**100% de la puissance de calcul s'exécute dans votre navigateur.** L'application ne contient aucun script de tracking externe, et aucune coordonnée ni log de vos fichiers GPX n'est envoyée vers un serveur tiers.

---
*Fait avec passion pour la communauté Geocaching.* 🌍🔍
