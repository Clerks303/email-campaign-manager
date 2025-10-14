# 📧 Naevoo - Plateforme d'Outreach Intelligente

**Automatisez votre prospection B2B avec l'intelligence artificielle**

---

## 🎯 Problème résolu

La prospection B2B moderne exige des campagnes multi-touch personnalisées, un suivi rigoureux des interactions et une qualification intelligente des réponses. Naevoo automatise l'ensemble du cycle de prospection : de la gestion des prospects au suivi des campagnes multi-étapes, du scoring automatique des réponses à l'analyse des performances en temps réel, permettant de réduire de 70% le temps passé sur les tâches répétitives tout en augmentant la qualité de la qualification.

---

## ✨ Fonctionnalités clés

- **Gestion intelligente des prospects** : Import CSV en masse avec déduplication automatique, scoring par IA (GPT-5), segmentation avancée et profils détaillés avec historique complet des interactions

- **Campagnes multi-étapes automatisées** : Séquences d'emails personnalisées avec variables dynamiques, délais anti-spam configurables, tracking des ouvertures/clics en temps réel et gestion avancée des statuts (draft, sending, paused, completed)

- **Agent IA conversationnel** : Assistant intelligent Claude 3.5 intégré pour créer des campagnes par commande vocale, analyser les KPIs automatiquement et générer des réponses contextuelles aux prospects

- **Inbox centralisée avec qualification automatique** : Toutes les conversations regroupées en un seul endroit avec système de Read/Unread, scoring automatique des réponses, et capacité de répondre directement depuis l'interface

- **Analytics temps réel** : Dashboard avec KPIs détaillés (open rate, click rate, response rate), funnel de conversion, graphiques d'évolution et rapports par campagne

---

## 🛠️ Stack technique

### Backend
- **Framework** : FastAPI (Python 3.9+)
- **Base de données** : SQLite (développement) / PostgreSQL (production)
- **ORM** : SQLAlchemy 2.0 avec migrations Alembic
- **Intelligence artificielle** : 
  - Anthropic Claude 3.5 Sonnet (agent conversationnel, réponses automatiques)
  - OpenAI GPT-4 (scoring de prospects)
- **Email & Notifications** : 
  - SMTP multi-providers (Gmail, Outlook, etc.)
  - SendGrid (notifications email)
  - Twilio (notifications SMS)
  - Firebase (push notifications)
- **Scheduler** : APScheduler pour l'envoi séquencé de campagnes
- **Authentification** : JWT avec refresh tokens et rotation automatique

### Frontend
- **Framework** : Next.js 15 avec React 19
- **Styling** : Tailwind CSS avec composants personnalisés
- **Animations** : Framer Motion pour les transitions fluides
- **Visualisation** : Chart.js pour les graphiques analytics
- **Éditeur** : Tiptap (rich text editor) pour la composition d'emails
- **Icons** : Lucide React

### Architecture
- **API REST** : 54 endpoints documentés avec Swagger/OpenAPI
- **Modèle de données** : 8 tables relationnelles optimisées
- **Système d'événements** : 3 déclencheurs automatiques (nouveau prospect, réponse reçue, campagne terminée)
- **Sécurité** : CORS configuré, rate limiting, validation Pydantic, mots de passe hashés (bcrypt)

---

## 📸 Aperçu

*Screenshots à venir*

### Pages disponibles :
- **Dashboard principal** : Vue d'ensemble avec métriques clés
- **Gestion des prospects** : Liste, import CSV, profils détaillés avec scoring IA
- **Campagnes** : Création multi-étapes, planification, suivi des performances
- **Inbox intelligente** : Conversations centralisées avec qualification automatique
- **Analytics** : KPIs temps réel, graphiques d'évolution, rapports détaillés
- **Agent Naevoo** : Chat IA pour automatiser les tâches répétitives
- **Notifications** : Historique complet avec filtres et statistiques
- **Paramètres** : Configuration profil, préférences de notifications, heures calmes

