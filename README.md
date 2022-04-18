# Recupera-Thor
Batterie parametrable evolutive pour elements li-ion de récuperation

Voila une idée qui me trote depuisun moment dans la tete

le but est de faire une battrie pouvant sortire une tension parametrabe avec des element de recuperation (batterie de vieux pc,aspirateur,battrie secour de telephone)
le microcontroleur poura  reconfigurer les branchement des element via le bus i2c (serie //) et recuperera les information de chaque element pour les envoyer
via une interface RG2,a un moniteur quelconque

elle poura egalement charger independament chaque element et tester son niveau de charge(en miliampere) pour savoir comment reconfigurer les branchement en
cas d'element défectueux, une led s alumera alor pour indiquer quel element est foutu et clignotera pour indiquer quel element dois etre changer.

il est egalement prévu de faire un port d extension pour rajouter des fonctionalitéé (wifi,bluethoot out tout autre idée)

C est un projet que je ne  sens pas de réaliser seul car je n ai pour l instant, ni les capacité, ni le temps pour réaliser la totalité de ce projet 
jusqua son terme.

je le laisse donc la dans les couloire d internet sous la bienveillance du grand Git en atendant de rencontrer des aventuriers interessé par Recupera-Thor

alor si cette aventure vous interesse ou si vous conaisser d autres projets similaire n'hesité pas a me contacter

Linux soit avec vous

OgmaDragno

Liste des composant Possiblement utilisé
-STC3100 Moniteur de batterie i²c https://www.farnell.com/datasheets/1690441.pdf (Trouver un autre circuit car celui ci a une adresse unique)
-AP9101C Protecteur de batterie   https://4donline.ihs.com/images/VipMasterIC/IC/DIOD/DIOD-S-A0007229744/DIOD-S-A0007229744-1.pdf?hkey=6D3A4C79FDBF58556ACFDE234799DDF0

![Schema simplifié](https://user-images.githubusercontent.com/80761004/162025851-89bb9339-a26e-488d-9d7f-797600614c27.jpg)
![Schema simplifié_P2](https://user-images.githubusercontent.com/80761004/162025866-c2effa08-0e3d-4671-84cc-094f17a46043.jpg)
