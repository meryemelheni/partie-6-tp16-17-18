# Synthèse TP18 : Comparaison des solutions de gestion de secrets

| Critère | Secret Kubernetes | Sealed Secrets | Vault + ESO |
| :--- | :--- | :--- | :--- |
| **Versionnable dans Git** | Non (base64 lisible) | **Oui** (chiffré) | Oui (les manifests ESO, pas les secrets) |
| **Source de vérité** | Le cluster (etcd) | Git (le fichier chiffré) | **Vault** |
| **Rotation** | Manuelle (redéploiement) | Manuelle (nouveau fichier + apply) | **Automatique** (via ESO) |
| **Audit des accès** | Via Kubernetes (RBAC) | Limité (contrôleur) | **Excellent** (audit Vault) |
| **Complexité d'exploitation** | Faible | Moyenne | **Élevée** (Vault à maintenir) |
| **Adapté à GitOps** | Non | **Oui** | Oui (via ESO) |
