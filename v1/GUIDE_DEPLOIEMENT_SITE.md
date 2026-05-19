# 🚀 Guide de déploiement — Site Gardère Logistique

## ✅ Contenu livré

Le site web complet contient **9 pages** + styles + logo :

| # | Fichier | Contenu |
|---|---|---|
| 1 | `index.html` | Page d'accueil |
| 2 | `a-propos.html` | À propos / Histoire |
| 3 | `services.html` | Services détaillés |
| 4 | `zones-desservies.html` | Québec, Ontario, Nouvelle-Écosse |
| 5 | `carrieres.html` | Page Carrières |
| 6 | `chauffeur-livreur-halifax.html` | **Offre de poste détaillée** (Schema.org JobPosting) |
| 7 | `contact.html` | Formulaire + coordonnées |
| 8 | `mentions-legales.html` | Mentions légales |
| 9 | `politique-confidentialite.html` | Conformité Loi 25 + LPRPDE |
| - | `styles.css` | Feuille de style partagée |
| - | `images/logo.png` | Logo de l'entreprise |

---

## 🌐 Déploiement sur Netlify (recommandé — GRATUIT)

### Méthode 1 — Drag & Drop (la plus simple, 2 minutes)

1. **Aller sur** https://app.netlify.com/drop
2. **Glisser le dossier `gardere-site/` au complet** dans la zone de drop (ou le ZIP)
3. Netlify génère automatiquement une URL temporaire (ex: `random-name-12345.netlify.app`)
4. **Cliquer sur "Domain settings"** pour ajouter `gardere-logistique.com` :
   - Cliquer "Add custom domain"
   - Entrer `gardere-logistique.com`
   - Suivre les instructions DNS

### Méthode 2 — Connexion DNS chez OVH

Une fois le site déployé sur Netlify, configurer le domaine OVH :

1. Aller dans **OVH Manager → Domaines → gardere-logistique.com**
2. Onglet **"Serveurs DNS"** → choisir "Modifier les serveurs DNS"
3. Remplacer les serveurs OVH par ceux de Netlify :
   - `dns1.p01.nsone.net`
   - `dns2.p01.nsone.net`
   - `dns3.p01.nsone.net`
   - `dns4.p01.nsone.net`
4. Sauvegarder. Délai de propagation : 1 à 24h.

OU plus simple : créer un **enregistrement CNAME** dans la zone DNS OVH :
- Type : `CNAME`
- Sous-domaine : `www`
- Cible : `votre-site.netlify.app`

---

## ⚠️ Notes importantes

### Formulaire de contact
Le formulaire utilise actuellement `mailto:` (ouvre le client de messagerie). Pour qu'il fonctionne directement sur le site :

**Option simple (Netlify Forms gratuit) :**
Modifier le formulaire dans `contact.html` :
```html
<form name="contact" method="POST" data-netlify="true">
```
Netlify gérera automatiquement les soumissions et les enverra à votre courriel.

### SSL / HTTPS
Netlify active automatiquement le certificat SSL (https://) gratuitement via Let's Encrypt une fois le domaine connecté.

---

## 🎯 Pour le dossier EIMT

Le site est conçu pour **renforcer la légitimité** auprès de Service Canada :

- ✅ **Adresse complète, téléphone, courriel** visibles partout
- ✅ **NEQ 1174723552** dans le pied de page de chaque page
- ✅ **Mentions légales** complètes (raison sociale 9401-7746 Québec Inc.)
- ✅ **Politique de confidentialité** conforme Loi 25 + LPRPDE
- ✅ **Schema.org JobPosting** sur la page du poste (Google for Jobs)
- ✅ **Schema.org LocalBusiness** sur la page d'accueil
- ✅ Cohérence avec l'affichage Guichet-Emplois (mêmes exigences, mêmes tâches, même salaire 36$/h)
- ✅ Narrative d'entreprise stable et crédible (fondée 2019, expansion progressive)

**Avant le dépôt EIMT (semaine du 16 juin), le site DOIT être actif** sur `gardere-logistique.com` pour que Service Canada puisse le consulter.

---

## 🔧 Modifications futures

Si vous souhaitez modifier du contenu :
- Ouvrir le fichier `.html` correspondant dans un éditeur (VS Code, Sublime, Notepad++)
- Modifier le texte directement (le code HTML est commenté pour vous guider)
- Redéployer sur Netlify (drag & drop du nouveau dossier)

Tout le design est centralisé dans `styles.css` — pour changer une couleur :
- Chercher `--color-accent` (orange cuivré)
- Chercher `--color-bg` (bleu marine)

---

## 📞 Coordonnées présentes partout sur le site

- **Téléphone :** 514-754-9012
- **Courriel :** info@gardere-logistique.com
- **Adresse :** 5484 avenue Notre-Dame-de-Grâce, Montréal (Québec) H4A 1L4
- **NEQ :** 1174723552
- **Raison sociale :** 9401-7746 Québec Inc.
- **Président :** Charles-Edouard Gardère

---

*Site créé le 18 mai 2026 · Gardère Logistique*
