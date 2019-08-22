Curso Hyperledger básico - Blockchain Academy
# Hyperledger-Básico

### Installation

A continuación están los comandos a ejecutar para una correcta instalación del BNA en nuestro ambiente local. Si reciben un error al crear la card para el admin de la red, es por que ya está creada. 

```sh
$ composer archive create -t dir -n . // Crear un archivo .bna
$ composer network install --card PeerAdmin@hlfv1 --archiveFile [Nombredelarchivocreado.bna]  // instalar el bna
$ composer network start --networkName [NombreRed] --networkVersion 0.0.1 --networkAdmin admin --networkAdminEnrollSecret adminpw --card PeerAdmin@hlfv1 --file networkadmin.card // Iniciar el BNA
$ composer card import --file networkadmin.card // Importar la credencial del admin network
$ composer network ping --card admin@[NombreRed] // Para revisar que la red esté operativa
```

### Iniciar Rest API

```sh
$ composer-rest-server  // Iniciar API rest
```
