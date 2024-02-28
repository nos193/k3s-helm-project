# k3s-helm-project

Bienvenue sur le repo du projet k3s-helm-project. Ce projet vise à déployer une stack LAMP et une application web Node.js en utilisant Helm sur k3s.

Ce projet est réalisé par Kilian ROSAK et MENOU Lucas

## Prérequis

### Installation de k3s

Ouvrez un terminal et exécutez la commande suivante pour installer k3s. Cette commande télécharge le script d'installation de k3s et l'exécute avec les privilèges de superutilisateur.

```bash
curl -sfL https://get.k3s.io | sh -
```

### Vérification de l'Installation

Après l'installation, vous pouvez vérifier que k3s fonctionne correctement en exécutant :

```bash
k3s kubectl get node
```

Cette commande devrait afficher le nœud de votre cluster k3s, indiquant que k3s est correctement installé et en cours d'exécution.

### Configuration de Kubectl pour utiliser k3s

kubectl est l'outil en ligne de commande pour interagir avec le cluster Kubernetes. k3s installe sa propre version de kubectl. Cependant, si vous souhaitez utiliser votre version existante de kubectl, vous devez configurer kubectl pour qu'il pointe vers le cluster k3s.

k3s stocke son fichier kubeconfig à /etc/rancher/k3s/k3s.yaml. Pour utiliser votre kubectl, vous devez configurer la variable d'environnement KUBECONFIG pour pointer vers ce fichier.

Vous pouvez le faire en ajoutant la commande suivante à votre fichier .bashrc, .zshrc, ou autre fichier de configuration de shell :

```bash
export KUBECONFIG=/etc/rancher/k3s/k3s.yaml
```

Après avoir ajouté cette ligne, rechargez votre configuration de shell avec la commande suivante (ou redémarrez votre terminal) :

```bash
source ~/.bashrc
```

Remplacez .bashrc par le fichier de configuration de votre shell si vous utilisez un shell différent.

## Démo du Projet

Pour exécuter la démo du projet, suivez les étapes ci-dessous:

1. Assurez-vous que vous avez k3s et Helm installés sur votre machine.
2. Clonez ce répertoire sur votre machine locale.
3. Ouvrez un terminal et naviguez jusqu'au répertoire cloné.
4. Exécutez `helm install my-lamp ./lamp-chart` pour déployer la stack LAMP.
5. Exécutez `helm install my-app ./nodejs-chart` pour déployer l'application web Node.js.
6. Utilisez `kubectl get services` pour trouver l'URL à laquelle l'application web est exposée et ouvrez-la dans votre navigateur.

Pour plus de détails sur notre approche, veuillez consulter le fichier `PLAN.md`.
