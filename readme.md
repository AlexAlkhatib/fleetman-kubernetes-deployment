# 🚚 **4KUBE — Déploiement Kubernetes de Fleetman**

**4KUBE : Fleetman** est un mini-projet DevOps visant à déployer une application distribuée de **suivi de flotte de véhicules en temps réel** sur un cluster Kubernetes.
Ce projet démontre ma capacité à orchestrer des conteneurs Docker, à créer un cluster Kubernetes fonctionnel et à assurer la **scalabilité**, la **résilience** et la **fiabilité** d’une application distribuée.

Ce travail a été réalisé dans un **cadre personnel** pour renforcer mes compétences Cloud / DevOps.


## 🎯 Objectifs du projet

* Comprendre en profondeur le fonctionnement de Kubernetes
* Déployer une architecture multi-services à l’aide de manifests Kubernetes
* Gérer des applications distribuées (front/webapp, queue, position simulator…)
* Assurer la scalabilité et la haute disponibilité via l’orchestration
* Manipuler Docker, kubectl, services, pods, déploiements, ConfigMaps, etc.
* Reproduire un cas concret d’architecture microservices


## 📦 Contenu du dépôt

```
projet-kubernetes/
 ├── docker/                  # Contient le fichier compose.yaml original
 ├── kubernetes/              # Manifestes Kubernetes (deployments, services…)
 ├── Montage cluster Kubernetes.pdf   # Documentation : création du cluster étape par étape
 └── README.md
```


## 🚀 Déployer le projet Kubernetes

### ✅ **Pré-requis**

* Docker Desktop avec Kubernetes activé
* `kubectl` installé et configuré
* Un poste local capable d’exécuter un cluster Kubernetes embarqué (local k8s de Docker Desktop)


### ▶️ **Lancement du cluster**

1. **Démarrer Docker Desktop**

2. **Appliquer tous les manifestes Kubernetes**

   ```bash
   kubectl apply -f kubernetes/
   ```

3. **Accéder à l’application**

   * Dans un navigateur, ouvrir :
     **[http://localhost:80](http://localhost:80)**


### ❗ Si l’application ne s’affiche pas

Il est possible que l’adresse locale varie.
Vérifier le service exposé :

```bash
kubectl get services
```

Rechercher :

* **fleetman-webapp**
* de type **LoadBalancer**

Récupérer la valeur **EXTERNAL-IP**, puis accéder à :

```
http://EXTERNAL-IP:80
```


## 🧰 Technologies utilisées

* **Kubernetes** : orchestration, déploiements, services, LoadBalancer
* **Docker** : conteneurisation des services Fleetman
* **kubectl** : gestion du cluster
* **Architecture microservices** : webapp, position simulator, queue, API…
* **LoadBalancer / Services / Deployments / ReplicaSets**


## 🧠 Compétences démontrées

- ✔ Mise en place d’un cluster Kubernetes complet
- ✔ Déploiement d’une application distribuée multi-conteneurs
- ✔ Utilisation avancée de manifests Kubernetes (YAML)
- ✔ Compréhension des services : ClusterIP, LoadBalancer
- ✔ Scalabilité via ReplicaSets et Deployments
- ✔ Gestion des ressources locales (ingress, nodes, pods…)
- ✔ Troubleshooting (kubectl logs, describe, get…)
- ✔ Capacité à transformer un docker-compose en architecture Kubernetes


## 📄 Documentation technique

Le fichier :
**Montage cluster Kubernetes.pdf**
explique étape par étape :

* la création du cluster Kubernetes
* la configuration de kubectl
* les tests initiaux
* le déploiement des ressources Fleetman
* la validation du fonctionnement


## 🔧 Améliorations possibles

* Ajouter des dashboards de monitoring (Prometheus / Grafana)
* Intégrer un pipeline CI/CD (GitHub Actions)
* Ajouter un Ingress Controller (NGINX)
* Sécuriser le cluster (RBAC, Network Policies)
* Déployer sur un cluster cloud (GKE, AKS, EKS, k3s)
* Ajouter de l’auto-scaling (HPA)


## 👤 À propos

Développeur et apprenant passionné par le **Cloud**, **Kubernetes**, et l’**écosystème DevOps**.
Je réalise ce type de projets personnels pour renforcer mes compétences et me préparer au contexte professionnel.

GitHub : [github.com/AlexAlkhatib](https://github.com/AlexAlkhatib)


## 📄 Licence

MIT License  Copyright (c) 2025 Alex Alkhatib  
