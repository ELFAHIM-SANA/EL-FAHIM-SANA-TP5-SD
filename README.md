-------------------------------------Rapport-----------------------------------

Tout d'abord, nous avons créé un projet Java avec IntelliJ. Dans le répertoire Java,
nous avons créé le package ws, dans lequel nous avons défini deux classes : 
la classe Compte

![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/f33bc53a-d3b8-4c51-9fd1-75e8301fc1f9)

![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/5c1127e0-dc54-4323-8a2f-7872c5a130f4)


et la classe BanqueService.
Dans la classe BanqueService, nous avons créé les méthodes suivantes :

• Convertir un montant de l’euro en DH , Consulter un Compte, Consulter une Liste de comptes.


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/d0bc405a-860a-4e4c-973f-44e0070e915a)


Déployement du Web service avec un simple Serveur JaxWS :

![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/25b188a5-93db-4714-bd90-4f2ab7a38ab7)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/30760516-c521-4660-ad3a-6bd9283c155d)


Consultation et analyse de WSDL avec un Browser HTTP :


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/450d126f-b5b6-4f6e-8dd2-1dfdce47c73a)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/ac7bf226-fa07-40ff-acea-b75c85085eb3)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/7f03b286-27b7-49c5-9c3e-6ce2cec97fa2)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/7c36e7c9-a700-4a25-9195-6303cbe2d41c)


Ce fichier XML est une définition WSDL (Web Services Description Language) pour le service web "BanqueWS".
Voici une analyse en bref des principaux composants de ce fichier :

En-tête et Métadonnées :

Le fichier est généré par XML-WS Runtime version 4.0.2.

Il utilise plusieurs espaces de noms (namespaces) pour la sécurité, les politiques web, l'adressage, le schéma XML, et les spécifications WSDL.

Types :

Définit un schéma XML (xsd:schema) qui importe un autre schéma situé à http://localhost:9090/?xsd=1.
Messages :

getCompte et getCompteResponse: Messages pour l'opération de récupération d'un compte.

listComptes et listComptesResponse: Messages pour l'opération de liste des comptes.

ConversionEuroToDH et ConversionEuroToDHResponse: Messages pour l'opération de conversion de l'euro au dirham.

PortType :

BanqueService: Définit trois opérations disponibles sur le service :

getCompte: Récupération d'un compte.

listComptes: Liste des comptes.

ConversionEuroToDH: Conversion de l'euro au dirham.

Chaque opération a des messages d'entrée et de sortie définis.

Binding :

BanqueServicePortBinding: Spécifie comment les opérations du service sont liées au protocole SOAP.

Utilise le transport HTTP pour SOAP.

Chaque opération utilise un style "document" et un "literal" encoding pour les messages.

Service :

BanqueWS: Définit le service web.

BanqueServicePort: Définit le port du service, qui est lié à BanqueServicePortBinding.

L'adresse du service est http://localhost:9090/.

Teste des opérations du web service avec un outil comme SoapUI ou Oxygen :

Après avoir installé l'outil SoapUI, nous avons créé un projet pour tester les opérations conversionEuroToDH avec différentes valeurs de montants, 
ainsi que l'opération getCompte en fournissant des valeurs pour le code. Nous avons également consulté la liste des comptes.


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/3ec45621-2c2a-4d66-9c2c-e2c7631544ef)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/adc23429-eae9-4c89-b6ca-c368da0bec75)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/6b76dbd2-463f-4e33-9f82-dc0add7df250)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/ee315e92-8280-4640-953b-993b1b561378)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/66ef75f1-d916-4556-8323-6c5113fd07a7)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/35294e0a-95d1-4825-8855-bd66c26b8865)


Créer un Client SOAP Java :

Générer le Stub à partir du WSDL :

Dans le projet, nous avons créé un module intitulé : client-soap-java :


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/757b67e1-57fa-41fc-9dbb-42010ae9115a)


Génération du proxy :


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/dc1639e1-1f25-4859-94be-12ffbc2c94ca)


Créer un client SOAP pour le web service


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/ab0f318c-9542-4e59-9486-7b33612f65b7)


![image](https://github.com/ELFAHIM-SANA/EL-FAHIM-SANA-TP5-SD/assets/131165163/64e3f7ed-d865-4421-99c6-b10b578fcf2b)