---

## 💼 Contexte d'utilisation

Naevoo est une **plateforme opérationnelle** développée pour répondre aux besoins réels de prospection B2B moderne. Le système gère actuellement :

- **Import et qualification de prospects** : Traitement automatisé de fichiers CSV avec déduplication intelligente et scoring IA instantané
- **Campagnes séquencées** : Envois multi-touch avec délais configurables (30s par défaut) et personnalisation avancée
- **Suivi en temps réel** : Tracking des ouvertures et clics avec mise à jour instantanée des métriques
- **Automatisation intelligente** : Réponses générées par Claude 3.5 basées sur le contexte et le profil du prospect

### Métriques de performance
- ⚡ **Scoring IA** : Analyse GPT-5 en moins de 2 secondes par prospect
- 📊 **Tracking temps réel** : Open & click tracking avec mise à jour instantanée
- 🤖 **Agent IA** : Réponse contextuelle en moins de 5 secondes avec Claude 3.5
- 🔄 **Déclencheurs automatiques** : 3 événements configurés (nouveau prospect, réponse, fin de campagne)

### Architecture modulaire
Le système est conçu avec une architecture **évolutive et maintenable** :
- 54 endpoints API documentés et testés
- 8 tables en base de données avec relations optimisées
- 10 pages frontend responsive et modernes
- 3 providers de notifications intégrés (SendGrid, Twilio, Firebase)

---

## 🔒 Note sur la disponibilité du code

Ce dépôt contient l'**architecture complète** et le **code source** du système Naevoo. 

