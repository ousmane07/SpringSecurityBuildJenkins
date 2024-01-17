
# Explications

Tout d'abord on a crée un simple projet Spring boot dans lequel on va créer des fichiers : Dockerfile, docker-compose.yml, first-command.sh et jenkinsfile

Voici les captures respectives de ces fichiers

Dockerfile : 
![Capture 1](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/dockerfile.png?raw=true)

docker-compose.yml :  
![Capture 2](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/dok-comp.png?raw=true)

first-command.sh : 

![Capture 3](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/first-command.png?raw=true)

jenkinsfile:

![Capture 4](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/jenkinsfile.png?raw=true)

Ensuite sur le terminal, on s'est pointé dans le projet puis on a lancé la commande : docker-compose up -d pour executer le fichier docker-compose.yml en mode démo

![Capture 5](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/1.png?raw=true)

Là on voit que le network, les volumes et les containers ont bien été créé

![Capture 6](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/2.png?raw=true)

On tape la commande docker ps pour pouvoir récupérer l'ID du container jenkins-devops...
On copie cet ID puis on tape la commande : docker logs IDCOPIé...
On aura ce mot de passe qui a été généré pour l'administration de jenkins...
![Capture 7](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/4.png?raw=true)

Voici l'interface de la page d'administration de Jenkins une fois qu'on s'est connecté en tant qu'administrateur
![Capture 8](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/5.png?raw=true)
On créé une nouvelle pipeline dans laquelle on va mettre notre lien Github...
Sachant qu'on a fait les configurations de maven au préalable
![Capture 9](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/6.png?raw=true)
Sur la partie ScriptPath, on renseigne notre fichier jenkinsfile
![Capture 10](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/7.png?raw=true)
Puis on lance le build
Voici le résultat obtenu au niveau de la console:
![Capture 11](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/8.png?raw=true)
![Capture 12](https://github.com/ousmane07/SpringSecurityBuildJenkins/blob/master/captures/9.png?raw=true)






