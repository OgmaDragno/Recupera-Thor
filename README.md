# Recupera-Thor
Batterie parametrable evolutive pour elements li-ion de récuperation

Voila une idée qui me trote depuisun moment dans la tete

le but est de faire une battrie pouvant sortire une tension parametrabe avec des element de recuperation (batterie de vieux pc,aspirateur,battrie secour de telephone)
le microcontroleur poura  reconfigurer les branchement des element via le bus i2c (serie //) et recuperera les information de chaque element pour les envoyer
via une interface RJ45,a un moniteur quelconque

elle poura egalement charger independament chaque element et tester son niveau de charge(en miliampere) pour savoir comment reconfigurer les branchement en
cas d'element défectueux, une led s alumera alor pour indiquer quel element est foutu et clignotera pour indiquer quel element dois etre changer.

il est egalement prévu de faire un port d extension pour rajouter des fonctionalitéé (wifi,bluethoot out tout autre idée)

C est un projet que je ne  sens pas de réaliser seul car je n ai pour l instant, ni les capacité, ni le temps pour réaliser la totalité de ce projet 
jusqua son terme.

je le laisse donc la dans les couloire d internet sous la bienveillance du grand Git en atendant de rencontrer des aventuriers interessé par Recupera-Thor

alor si cette aventure vous interesse ou si vous conaisser d autres projets similaire n'hesité pas a me contacter

Linux soit avec vous

OgmaDragno

________REFLEXION_______

<Comunication entre battrie>:
-Plutot que de devoir parametrer deux module rj45 en entrée eten sortie ce qui me parais tres complexe. Ou devoire utiliser un "routeur?" dans le cas ou il n y aurrais qu une seul connecteur en sortie.
Je penche sur une idée de deux port serie (in/out) qui echangeron les information selon un model adressable et faire un module extene dedié uniquement au traitement et emission de donnée ethernet via un RJ45
chaque batterie sera brancher en serie via deux liaion (tx(in-out)/rx(in-out))
a l initialisation elle verifiron si elle sont brancher en out.ainsi la derniere batterie saura qu elle est la  dernier et elle pouront s auto attribuer un numero d identification



Liste des composant Possiblement utilisé
-STC3100 Moniteur de batterie i²c 
https://www.farnell.com/datasheets/1690441.pdf (Trouver un autre circuit car celui ci a une adresse unique)
-bq27742-g1 Interessant car integre une gestion de charge mais egalement en adresse unique
https://www.ti.com/lit/ds/symlink/bq27742-g1.pdf?HQS=dis-mous-null-mousermode-dsf-pf-null-wwe&ts=1650902664515&ref_url=https%253A%252F%252Fbr.mouser.com%252F

-AP9101C Protecteur de batterie   
https://4donline.ihs.com/images/VipMasterIC/IC/DIOD/DIOD-S-A0007229744/DIOD-S-A0007229744-1.pdf?hkey=6D3A4C79FDBF58556ACFDE234799DDF0

-PCF8574 Pour l instant je n ai pas trouver les switch i²c donc j opte pour un expensseur I/O i²c couplé a des mosfet
https://www.farnell.com/datasheets/1716973.pdf

-TCA9548APWR Pour la gestion des elements , limite donc une cellule a 8 element et 8 cellules par batterie donc maximum 48 element
             L'on pourais maximiser lenombre d element par battrie en trouvant un CI moniteur de battrie avec une adresse configurable
https://www.ti.com/lit/ds/symlink/tca9548a.pdf?HQS=dis-dk-null-digikeymode-dsf-pf-null-wwe&ts=1650330594627&ref_url=https%253A%252F%252Fwww.ti.com%252Fgeneral%252Fdocs%252Fsuppproductinfo.tsp%253FdistId%253D10%2526gotoUrl%253Dhttps%253A%252F%252Fwww.ti.com%252Flit%252Fgpn%252Ftca9548a

![Schema simplifié](https://user-images.githubusercontent.com/80761004/162025851-89bb9339-a26e-488d-9d7f-797600614c27.jpg)
![Schema simplifié_P2](https://user-images.githubusercontent.com/80761004/162025866-c2effa08-0e3d-4671-84cc-094f17a46043.jpg)
