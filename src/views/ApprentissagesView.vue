<script setup lang="ts">
import { ref } from 'vue';

const competences = ref([
  {
    id: 1,
    niveau: 3,
    isOpen: false,
    title: "Compétence 1 - Réaliser des applications",
    description: "Cette compétence concerne le développement d'applications.",
    acs: [
      "AC1: Choisir et implémenter les architectures adaptées",
      "AC2: Faire évoluer une application existante",
      "AC3: Intégrer des solutions dans un environnement de production"
    ],
    projects: [
      {
        title: "API Gestion de Critiques de Jus",
        content: `Projet académique visant à créer une architecture robuste séparant totalement la logique métier (Backend) de l'interface utilisateur (Frontend). Développement d'une API REST complète avec Symfony et API Platform permettant de gérer une base de données de Jus de fruits et les critiques associées.

L'objectif était de créer une architecture adaptée avec une séparation claire des responsabilités :
- API Platform pour générer automatiquement des endpoints REST standardisés (GET, POST, PUT, DELETE) avec documentation OpenAPI intégrée,
- Sérialisation avec groupes de données (serialization groups) pour contrôler finement les données exposées selon le contexte (lecture, écriture, admin),
- Authentification JWT (JSON Web Token) pour sécuriser les endpoints sensibles avec gestion des tokens d'accès et de refresh,
- Voter Symfony pour la gestion fine des droits d'accès au niveau de chaque ressource (ex: un utilisateur ne peut modifier que ses propres critiques),
- Frontend Vue.js consommant l'API via axios avec gestion des états de loading et des erreurs.

Aspects techniques approfondis :
- Création de Custom Operations dans API Platform pour des endpoints spécifiques (ex: recherche par type de jus, filtrage par note),
- Validation des données avec les contraintes Symfony (Assert) pour garantir l'intégrité des données envoyées,
- Pagination et filtrage natifs offerts par API Platform pour gérer de gros volumes de données,
- Tests fonctionnels avec PHPUnit pour valider le bon fonctionnement de chaque endpoint.

Ce projet a permis de valider l'AC1 (choix d'architecture API REST avec API Platform) et l'AC3 (intégration en production avec JWT sécurisé et déploiement sur serveur).`,
        link: "/project/2"
      },
      {
        title: "Capital Wars",
        content: `Digitalisation du jeu de simulation d'entreprise EXIGE. Projet semestriel de 7 mois réalisé en équipe de 5 personnes où les équipes s'affrontent sur un marché virtuel concurrentiel. Le jeu existait auparavant sous format papier/Excel, l'objectif était de le transposer en application web complète.

En tant que Frontend Lead, mes responsabilités et réalisations :
- Conception de l'architecture MVC côté Frontend avec séparation claire entre les vues, les contrôleurs et la logique métier JavaScript,
- Création de tableaux de bord interactifs affichant en temps réel les indicateurs clés (part de marché, bénéfices, RH, production) pour permettre aux joueurs de prendre des décisions stratégiques éclairées,
- Développement de formulaires complexes et validés pour la saisie des décisions stratégiques : fixation des prix, budgets publicitaires, plans d'embauche, investissements en R&D,
- Implémentation d'un système de notifications en temps réel pour informer les joueurs des tours de jeu et des événements du marché,
- Gestion du state côté client pour maintenir la cohérence des données entre les différentes pages du dashboard.

Architecture et techniques :
- Communication avec le Backend via des appels API REST asynchrones (fetch/axios),
- Validation côté client des formulaires pour éviter les allers-retours inutiles vers le serveur,
- Design responsive pour assurer une bonne expérience sur tous les supports,
- Gestion des rôles utilisateurs (Étudiants joueurs vs Arbitres du jeu) avec des interfaces adaptées.

Ce projet a permis de valider l'AC2 (faire évoluer une application existante en digitalisant un processus papier) et l'AC1 (choix d'architecture MVC adaptée pour une application de gestion complexe).`,
        link: "/project/3"
      },
      {
        title: "Grabastar",
        content: `Service centralisé de gestion d'avatars inspiré de Gravatar. Projet réalisé en équipe de 4 étudiants dans le cadre du module "Programmation Avancée Web". L'objectif était de créer un service permettant aux utilisateurs de créer un profil, uploader un avatar, et récupérer leur image via une URL unique basée sur leur email.

Ma contribution principale - Développement Frontend :
- Templates Twig avec utilisation avancée des fonctionnalités : héritage de layouts (block/extends), inclusion de composants (include), et création de macros pour les éléments réutilisables (formulaires, cartes de profil),
- Upload sécurisé d'avatars avec validation côté serveur (type MIME, taille max, extension) et redimensionnement automatique via la librairie Imagine pour générer plusieurs tailles (thumbnail, medium, large),
- Interface de gestion de profil avec prévisualisation en temps réel de l'avatar avant validation,
- Design responsive en CSS pur (sans framework) avec utilisation de Flexbox et CSS Grid pour la mise en page, media queries pour l'adaptation mobile.

Ma contribution secondaire - Administration :
- Développement de commandes console Symfony pour les tâches d'administration : nettoyage des avatars orphelins, export des statistiques utilisateurs, génération de rapports,
- Création d'une interface d'administration restreinte pour la modération des avatars (suppression d'images inappropriées).

Sécurité et production :
- Protection CSRF sur tous les formulaires via les tokens Symfony,
- Vérification des permissions avec Voters pour garantir qu'un utilisateur ne puisse modifier que son propre profil,
- Stockage sécurisé des fichiers avec renommage aléatoire et déplacement hors du dossier web public,
- Mise en production sur le serveur universitaire avec configuration Apache, gestion des permissions et optimisation des performances.

Ce projet a validé l'AC3 grâce à la mise en production sur serveur universitaire avec gestion sécurisée des fichiers et l'AC1 par le choix d'une architecture Symfony/Twig adaptée.`,
        link: "/project/4"
      }
    ]
  },
  {
    id: 5,
    niveau: 3,
    isOpen: false,
    title: "Compétence 5 - Conduire un projet",
    description: "Cette compétence concerne la conduite de projet.",
    acs: [
      "AC1: Mesurer les impacts économiques, sociétaux et technologiques d'un projet informatique",
      "AC2: Savoir intégrer un projet informatique dans le système d'information d'une organisation",
      "AC3: Savoir adapter un système d'information",
      "AC4: Accompagner le management de projet informatique"
    ],
    projects: [
      {
        title: "Capital Wars",
        content: `Digitalisation du jeu de simulation d'entreprise EXIGE. Projet semestriel de 7 mois (Sept 2025 - Mar 2026) réalisé en équipe de 4 personnes. Les équipes dirigent des entreprises fabriquant des appareils électriques et s'affrontent sur un marché virtuel concurrentiel en prenant des décisions stratégiques à chaque tour (année) : fixation des prix, budget publicité, gestion des RH (embauches, salaires), et investissements en R&D.

Le défi technique majeur était de transformer un manuel de jeu dense (gestion de bilans, comptes de résultats, amortissements) en une application web fluide et intuitive avec deux rôles distincts : Étudiants (joueurs) et Professeurs (arbitres).

Ce projet a permis de valider :
- AC1 (Impacts économiques, sociétaux et technologiques) : Le jeu simule un marché concurrentiel où les équipes gèrent les impacts financiers, humains et environnementaux de leurs décisions. Analyse des coûts de production, bilan carbone implicite des décisions industrielles, et compréhension des mécanismes économiques réels (offre/demande, part de marché).
- AC2 (Intégration dans le SI) : L'application s'intègre dans le système d'information pédagogique de l'IUT, remplaçant un processus papier/Excel par une solution web centralisée avec gestion des rôles et des permissions.
- AC4 (Management de projet) : En tant que Frontend Lead, coordination du travail entre l'équipe backend et frontend, utilisation de GitLab pour la gestion de version avec revues de code, organisation de meetings réguliers et respect des jalons du semestre.`,
        link: "/project/3"
      },
      {
        title: "Nuit de l'Info 2025",
        content: `Événement national (4-5 Décembre 2025) où des équipes développent un site web en 15 heures pour promouvoir des causes numériques. Édition 2025 sur le thème "Village Numérique Résistant" : imaginer comment les établissements scolaires peuvent tenir tête aux géants du Web ("Big Tech") et promouvoir la démarche NIRD (Numérique Inclusif, Responsable et Durable).

Équipe de 10 personnes avec répartition des rôles : chatbot, génération d'images, mini-jeu laser game, et pages principales du site. Méthodologie agile avec brainstorming initial (18h-20h), développement intensif (20h-05h) et finitions/livraison (05h-08h).

Ma contribution :
- Conception et développement complète de la page "Sobriété Numérique" en CSS natif (sans framework), expliquant les impacts du numérique (pollution, consommation) et les bonnes pratiques NIRD,
- Page d'accueil réalisée entièrement en CSS3 pur avec animations fluides sur mesure, cohérent avec le thème de la sobriété numérique (code ultra-léger),
- Collaboration Git avec résolution de conflits lors du merge final.

Ce projet a permis de valider :
- AC1 : Impacts sociétaux du projet (sensibilisation au numérique responsable, eco-conception web).
- AC2 : Intégration et déploiement sur GitHub Pages pour l'association organisatrice.
- AC3 : Adaptation aux contraintes extrêmes (15h, fatigue, nécessité de prioriser les fonctionnalités essentielles).
- AC4 : Gestion de projet sous pression, coordination d'équipe de 10 personnes, répartition des tâches et communication efficace.`,
        link: "/project/1"
      }
    ]
  },
  {
    id: 6,
    niveau: 3,
    isOpen: false,
    title: "Compétence 6 - Collaborer dans un projet",
    description: "Cette compétence concerne la collaboration.",
    acs: [
      "AC1: Organiser et partager une veille numérique",
      "AC2: Identifier les enjeux de l'économie de l'innovation numérique",
      "AC3: Guider la conduite du changement informatique au sein d'une organisation",
      "AC4: Accompagner le management de projet informatique"
    ],
    projects: [
      {
        title: "Capital Wars",
        content: `Projet semestriel de 7 mois (Sept 2025 - Mar 2026) en équipe de 4 personnes avec des rôles bien définis : Backend, Frontend, Base de données, et Arbitres.

Organisation et collaboration mises en place :
- Utilisation de GitLab pour la gestion de version avec une stratégie de branching claire (main, dev, feature branches) et des merge requests systématiques avec revues de code par les pairs,
- En tant que Frontend Lead, j'ai servi de pont entre l'équipe backend et l'équipe frontend : définition conjointe des contrats d'API, documentation des endpoints nécessaires, et validation des données échangées,
- Meetings quotidiens (stand-ups de 10-15 min) pour suivre l'avancement, identifier les blocages et réajuster les priorités,
- Gestion des conflits de fusion lors de l'intégration des différentes fonctionnalités frontend,
- Utilisation de l'outil de suivi de tâches (issues GitLab) pour répartir le travail et suivre la progression.

Ce projet a validé l'AC4 (accompagner le management de projet) grâce à la coordination entre les membres de l'équipe, la répartition équitable des tâches et le maintien d'une dynamique de groupe positive sur la durée du semestre. L'AC1 a également été sollicitée via la veille sur les bonnes pratiques Git et les méthodologies agiles adaptées aux projets scolaires.`,
        link: "/project/3"
      },
      {
        title: "Grabastar",
        content: `Projet réalisé en équipe de 4 étudiants dans le cadre du module "Programmation Avancée Web". L'objectif était de créer un service centralisé de gestion d'avatars inspiré de Gravatar.

Organisation de la collaboration :
- Répartition claire des tâches entre backend (API, gestion des utilisateurs, sécurité des fichiers) et frontend (templates Twig, CSS, UX),
- Utilisation de Git pour la gestion de version avec résolution régulière des conflits lors des merges,
- Respect d'un cahier des charges strict défini par les enseignants : sécurité des fichiers uploadés, droits d'accès granulaires, validation des emails pour la génération d'URL d'avatar,
- Sessions de programmation en binôme pour les parties les plus complexes (upload et redimensionnement d'images).

Veille et innovation (AC1 & AC2) :
- Organisation d'une veille technologique sur les services d'avatars existants (Gravatar, DiceBear, etc.) pour identifier les fonctionnalités attendues et les standards du marché,
- Analyse des enjeux économiques d'un service type Gravatar : modèle économique basé sur la gratuité avec monétisation via les APIs premium pour les entreprises,
- Identification des enjeux de l'innovation numérique : comment un service apparemment simple peut devenir un standard utilisé par des milliers de plateformes.`,
        link: "/project/4"
      },
      {
        title: "Nuit de l'Info 2025",
        content: `Hackathon national de 15 heures (4-5 Décembre 2025) en équipe de 10 personnes sur le thème "Village Numérique Résistant". L'événement impose des contraintes extrêmes : temps limité, fatigue, nécessité de livrer un produit fonctionnel en une nuit.

Organisation sous pression :
- Brainstorming initial structuré (18h-20h) pour définir le concept, répartir les rôles et établir un plan d'action : chatbot, génération d'images, mini-jeu laser game, pages principales,
- Adoption immédiate d'un Git Flow simplifié : chaque membre travaille sur sa feature branch avec des merges réguliers vers la branche principale,
- Coordination continue tout au long de la nuit : points réguliers, entraide entre les membres, et adaptation en temps réel des priorités en fonction de l'avancement.

Conduite du changement et innovation (AC2 & AC3) :
- Veille éclair sur les technologies à utiliser : choix de Vue.js pour la rapidité de développement et la modularité, CSS natif pour la sobriété numérique (cohérent avec le thème),
- Adaptation de notre manière de travailler à l'urgence : simplification des processus, acceptance du "fait est mieux que parfait", focus sur les fonctionnalités essentielles,
- Innovation dans l'approche éco-responsable : conception d'un site léger et performant, en phase avec la démarche NIRD (Numérique Inclusif, Responsable et Durable).

Ce projet a particulièrement validé l'AC1 (veille numérique rapide et ciblée), l'AC3 (conduite du changement sous pression avec adaptation des méthodes de travail) et l'AC4 (management d'une équipe de 10 personnes dans un contexte de stress et de fatigue).`,
        link: "/project/1"
      }
    ]
  },
  {
    id: 2,
    niveau: 2,
    isOpen: false,
    title: "Compétence 2 - Optimiser des applications",
    description: "Cette compétence concerne la sélection et l'utilisation d'algorithmes adaptés pour résoudre efficacement des problèmes complexes.",
    acs: [
      "AC1: Choisir des structures de données complexes adaptées au problème",
      "AC2: Utiliser des techniques algorithmiques adaptées pour des problèmes complexes",
      "AC3: Comprendre les enjeux et moyens de sécurisation des données et du code",
      "AC4: Évaluer l'impact environnemental et sociétal des solutions proposées"
    ],
    projects: [
      {
        title: "Développement d’un algorithme de chiffrement des données (RSA)",
        content: `Dans le cadre de mon stage, j’ai été chargé d’implémenter un algorithme de chiffrement RSA dans le but de sécuriser les données sensibles des clients de l’entreprise. Ce projet m’a permis de mobiliser l’ensemble des apprentissages critiques associés à la compétence "sélection et utilisation d'algorithmes adaptés pour résoudre efficacement des problèmes complexes".

Tout d’abord, le choix des structures de données a été déterminant pour garantir l’efficacité et la robustesse du chiffrement. J’ai utilisé des structures adaptées telles que les grands entiers (pour les clés), des paires de clés publiques/uniques. Ce choix, réfléchi et justifié, relève de l’AC1.

Ensuite, le développement de l’algorithme m’a permis de mettre en œuvre des techniques algorithmiques avancées (AC2), notamment :
- la génération de grands nombres premiers,
- l’exponentiation modulaire,
- et le calcul de l’inverse modulaire via l’algorithme d’Euclide étendu.

Ces éléments sont essentiels au bon fonctionnement de l’algorithme RSA, qui repose sur des fondements mathématiques solides et une logique algorithmique rigoureuse.

Ce projet m’a aussi permis de me confronter directement aux enjeux de la sécurité informatique (AC3). En plus du chiffrement, j’ai intégré des mécanismes de validation des entrées pour éviter les injections SQL, protégé les clés contre les fuites potentielles, et suivi les bonnes pratiques en matière de développement sécurisé.

Enfin, j’ai également pris en compte les aspects environnementaux et sociétaux (AC4). L’algorithme ayant un coût computationnel élevé, j’ai optimisé les traitements pour réduire la consommation de ressources (temps CPU, mémoire), et ainsi limiter l’impact environnemental. Sur le plan sociétal, la sécurisation des données client contribue à renforcer la protection de la vie privée, un enjeu majeur dans notre société numérique.

Ainsi, ce projet a été une occasion concrète d’appliquer et de valider la compétence visée, à travers un travail complet allant de l’analyse du besoin à l’implémentation, en passant par l’optimisation et la sécurisation du code.`,
        link: "/project/6"
      }
    ]
  },
  {
    id: 3,
    niveau: 2,
    isOpen: false,
    title: "Compétence 3 - Administrer des systèmes informatiques communicants complexes",
    description: "Cette compétence concerne le déploiement et la gestion de services dans une architecture réseau.",
    acs: [
      "AC1: Concevoir et développer des applications communicantes",
      "AC2: Utiliser des serveurs et des services réseaux virtualisés",
      "AC3: Sécuriser les services et données d'un système"
    ],
    projects: [
      {
        title: "TP - Développement d’applications communicantes en C avec l’API Socket",
        content: `Dans le cadre des travaux pratiques du module réseau, j’ai conçu plusieurs applications client-serveur en langage C, en utilisant l’API socket avec le protocole TCP/IP. Ces applications permettaient d’établir une communication fiable entre deux machines pour l’échange de messages textuels ou de fichiers.

Ce travail m’a permis de valider l’AC1, car il m’a donné l’opportunité de maîtriser la création de sockets, la gestion des connexions multiples via select() et la structuration des échanges réseau. J’ai également implémenté des mécanismes de détection et gestion des erreurs réseau, et respecté les normes liées au protocole TCP pour garantir une communication fiable et structurée.`,
        link: null
      },
      {
        title: "Sécurisation de l’authentification utilisateur",
        content: `Lors d’un projet de développement d’un site web en PHP, j’ai mis en place un système d’authentification sécurisé. Pour cela, j’ai utilisé un mécanisme de hachage des mots de passe avec ajout de sel et poivre avant stockage en base de données.

J’ai également veillé à la sécurité des sessions en régénérant les identifiants de session et en configurant les cookies avec les options HttpOnly et Secure.

Cette mise en œuvre m’a permis de valider l’AC3 en assurant la protection des données sensibles des utilisateurs face à des menaces courantes telles que le vol de mots de passe, les attaques par force brute ou le vol de session. J’ai appliqué les bonnes pratiques de sécurité web et suivi les recommandations de l’OWASP.`,
        link: "/project/7"
      }
    ]
  },
  {
    id: 4,
    niveau: 2,
    isOpen: false,
    title: "Compétence 4 - Gérer des données de l’information",
    description: "Cette compétence concerne l'optimisation des bases de données et leur intégration dans des applications tout en garantissant la sécurité.",
    acs: [
      "AC1: Optimiser les modèles de données de l'entreprise",
      "AC2: Assurer la confidentialité des données (intégrité et sécurité)",
      "AC3: Organiser la restitution de données à travers la programmation et la visualisation",
      "AC4: Manipuler des données hétérogènes"
    ],
    projects: [
      {
        title: "Développement d'un site E-Commerce",
        content: `Réalisation d'un site de e-commerce proposant des produits de notre choix, sans restrictions particulières. L’objectif pédagogique de ce projet était de mettre en œuvre les techniques apprises en cours tout en respectant les critères de notation établis, notamment la gestion des produits via un MVC.

Cette réalisation m'a permis de travailler sur l'AC2 en mettant en œuvre des mécanisme de securité comme le hachage de mot de passe, la préparation de requêtes SQL limitant les injections de tous type.

Également, ce travail m'a permis de développer l'AC1 en créant une interface qui simplifie les opérations CRUD (Create, Read, Update, Delete) et en implémentant des mise en cache pour réduire la charge sur la base de données. Ce qui a impliqué les compétences CE4.01, CE4.02 et CE4.04 en respectant les règlementations sur le respect de la vie privé, en assurant la cohérence et la qualité du code et pour finir en respectant les enjeux économiques, sociétaux et écologiques de l'utilisation du stockage de données.`,
        link: "/project/7"
      },
      {
        title: "Interface de gestion commerciale et comptable",
        content: `Réalisation d’une application web destinée à centraliser la gestion des activités commerciales et comptables d'une entreprise fictive. L'objectif pédagogique de ce projet était de structurer, exploiter et restituer efficacement des données commerciales (factures, paiements) à travers une interface claire et fonctionnelle, tout en appliquant les bonnes pratiques de développement et de visualisation.

Cette réalisation m’a permis de valider l’AC3 en mettant en place des tableaux de bord dynamiques et interactifs pour les utilisateurs. Ces tableaux affichaient des indicateurs clés (Nom de compte, informations bancaires, paiement, etc.) sous forme de tableaux et de visualisations créés avec la librairie DataTables de JavaScript.

J’ai également développé des fonctionnalités de filtres, tris et exports (PDF, CSV) permettant une restitution personnalisée et exploitable des données. J’ai également mobilisé l’AC4 en traitant des données hétérogènes provenant de différentes sources comme des fichiers Excel transmis par les commerciaux et des informations saisies directement via l'interface utilisateur. Cela m’a amené à implémenter des mécanismes de nettoyage, validation, formatage et transformation des données pour assurer leur intégration dans la base de données de manière cohérente.`,
        link: "/project/6"
      }
    ]
  }
]);

