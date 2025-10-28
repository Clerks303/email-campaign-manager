# Naevoo – Plateforme d’automatisation de prospection B2B pilotée par IA

## Résumé exécutif
Naevoo est une plateforme d'outreach B2B pilotée par l'IA qui automatise la prospection multi‑étapes, la qualification des réponses et l'analyse des performances en temps réel. L'objectif: réduire de ~70% le temps passé sur les tâches répétitives, tout en améliorant la qualité de qualification et la mesure du ROI.

## Problème business
Les équipes Sales/Marketing gèrent des volumes croissants de prospects et doivent personnaliser leurs séquences, suivre les KPIs et qualifier vite les réponses. Les outils existants imposent beaucoup d'opérations manuelles et des intégrations complexes.

## Solution livrée
- Gestion de prospects: import CSV en masse, déduplication, segmentation, scoring IA
- Campagnes multi‑étapes: variables dynamiques, délais anti‑spam, pause/reprise/stop
- Tracking temps réel: ouvertures, clics, réponses, KPIs et rapports par campagne
- Inbox centralisée: conversations, read/unread, réponse directe, historique par prospect
- Agent IA: création de campagnes, analyse automatique des KPIs, réponses contextuelles

## Impact (mesuré)
- ~70% de réduction du temps sur les tâches répétitives
- Scoring IA < 2 s / prospect
- Réponses IA contextuelles < 5 s (agent Claude 3.5)

## Architecture (aperçu)
- Backend: FastAPI (Python), SQLAlchemy + Alembic, JWT + refresh, APScheduler
- Frontend: Next.js 15 / React 19, Tailwind, Chart.js, Tiptap
- IA: Anthropic Claude 3.5 (agent), OpenAI (scoring)
- Notifications: SendGrid (email), Twilio (SMS), Firebase (push)

Ce case study ne publie pas le code propriétaire. Il présente l'architecture, les choix techniques, les résultats et une démo produit.

## Démo (vidéo)
Lien : 
https://github.com/user-attachments/assets/0d98ab89-c9f1-4887-8aa3-a39fa1c82f31


## ScreenShots avec données fictives :

- Campagnes : <img width="1015" height="515" alt="Campagnes" src="https://github.com/user-attachments/assets/35696e6d-eed3-49b7-95bf-73af5861f1e4" />

- Inbox : <img width="1014" height="574" alt="Inbox" src="https://github.com/user-attachments/assets/defc63d4-49bf-4bbb-80a7-bbd962106de2" />

- Analytics : <img width="1022" height="573" alt="Analytics" src="https://github.com/user-attachments/assets/b3dfd565-53a9-4866-9996-86e3b8b4b474" />


## Pourquoi cette approche est "production‑ready"
- 54 endpoints REST documentés (Swagger)
- Migrations Alembic et séparation dev/prod (SQLite → PostgreSQL)
- Sécurité: JWT, bcrypt, CORS, rate limiting, validation Pydantic
- Orchestration: APScheduler pour l'envoi séquencé anti‑spam
- Observabilité: logs structurés, gestion d'erreurs, guides d'ops

## Ce que vous trouverez ici (public)
- Présentation produit orientée valeur et résultats
- Architecture et décisions clés
- Script de démo vidéo et shotlist
- Texte "Pourquoi moi ? en 10 lignes"

## Ce que vous ne trouverez pas ici
- Code source propriétaire, secrets, BDD, logs
- Algorithmes détaillés de scoring et logique métier sensible

## Contact
Romain — Créateur de Naevoo  
[Insérer email / LinkedIn]  