**Utilisation et déploiement** :
- ✅ Code disponible pour étude et déploiement personnel
- ✅ Documentation complète (installation, configuration, guides d'utilisation)
- ✅ Architecture détaillée et choix techniques explicités
- ⚠️ Logique métier propriétaire et algorithmes de scoring inclus

Pour toute question sur l'architecture, les choix techniques ou une éventuelle collaboration, n'hésitez pas à prendre contact.

---

## 🚀 Démarrage rapide

```bash
# 1. Cloner le repository
git clone <url>
cd Naevoo

# 2. Backend
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp env.example.txt .env  # Configurer les variables d'environnement
uvicorn app.main:app --reload --port 8000

# 3. Frontend (nouveau terminal)
cd frontend
npm install
cp env.example.txt .env.local  # Configurer les variables
npm run dev
```

**Accès** :
- Frontend : http://localhost:3000
- API Backend : http://localhost:8000
- Documentation API : http://localhost:8000/docs

**📚 Consultez le [Guide de Démarrage Rapide](GUIDE_DEMARRAGE_RAPIDE.md) pour plus de détails**

---

## 📊 Système de notifications avancé

Naevoo intègre un **système de notifications multi-canal** complet :

- **3 canaux configurables** : Email (SendGrid), SMS (Twilio), Push (Firebase)
- **3 déclencheurs automatiques** : Nouveau prospect importé, réponse reçue, campagne terminée
- **Préférences personnalisables** : Choix des canaux, heures calmes, types de notifications
- **Historique complet** : Tracking de toutes les notifications envoyées avec statuts et erreurs

**Mode développement** : Fonctionne sans clés API (notifications enregistrées en BDD uniquement)  
**Mode production** : Configuration des providers pour envois réels

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [Guide de Démarrage](GUIDE_DEMARRAGE_RAPIDE.md) | Installation en 5 minutes |
| [Configuration Complète](CONFIGURATION_COMPLETE.md) | Configuration détaillée du système |
| [Agent IA Claude](GUIDE_AGENT_CLAUDE.md) | Utilisation de l'assistant intelligent |
| [Envoi d'Emails](ENVOI_EMAILS_REEL.md) | Configuration SMTP et bonnes pratiques |
| [Système de Notifications](GUIDE_INSTALLATION_NOTIFICATIONS_AVANCEES.md) | Installation SendGrid/Twilio/Firebase |
| [Gestion des Campagnes](GESTION_STATUTS_CAMPAGNES.md) | Gestion avancée des campagnes |
| [Audit Complet](AUDIT_COMPLET_PROJET.md) | Vue d'ensemble des 54 endpoints |
| [API Documentation](http://localhost:8000/docs) | Swagger/OpenAPI (après démarrage) |

---

## ⚡ Fonctionnalités complètes

### Gestion des Prospects
- ✅ Import CSV en masse avec déduplication
- ✅ Scoring automatique par IA (GPT-4)
- ✅ Segmentation et filtres avancés
- ✅ Profils détaillés avec historique complet
- ✅ Notifications automatiques sur nouveaux prospects

### Campagnes d'Emails
- ✅ Séquences multi-étapes personnalisables
- ✅ Variables dynamiques et personnalisation
- ✅ Tracking ouvertures/clics en temps réel
- ✅ Gestion des statuts (draft, sending, paused, completed)
- ✅ Délai anti-spam configurable entre envois
- ✅ Support SMTP multi-providers
- ✅ Fonctions Pause/Resume/Stop

### Analytics & KPIs
- ✅ Dashboard temps réel avec métriques clés
- ✅ Taux par campagne (open, click, response rate)
- ✅ Funnel de conversion
- ✅ Graphiques d'évolution temporelle
- ✅ Rapports détaillés exportables

### Inbox Intelligente
- ✅ Centralisation de toutes les conversations
- ✅ Système Read/Unread automatique
- ✅ Réponse directe depuis l'interface
- ✅ Historique complet par prospect
- ✅ Scoring automatique des réponses

### Agent IA (Naevoo)
- ✅ Chat conversationnel avec Claude 3.5 Sonnet
- ✅ Création de campagnes par commande vocale
- ✅ Analyse automatique des KPIs
- ✅ Suggestions de séquences optimales
- ✅ Réponses contextuelles aux prospects

### Notifications Multi-Canal
- ✅ Email, SMS et Push notifications
- ✅ Préférences personnalisables par utilisateur
- ✅ Heures calmes configurables
- ✅ Historique complet avec filtres
- ✅ Statistiques détaillées (envoyées, échouées, par canal)

---

## 🔒 Sécurité

- ✅ Authentification JWT avec rotation des tokens
- ✅ Mots de passe hashés avec bcrypt
- ✅ Rate limiting sur les endpoints critiques
- ✅ CORS configuré et sécurisé
- ✅ Validation des données avec Pydantic
- ✅ Protection CSRF

**⚠️ Pour la production** : Utiliser PostgreSQL, HTTPS, variables d'environnement sécurisées et monitoring (Sentry)

---

## ⚠️ Conformité et bonnes pratiques

**Important** : Respectez toujours les réglementations en vigueur lors de l'envoi d'emails :
- 🇪🇺 **RGPD** (Europe) : Consentement, droit à l'oubli, portabilité des données
- 🇺🇸 **CAN-SPAM Act** (États-Unis) : Option de désabonnement, identification claire
- 🇨🇦 **CASL** (Canada) : Consentement exprès ou implicite

Naevoo inclut les fonctionnalités nécessaires à la conformité, mais la responsabilité légale incombe à l'utilisateur.

---

## 📬 Contact & Support

**Romain** - Créateur de Naevoo

Pour toute question concernant :
- Architecture et choix techniques
- Déploiement et mise en production
- Collaboration ou contributions
- Support et assistance

N'hésitez pas à prendre contact.

---

## 📝 License

Ce projet est développé pour un usage personnel et professionnel. Le code est disponible à des fins d'étude et de déploiement personnel.

---

<div align="center">

**Naevoo** - Propulsez votre prospection B2B avec l'IA

*Développé avec FastAPI, Next.js, Claude AI et OpenAI*

</div>
