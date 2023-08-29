# DHCP

  **installation de Windows Server sur la machine virtuelle**                                                                             
- Assurez-vous d'avoir un (snapshot) de votre machine virtuelle avant de commencer la configuration, au cas où quelque chose tournerait mal.                                       

  **Configuration de la carte réseau en réseau interne**
- Ouvrez les paramètres de la machine virtuelle et allez dans la configuration réseau.
- Configurez la carte réseau en mode "Réseau Interne" pour isoler le réseau.

  **Configuration du service et des plages DHCP**

- Ouvrez le "Gestionnaire de serveur" sur le serveur Windows.

  ![gestionnaire serveur](https://github.com/omaymaaboumoussa/DHCP/assets/137881447/f17c6222-c779-4dac-aee2-0c381fadcade)


- sélectionnez "Gérer" dans le coin supérieur droit, puis choisissez "Ajouter des rôles et fonctionnalités".
- Suivez l'assistant d'installation des rôles et fonctionnalités. Sélectionnez "Serveur DHCP" dans la liste des rôles disponibles et installez-le.
- ouvrez "Outils d'administration" et sélectionnez "DHCP"
- cliquez avec le bouton droit sur "Attributs étendus".
- il faut spécifier l'adresse IP 172.20.0.10.
-  Dans la console DHCP il faut cliquer avec le bouton droit sur "Nouvelle étendue".
-  Il faut donner un nom a l'étendue, moi j'ai mis "DHCP", et définisser la plage d'adresses IP de 172.20.0.100 à 172.20.0.200.
  
 ![plages d'adresse](https://github.com/omaymaaboumoussa/DHCP/assets/137881447/498bbd7d-20e1-4faa-95c3-d62f0e0ec343)

 **Un client qui rejoint le réseau obtient une adresse IP dans la plage donnée par le DHCP**
 - Configurez la carte réseau client en mode "Réseau Interne"
 - ouvrir un terminal et verifiez si le client obtient une adresse IP dans la plage 172.20.0.100 - 172.20.0.200 ( oui, on a 169.254.23.0
   
   
 ![client](https://github.com/omaymaaboumoussa/DHCP/assets/137881447/df358e93-dd6d-47f6-aada-b486ee63f47f)

 - Dans la liste des "Adresses réservées", cliquez avec le bouton droit et sélectionnez "Nouvelle réservation".

 - Spécifiez un nom pour la réservation, par exemple, "Client windows 10", puis entrez l'adresse MAC de la machine cliente que vous avez récupérez a l'aide du terminal avec la commande(ipconfig /All) et c'est l'adresse physique.

   
   ![adresse physique](https://github.com/omaymaaboumoussa/DHCP/assets/137881447/b2d67ee7-44e4-4260-a505-0188548564d9)
   
   ![reservation](https://github.com/omaymaaboumoussa/DHCP/assets/137881447/80611c73-7f63-4bf9-8f5e-e94eadbb758a)