const toggleCompetence = (id: number) => {
  const competence = competences.value.find(c => c.id === id);
  if (competence) {
    competence.isOpen = !competence.isOpen;
  }
};
</script>

<template>
  <div class="min-h-screen bg-slate-50 dark:bg-slate-950 pt-32">

    <div class="container mx-auto px-6 md:px-12 pb-20">

      <div class="text-center mb-16">
        <h1 class="text-4xl md:text-5xl font-bold text-slate-900 dark:text-white mb-6">
          Portfolio <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-500 to-teal-500">d'Apprentissage</span>
        </h1>
        <p class="text-slate-600 dark:text-slate-400 max-w-2xl mx-auto text-lg">
          Validation des compétences du BUT Informatique à travers mes projets et expériences.
          <br><span class="text-sm opacity-70">(Cliquez sur une compétence pour voir les détails)</span>
        </p>
      </div>

      <div class="mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-slate-900 dark:text-white mb-2 flex items-center gap-3">
          <span class="w-12 h-12 rounded-xl bg-gradient-to-r from-amber-500 to-orange-500 text-white flex-shrink-0 flex items-center justify-center text-xl font-bold shadow-lg shadow-amber-500/30">
            3
          </span>
          Niveau 3
        </h2>
        <p class="text-slate-500 dark:text-slate-400 ml-15 text-lg">Compétences de BUT3 (BAC+3)</p>
      </div>

      <div class="space-y-6 mb-20">

        <section
          v-for="comp in competences.filter(c => c.niveau === 3)"
          :key="comp.id"
          class="bg-white dark:bg-slate-900 rounded-3xl overflow-hidden border border-slate-200 dark:border-slate-800 shadow-sm transition-all duration-300"
          :class="{ 'shadow-xl ring-2 ring-indigo-500/10': comp.isOpen }"
        >
          <div
            @click="toggleCompetence(comp.id)"
            class="cursor-pointer p-6 md:p-8 flex items-start justify-between gap-6 hover:bg-slate-50 dark:hover:bg-slate-800/50 transition-colors"
          >
            <div class="flex-1">
              <h2 class="text-2xl md:text-3xl font-bold text-slate-900 dark:text-white flex items-center gap-4">
                <span class="w-10 h-10 rounded-lg bg-indigo-600 text-white flex-shrink-0 flex items-center justify-center text-lg font-bold shadow-lg shadow-indigo-500/30">
                  {{ comp.id }}
                </span>
                {{ comp.title.split(' - ')[1] }}
              </h2>
              <p class="mt-2 text-slate-500 dark:text-slate-400 italic md:ml-14">
                {{ comp.description }}
              </p>
            </div>

            <div class="flex-shrink-0 mt-2">
              <svg
                class="w-6 h-6 text-slate-400 transition-transform duration-300"
                :class="{ 'rotate-180 text-indigo-600': comp.isOpen }"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </div>
          </div>

          <div v-show="comp.isOpen" class="border-t border-slate-100 dark:border-slate-800">
            <div class="p-6 md:p-8 grid grid-cols-1 lg:grid-cols-12 gap-12">

              <div class="lg:col-span-4">
                <div class="bg-slate-50 dark:bg-slate-950/50 p-6 rounded-2xl border border-slate-200 dark:border-slate-800">
                  <h3 class="font-bold text-slate-900 dark:text-white mb-4 flex items-center gap-2">
                    <svg class="w-5 h-5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                    Apprentissages Critiques
                  </h3>
                  <ul class="space-y-3">
                    <li
                      v-for="(ac, idx) in comp.acs"
                      :key="idx"
                      class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed pl-3 border-l-2 border-indigo-200 dark:border-indigo-800"
                    >
                      <strong class="text-indigo-600 dark:text-indigo-400">{{ ac.split(':')[0] }}:</strong>
                      {{ ac.split(':')[1] }}
                    </li>
                  </ul>
                </div>
              </div>

              <div class="lg:col-span-8 space-y-10">

                <div
                  v-for="(projet, idx) in comp.projects"
                  :key="idx"
                  class="relative pl-0 md:pl-8 border-l-0 md:border-l border-slate-200 dark:border-slate-800"
                >
                  <div class="hidden md:block absolute -left-[5px] top-0 w-2.5 h-2.5 rounded-full bg-slate-300 dark:bg-slate-700"></div>

                  <h3 class="text-xl font-bold text-slate-800 dark:text-white mb-4">
                    {{ projet.title }}
                  </h3>

                  <div class="prose dark:prose-invert max-w-none text-slate-600 dark:text-slate-300 whitespace-pre-line mb-6 text-sm md:text-base">
                    {{ projet.content }}
                  </div>

                  <div v-if="projet.link">
                    <RouterLink
                      :to="projet.link"
                      class="inline-flex items-center gap-2 text-sm font-semibold text-indigo-600 dark:text-indigo-400 hover:underline"
                    >
                      Voir le projet détaillé
                      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path></svg>
                    </RouterLink>
                  </div>
                </div>

              </div>

            </div>
          </div>

        </section>

      </div>

      <div class="mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-slate-900 dark:text-white mb-2 flex items-center gap-3">
          <span class="w-12 h-12 rounded-xl bg-gradient-to-r from-indigo-500 to-purple-500 text-white flex-shrink-0 flex items-center justify-center text-xl font-bold shadow-lg shadow-indigo-500/30">
            2
          </span>
          Niveau 2
        </h2>
        <p class="text-slate-500 dark:text-slate-400 ml-15 text-lg">Compétences de BUT2 (BAC+2)</p>
      </div>

      <div class="space-y-6">

        <section
          v-for="comp in competences.filter(c => c.niveau === 2)"
          :key="comp.id"
          class="bg-white dark:bg-slate-900 rounded-3xl overflow-hidden border border-slate-200 dark:border-slate-800 shadow-sm transition-all duration-300"
          :class="{ 'shadow-xl ring-2 ring-indigo-500/10': comp.isOpen }"
        >
          <div
            @click="toggleCompetence(comp.id)"
            class="cursor-pointer p-6 md:p-8 flex items-start justify-between gap-6 hover:bg-slate-50 dark:hover:bg-slate-800/50 transition-colors"
          >
            <div class="flex-1">
              <h2 class="text-2xl md:text-3xl font-bold text-slate-900 dark:text-white flex items-center gap-4">
                <span class="w-10 h-10 rounded-lg bg-indigo-600 text-white flex-shrink-0 flex items-center justify-center text-lg font-bold shadow-lg shadow-indigo-500/30">
                  {{ comp.id }}
                </span>
                {{ comp.title.split(' - ')[1] }}
              </h2>
              <p class="mt-2 text-slate-500 dark:text-slate-400 italic md:ml-14">
                {{ comp.description }}
              </p>
            </div>

            <div class="flex-shrink-0 mt-2">
              <svg
                class="w-6 h-6 text-slate-400 transition-transform duration-300"
                :class="{ 'rotate-180 text-indigo-600': comp.isOpen }"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </div>
          </div>

          <div v-show="comp.isOpen" class="border-t border-slate-100 dark:border-slate-800">
            <div class="p-6 md:p-8 grid grid-cols-1 lg:grid-cols-12 gap-12">

              <div class="lg:col-span-4">
                <div class="bg-slate-50 dark:bg-slate-950/50 p-6 rounded-2xl border border-slate-200 dark:border-slate-800">
                  <h3 class="font-bold text-slate-900 dark:text-white mb-4 flex items-center gap-2">
                    <svg class="w-5 h-5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                    Apprentissages Critiques
                  </h3>
                  <ul class="space-y-3">
                    <li
                      v-for="(ac, idx) in comp.acs"
                      :key="idx"
                      class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed pl-3 border-l-2 border-indigo-200 dark:border-indigo-800"
                    >
                      <strong class="text-indigo-600 dark:text-indigo-400">{{ ac.split(':')[0] }}:</strong>
                      {{ ac.split(':')[1] }}
                    </li>
                  </ul>
                </div>
              </div>

              <div class="lg:col-span-8 space-y-10">

                <div
                  v-for="(projet, idx) in comp.projects"
                  :key="idx"
                  class="relative pl-0 md:pl-8 border-l-0 md:border-l border-slate-200 dark:border-slate-800"
                >
                  <div class="hidden md:block absolute -left-[5px] top-0 w-2.5 h-2.5 rounded-full bg-slate-300 dark:bg-slate-700"></div>

                  <h3 class="text-xl font-bold text-slate-800 dark:text-white mb-4">
                    {{ projet.title }}
                  </h3>

                  <div class="prose dark:prose-invert max-w-none text-slate-600 dark:text-slate-300 whitespace-pre-line mb-6 text-sm md:text-base">
                    {{ projet.content }}
                  </div>

                  <div v-if="projet.link">
                    <RouterLink
                      :to="projet.link"
                      class="inline-flex items-center gap-2 text-sm font-semibold text-indigo-600 dark:text-indigo-400 hover:underline"
                    >
                      Voir le projet détaillé
                      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path></svg>
                    </RouterLink>
                  </div>
                </div>

              </div>

            </div>
          </div>

        </section>

      </div>

    </div>
  </div>
</template>
