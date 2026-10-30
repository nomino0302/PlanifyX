# PlanifyX

PlanifyX est une application de gestion commerciale qui réunit les activités quotidiennes d'un commerce dans une interface web.

## Fonctionnalités

- Gérer les produits et suivre les stocks.
- Enregistrer les ventes en caisse, y compris en mode hors ligne.
- Consulter les factures et les informations des clients.
- Gérer les fournisseurs et leurs commandes.
- Suivre les employés et les indicateurs d'activité dans des tableaux de bord.

## Technologies

- **Frontend** : JavaScript, React 19, Vite, React Router, Tailwind CSS et Flowbite. Zustand gère une partie de l'état, Axios les requêtes HTTP, Recharts les graphiques et le plugin Vite PWA les fonctionnalités d'application web progressive.
- **Backend** : Python, Django 6, Django REST Framework, authentification JWT et documentation OpenAPI avec drf-spectacular. Le projet utilise aussi APScheduler et ReportLab.
- **Base de données** : PostgreSQL.

Le code est réparti entre `frontend/` et `backend/`. Les scripts SQL se trouvent dans `backend/sql/`.

## Démarrage local

Prévoir Python compatible avec Django 6, Node.js et PostgreSQL. Créer une base PostgreSQL, copier `backend/model.env` vers `backend/.env` et renseigner les paramètres de l'application, de la base de données et du courrier électronique.

Dans un terminal, depuis `backend/` :

```sh
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Dans un autre terminal, depuis `frontend/`, copier `model.env` vers `.env`, renseigner l'adresse de l'API (`VITE_API_BASE_URL=http://127.0.0.1:8000` pour une installation locale), puis lancer :

```sh
npm install
npm run dev
```

L'interface est accessible sur `http://localhost:5173` et la documentation de l'API sur `http://127.0.0.1:8000/api/docs/`.

## Crédits

- Asmaou B.
- Anthony T.
- Brahim B.
