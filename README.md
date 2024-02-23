# k3s-helm-project

Bienvenue sur le répertoire du projet k3s-helm-project. Ce projet vise à déployer une stack LAMP et une application web Node.js en utilisant Helm sur k3s.

## Démo du Projet

Pour exécuter la démo du projet, suivez les étapes ci-dessous:

1. Assurez-vous que vous avez k3s et Helm installés sur votre machine. Si vous utilisez Minikube ou Kind, assurez-vous qu'ils sont configurés correctement.
2. Clonez ce répertoire sur votre machine locale.
3. Ouvrez un terminal et naviguez jusqu'au répertoire cloné.
4. Exécutez `helm install my-lamp ./charts/lamp` pour déployer la stack LAMP.
5. Exécutez `helm install my-app ./charts/myapp` pour déployer l'application web Node.js.
6. Utilisez `kubectl get services` pour trouver l'URL à laquelle l'application web est exposée et ouvrez-la dans votre navigateur.

Pour plus de détails sur notre approche, veuillez consulter le fichier `PLAN.md`.

