# 🌍 Marketplace Blockchain de Billets Mondial 2030

![Blockchain](https://img.shields.io/badge/Blockchain-Ethereum-627EEA?style=for-the-badge&logo=ethereum)
![Solidity](https://img.shields.io/badge/Smart_Contracts-Solidity-363636?style=for-the-badge&logo=solidity)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=for-the-badge&logo=node.js)
![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge&logo=mongodb)


## 📋 Table des matières

- [À propos du projet](#-à-propos-du-projet)
- [Problématique](#-problématique)
- [Solution proposée](#-solution-proposée)
- [Fonctionnalités principales](#-fonctionnalités-principales)
- [Architecture technique](#-architecture-technique)
- [Technologies utilisées](#-technologies-utilisées)
- [Smart Contracts](#-smart-contracts)
- [Avantages](#-avantages)


## 🎯 À propos du projet

**Marketplace Blockchain de Billets Mondial 2030** est une plateforme décentralisée révolutionnaire qui transforme la vente et la revente de billets pour les grands événements sportifs. En utilisant la technologie blockchain et les NFTs, nous garantissons authenticité, transparence et équité dans l'écosystème de la billetterie.

### Vision

Créer un marché secondaire de billets où :
- ✅ Chaque billet est authentifié et infalsifiable
- ✅ Les prix sont régulés pour éviter la spéculation abusive
- ✅ Les organisateurs bénéficient de chaque revente
- ✅ L'historique complet est traçable et transparent

---

## 🚨 Problématique

Le marché actuel de la billetterie souffre de plusieurs problèmes critiques :

|           Problème                  |                     Impact                       |
|-------------------------------------|--------------------------------------------------|
| **Contrefaçon**                     | Des milliers de billets faux vendus chaque année |
| **Spéculation excessive**           | Prix multipliés par 5 ou 10 sur le marché noir   |
| **Absence de traçabilité**          | Impossible de vérifier l'authenticité            |
| **Organisateurs non rémunérés**     | Aucun bénéfice sur le marché secondaire          |
| **Expérience utilisateur médiocre** | Processus complexe et peu sécurisé               |



## 💡 Solution proposée

Notre plateforme résout ces problèmes grâce à quatre piliers technologiques :

### 1. 🎫 NFT Authentifiés
Chaque billet est un token non-fongible (NFT) unique avec un QR code infalsifiable généré on-chain.

### 2. 💵 Paiements Stables (USDT)
Utilisation d'une stablecoin pour éliminer la volatilité des cryptomonnaies traditionnelles.

### 3. 📊 Prix Régulés
Plafond automatique de revente à 120% du prix initial pour empêcher la spéculation excessive.

### 4. 💰 Royalties Automatiques
5% de chaque revente reversés automatiquement à l'organisateur via smart contract.

## ⚡ Fonctionnalités principales

### Pour les utilisateurs

- 🛒 **Achat de billets NFT** : Achetez des billets authentifiés directement sur la plateforme
- 💼 **Gestion de collection** : Visualisez et gérez tous vos billets en un seul endroit
- 🔄 **Revente sécurisée** : Revendez vos billets facilement avec protection intégrée
- 📱 **QR Code unique** : Chaque billet génère un QR code pour l'accès au stade
- 📜 **Historique complet** : Consultez l'historique complet de chaque billet
- 🔐 **Wallet MetaMask** : Connexion simple via MetaMask

### Pour les organisateurs

- 🎨 **Création de billets** : Émission de billets NFT avec toutes les métadonnées
- 💎 **Royalties automatiques** : 5% de revenus sur chaque revente
- 📊 **Tableau de bord** : Suivi des ventes et analytics en temps réel
- 🔍 **Traçabilité totale** : Visibilité complète sur le marché secondaire


## 🏗 Architecture technique

┌────────────────────────────┐
│   Utilisateur (Client)     │
│    🧍 via Navigateur       │
└────────────┬───────────────┘
             │
    Connexion Web3 (MetaMask)
             │
┌────────────▼────────────────┐
│  Frontend (React/Lovable)   │
│  - Affichage billets        │
│  - Appels API Node.js       │
│  - Interactions Web3        │
└────────────┬────────────────┘
             │ (HTTP + Web3)
┌────────────▼────────────────┐
│   Backend Node.js (API)     │
│  - Routes Express           │
│  - Écoute blockchain        │
│  - Sauvegarde MongoDB       │
└────────────┬────────────────┘
             │     │
   ┌─────────┘     └─────────┐
   │                          │
┌──▼────────────────┐  ┌─────▼──────────────┐
│ Blockchain (ETH)  │  │  MongoDB Database  │
│ - Smart Contracts │  │  - Billets, logs   │
│ - NFT, ventes     │  │  - QR codes, users │
└───────────────────┘  └────────────────────┘

### Composants principaux

|      Composant        |         Technologie             |                    Rôle                      |
|-----------------------|---------------------------------|----------------------------------------------|
| **Smart Contracts**   | Solidity / Foundry              | Gestion des NFT, ventes, reventes, royalties |
| **Blockchain**        | Ethereum (Sepolia/Polygon Amoy) | Stockage transactions et propriété           |
| **Backend API**       | Node.js + Express.js            | Pont entre frontend et blockchain            |
| **Base de données**   | MongoDB                         | Données off-chain : historique, QR codes     |
| **Frontend**          | React                           | Interface utilisateur intuitive              |
| **Token de paiement** | USDT (ERC-20)                   | Paiements stables sans volatilité            |
| **Stockage**          | IPFS                            | Stockage décentralisé des images             |



## 🛠 Technologies utilisées

### Blockchain & Smart Contracts
- **Solidity** `^0.8.20` - Langage de programmation des smart contracts
- **Foundry** - Framework de développement et testing
- **OpenZeppelin** - Bibliothèques de contrats sécurisés
- **Hardhat** (optionnel) - Environnement de développement alternatif

### Backend
- **Node.js** `v18+` - Runtime JavaScript
- **Express.js** `^4.18` - Framework web
- **Ethers.js** `^6.0` - Interaction avec la blockchain
- **Mongoose** `^8.0` - ODM pour MongoDB
- **dotenv** - Gestion des variables d'environnement
- **cors** - Gestion des requêtes cross-origin

### Frontend
- **React** `^18.2` - Bibliothèque UI
- **Web3.js** / **Ethers.js** - Interaction blockchain côté client
- **MetaMask SDK** - Intégration wallet
- **TailwindCSS** - Framework CSS
- **React Router** - Navigation

### Base de données & Stockage
- **MongoDB** `^7.0` - Base de données NoSQL
- **IPFS** - Stockage décentralisé
- **Pinata** (optionnel) - Service IPFS managé

### DevOps & Déploiement
- **Vercel** - Hébergement frontend
- **Render** / **Railway** - Hébergement backend
- **MongoDB Atlas** - Base de données cloud


## 📝 Smart Contracts

### 1. MondialTicketNFT.sol

**Standard** : ERC-721 (NFT)

**Fonctionnalités** :
```solidity
// Création d'un billet NFT
function createTicket(
    string memory team,
    string memory category,
    uint256 price,
    string memory qrCode
) public returns (uint256)

// Récupération des infos d'un billet
function getTicketInfo(uint256 tokenId) public view returns (
    string memory team,
    string memory category,
    uint256 initialPrice,
    string memory qrCode
)

// Vérification de l'unicité du QR code
function isQRCodeUsed(string memory qrCode) public view returns (bool)
```

**Sécurité** :
- ✅ Anti-duplication de QR codes
- ✅ Métadonnées immuables
- ✅ Propriété traçable

### 2. TicketMarketplace.sol

**Fonctionnalités** :
```solidity
// Lister un billet pour la vente
function listBilletForSale(
    uint256 tokenId,
    uint256 price
) public

// Acheter un billet
function buyBillet(uint256 tokenId) public

// Annuler une liste
function cancelListing(uint256 tokenId) public

// Récupérer l'historique des ventes
function getSalesHistory(uint256 tokenId) public view returns (
    SaleRecord[] memory
)
```

**Règles automatiques** :
- ✅ Prix maximum : 120% du prix initial
- ✅ Royalties : 5% pour l'organisateur
- ✅ Paiement en USDT uniquement
- ✅ Historique immuable on-chain

**Événements** :
```solidity
event TicketListed(uint256 tokenId, address seller, uint256 price);
event TicketSold(uint256 tokenId, address from, address to, uint256 price);
event ListingCanceled(uint256 tokenId, address seller);
```

## ✨ Avantages

### Pour les utilisateurs
- 🎯 **Authenticité garantie** : Fini les billets contrefaits
- 💰 **Prix équitables** : Protection contre la spéculation
- 🔐 **Sécurité maximale** : Transactions blockchain immuables
- 📱 **Expérience simple** : Interface intuitive, même sans expertise crypto
- 🌍 **Accessibilité globale** : Achetez depuis n'importe où

### Pour les organisateurs
- 💎 **Revenus récurrents** : 5% sur chaque revente
- 📊 **Visibilité totale** : Suivi du marché secondaire en temps réel
- 🛡 **Protection de la marque** : Contrôle des prix de revente
- 🤝 **Relation directe** : Connexion avec les fans
- 📈 **Analytics avancés** : Données comportementales des acheteurs

### Pour l'écosystème
- 🌱 **Marché transparent** : Toutes les transactions visibles
- ⚖️ **Équité** : Règles identiques pour tous
- 🔗 **Interopérabilité** : Compatible avec d'autres plateformes NFT
- 🌍 **Décentralisation** : Pas de point de défaillance unique

<div align="center">

**⚡ Fait avec passion pour le Mondial 2030 ⚽🌍**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

</div>
