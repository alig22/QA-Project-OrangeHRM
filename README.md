# QA-Project-OrangeHRM
Ce projet présente un test fonctionnel manuel complet réalisé sur le module Login de l'application OrangeHRM — une application RH open source utilisée comme environnement de test.

 Objectifs des Tests


✅ Vérifier le bon fonctionnement du login avec des identifiants valides
✅ Valider les messages d'erreur pour les cas invalides
✅ Tester la validation des champs obligatoires
✅ Vérifier la compatibilité cross-browser (Chrome, Firefox)
✅ Tester le comportement sur mobile (responsive)
✅ Identifier les anomalies de sécurité et d'ergonomie



🧪 Cas de Test — Résumé

IDTitreStatutSévéritéTC001Login avec identifiants valides✅ PASSÉCritiqueTC002Mot de passe incorrect✅ PASSÉHauteTC003Champs vides✅ PASSÉHauteTC004Username inexistant✅ PASSÉHauteTC005Username vide + mdp saisi✅ PASSÉHauteTC006Username vide uniquement✅ PASSÉHauteTC007Test sur Firefox✅ PASSÉMoyenneTC008Test mobile responsive✅ PASSÉMoyenneTC009Copier-coller mot de passe⏳ NON EXÉCUTÉBasseTC010Username avec espaces⏳ NON EXÉCUTÉBasse


🐛 Bugs Détectés

BUG001 — 🔴 Critique

Titre : Aucune limite de tentatives de connexion
Description : Le système n'impose aucun blocage après plusieurs tentatives échouées, exposant l'application à des attaques par force brute.
Résultat obtenu : Aucun blocage après 10+ tentatives
Résultat attendu : Blocage du compte après 5 tentatives + CAPTCHA
Impact : Risque de sécurité majeur


BUG002 — 🟡 Moyenne

Titre : Message d'erreur trop générique
Description : Le message "Invalid credentials" ne précise pas si l'erreur vient du username ou du mot de passe.
Résultat obtenu : Message générique identique pour tous les cas d'erreur
Résultat attendu : Messages distincts selon le champ incorrect
Impact : Mauvaise expérience utilisateur


📊 Métriques d'Exécution

Total cas de test prévus   : 10
Cas exécutés               : 8
Cas PASSÉS            ✅   : 8
Cas ÉCHOUÉS           ❌   : 0
Cas non exécutés      ⏳   : 2
Taux de réussite           : 100%
Bugs détectés              : 2
  └── Critiques 🔴         : 1
  └── Moyens    🟡         : 1


🛠️ Outils Utilisés

CatégorieOutilsGestion des testsJira · TestRailDocumentationGoogle Sheets · Microsoft ExcelTests UIChrome · Firefox · Chrome DevToolsTests mobileChrome DevTools (mode responsive)Reporting bugsShareX (captures d'écran)MéthodesBlack Box Testing · STLC


📁 Structure du Repository

QA-Portfolio-OrangeHRM/
│
├── 📊 Projet_QA_OrangeHRM_Complet.xlsx
│   ├── Feuille 1 : Plan de Test
│   ├── Feuille 2 : Cas de Test (10 cas)
│   ├── Feuille 3 : Rapports de Bugs
│   ├── Feuille 4 : Résumé & Métriques
│   └── Feuille 5 : Screenshots (8 preuves)
│
└── 📖 README.md


📸 Aperçu des Screenshots


Les screenshots réels de l'exécution des tests sont disponibles dans le fichier Excel — Feuille 5 "Screenshots".

TC001 — Login valideTC003 — Champs videsTC008 — Mobile✅ Dashboard affiché✅ Required affiché✅ Interface adaptée


🎓 Compétences Démontrées

✅ Rédaction d'un plan de test complet
✅ Conception et exécution de cas de test (Black Box)
✅ Rédaction de rapports de bugs structurés
✅ Tests cross-browser et mobile
✅ Identification d'anomalies de sécurité
✅ Analyse des métriques de test
✅ Application des principes STLC
