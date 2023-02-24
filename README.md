[![1](https://github.com/rozoandrescamilo/Smart-Contract-para-consultar-estados-de-una-Purchase-Order/blob/main/img/1.jpg?raw=true "1")](https://github.com/Smart-Contract-para-consultar-estados-de-una-Purchase-Order/blob/main/img/1.jpg?raw=true "1")

- [Consultar parámetros de un smart contract desde API de Kaleido](#consultar-parámetros-de-un-smart-contract-desde-api-de-kaleido)
  - [Despliege de smart contract en la API](#despliege-de-smart-contract-en-la-api)
    - [Crear una nueva red](#crear-una-nueva-red)
    - [Crear un nuevo entorno de trabajo](#crear-un-nuevo-entorno-de-trabajo)
    - [Crear un nuevo SuperNodo](#crear-un-nuevo-supernodo)
    - [Crear un nueva App](#crear-un-nueva-app)
    - [Compilación y despliegue de contrato](#compilación-y-despliegue-de-contrato)
  - [Métodos para consultar parámetros del contrato](#métodos-para-consultar-parámetros-del-contrato)
    - [Por medio de REST API Gateway ](#por-medio-de-rest-api-gateway)
    - [Conexión por Javascript y biblioteca Web3.js](#conexión-por-javascript-y-biblioteca-web3.js)


# Consultar parámetros de un smart contract desde API de Kaleido

## Despliege de smart contract en la API

### Crear una nueva red

Como requisito es necesario tener una cuenta en la Página oficial de la consola de Kaleido: [https://console.kaleido.io/login](https://console.kaleido.io/login "https://console.kaleido.io/login")

Como inicio se crea nueva red o consorcio, que permite construir la red blockchain. se proporciona un nombre para la red comercial y una misión describiendo el proposito de esta.

[![1](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/1.png?raw=true "1")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/1.png?raw=true "1")

Luego seleccionar una región para conectar con los servicios en la nube, donde los proveedores son AWS y Azure.

[![2](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/2.png?raw=true "2")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/2.png?raw=true "2")

### Crear un nuevo entorno de trabajo

Se requiere crear un nuevo entorno de trabajo y se selecciona el Servicio de cadena de bloques estándar + Supernodo FireFly, Implemente FireFly SuperNodes para web3 además de nuestro servicio de cadena de bloques estándar. Hyperledger FireFly SuperNodes es un enfoque de próxima generación para web3, que proporciona una pila completa para que las empresas construyan y escalen aplicaciones web3 seguras.

[![3](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/3.png?raw=true "3")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/3.png?raw=true "3")

Dentro de los posibles protocolos blockchain para el entorno de trabajo se selecciona la red de Ethereum. 

[![4](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/4.png?raw=true "4")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/4.png?raw=true "4")

Se agregan los detalles del nuevo entorno de trabajo y el despliegue solo en la nube del proveedor que se selccionó.

[![5](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/5.png?raw=true "5")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/5.png?raw=true "5")

A continuación, se elije su cliente Ethereum blockchain y un algoritmo asociado. Las opciones son Geth / PoA, Quorum / IBFT, Quorum / Raft, Besu / PoA y Besu / IBFT. Se recomienda una configuración simple de Geth / PoA.

[![6](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/6.png?raw=true "6")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/6.png?raw=true "6")

### Crear un nuevo SuperNodo

Hacer clic en el botón CREAR SUPERNODO para comenzar a configurar el FireFly Supernode.

[![7](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/7.png?raw=true "7")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/7.png?raw=true "7")

Se elije un nombre y membresía para el nodo. La membresía predeterminada está disponible para su uso en esta etapa. Por defecto se selecciona los entornos de tokens ERC20_ERC721.

[![8](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/8.png?raw=true "8")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/8.png?raw=true "8")

Se asignará el nodo FireFly a un nodo blockchain nuevo o existente y un tiempo de ejecución ipfs nuevo o existente. Dado el contexto de este inicio rápido, se creara un nuevo elemento para cada uno.

[![9](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/9.png?raw=true "9")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/9.png?raw=true "9")

Actualmente solo están disponibles nodos FireFly de pequeño tamaño para la membresia gratuita, pero para membresia empresarial se podrá pedir mas tamaño.

[![10](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/10.png?raw=true "10")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/10.png?raw=true "10")

Detrás de escena, Kaleido te está generando un espacio de nombres de aplicaciones, compilar el contrato inteligente central de FireFly (ya que FireFly requiere un contrato inteligente implementado para sincronizar la actividad con la cadena) y promover la fuente en su entorno FireFly recién creado.

Si el nodo FireFly se inicializa correctamente, verá una pantalla de descripción general del entorno con todos los tiempos de ejecución en un estado Iniciado.

[![11](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/11.png?raw=true "11")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/11.png?raw=true "11")

[![12](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/12.png?raw=true "12")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/12.png?raw=true "12")

[![13](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/13.png?raw=true "13")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/13.png?raw=true "13")

### Crear un nueva App

Para la gestión de contratos empresariales de Kaleido es necesario crear una aplicación. Las aplicaciones Kaleido ayudan a administrar la lógica comercial compartida en la red descentralizada.

Contiene versiones de los contratos inteligentes, permite que los participantes de la red rastreen esas compilaciones hasta el código fuente original, versiones y aprobaciones.

[![14](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/14.png?raw=true "14")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/14.png?raw=true "14")

Dentro de los posibles protocolos blockchain para la aplicación se selecciona la red de Ethereum. 

[![15](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/15.png?raw=true "15")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/15.png?raw=true "15")

Agregue detalles de la aplicación especificando un nombre e indicando dónde se encuentra el código fuente de este proyecto. Para este caso se usa n contrato inteligente en un repositorio de Github.

[![16](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/16.png?raw=true "16")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/16.png?raw=true "16")

```solidity
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

// Declara un nuevo contrato
contract SimpleStorage {
    // Storage Persiste entre transacciones
    uint256 x;

    // Permite cambiar el entero sin signo almacenado
    function set(uint256 newValue) public {
        x = newValue;
        emit Changed(msg.sender, newValue);
    }

    // Devuelve el entero sin signo almacenado actualmente
    function get() public view returns (uint256) {
        return x;
    }

    event Changed(address indexed from, uint256 value);
}

```

Una vez creada la aplicación se debe dar clic en el boton de CREAR NUEVA VERSIÓN para agregar los parametros del contrato a gestionar.

[![17](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/17.png?raw=true "17")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/17.png?raw=true "17")

### Compilación y despliegue de contrato

A continuación, se deben ingresar los detalles del proyecto como nombre, versión, la URL del repositorio de Github donde se encuentra el contrato inteligente y la versión del compilador de la EVM - Ethereum Virtual Machine.

[![18](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/18.png?raw=true "18")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/18.png?raw=true "18")

Una vez finalizado el ingreso de detalles se mostrará los parametros de la versión y el contrato debe pasar de status **Compiling** a **Compiled** para poder continuar.

[![19](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/19.png?raw=true "19")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/19.png?raw=true "19")

[![20](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/20.png?raw=true "20")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/20.png?raw=true "20")

Compilado el contrato, el siguiente paso es promocionar el contrato en el entorno ya creado Blockchain Development. Esto instalará la API de Gateway en cada nodo del entorno. Luego, puede usar la API de Gateway en cualquiera de los nodos para implementar nuevas instancias de este contrato, así como enviar transacciones en instancias existentes. 

[![21](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/21.png?raw=true "21")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/21.png?raw=true "21")

[![22](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/22.png?raw=true "22")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/22.png?raw=true "22")

Después de ser promovido se mostrará detalles del Smart Contract donde se podran realizar varias actividades con API GATEWAY:

- Crear una API de puerta de enlace: crea una consola swagger dinámica y una especificación descargable para la interacción RESTful con métodos de contrato inteligente.

- Implementar contratos: use la API de Gateway para implementar su contrato inteligente mediante programación o directamente a través de la consola.

- Enviar transacciones: Aproveche la API para interactuar con contratos inteligentes en cadena existentes al pasar la dirección del contrato como parámetro en la llamada.

## Métodos para consultar parámetros del contrato

### Por medio de REST API Gateway 

Se tiene en cuenta la documentación oficial de Gateway de API REST Kaleido: [https://api.kaleido.io/ethconnect.html](https://api.kaleido.io/ethconnect.html "https://api.kaleido.io/ethconnect.html") 

En la anterior sección de detalles del Smart Contract se encuentra el primer método para consultar parámetros usando la interfaz REST API dando clic en el boton VIEW GATEWAY API.

Se abrirá la definición REST API donde se selecciona el nodo que se usará para interactuar con la instancia, se selecciona la opción de Desplegar Contrato  y dar clic en el boton VIEW API.

[![23](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/23.png?raw=true "23")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/23.png?raw=true "23")

La interfaz de usuario Swagger incorporada se despliega y se pueden visualizar los servicios web de acceso y gestión de datos de organizaciones y proyectos a través de REST APIs.

En el **POST/constructor()** se debe agregar el archivo ABI de la compilación del contrato y hacer clic en EJECUTAR.

[![24](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/24.png?raw=true "24")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/24.png?raw=true "24")

Modelo de archivo ABI compilado:

```javascript

{
	"input": {
	  "abi": [
		{
		  "anonymous": false,
		  "inputs": [
			{
			  "indexed": true,
			  "internalType": "address",
			  "name": "from",
			  "type": "address"
			},
			{
			  "indexed": false,
			  "internalType": "uint256",
			  "name": "value",
			  "type": "uint256"
			}
		  ],
		  "name": "Changed",
		  "type": "event"
		},
		{
		  "inputs": [],
		  "name": "get",
		  "outputs": [
			{
			  "internalType": "uint256",
			  "name": "",
			  "type": "uint256"
			}
		  ],
		  "stateMutability": "view",
		  "type": "function"
		},
		{
		  "inputs": [
			{
			  "internalType": "uint256",
			  "name": "newValue",
			  "type": "uint256"
			}
		  ],
		  "name": "set",
		  "outputs": [],
		  "stateMutability": "nonpayable",
		  "type": "function"
		}
	  ]

	}
}

```

[![25](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/25.png?raw=true "25")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/25.png?raw=true "25")

En la sección de Respuesta del servidor se genera un archivo JSON donde se obtiene los principales ss del despliegue del contrato de prueba simplestorage. 

[![26](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/26.png?raw=true "26")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/26.png?raw=true "26")

Respuesta del servidor:

```javascript

{
  "headers": {
    "id": "baaba175-f54f-4a7d-6e54-b5f3d310d413",
    "type": "TransactionSuccess",
    "ctx": {
      "isRemoteRegistry": true
    },
    "timeReceived": "2023-02-24T06:46:08.060494642Z",
    "timeElapsed": 4.849915391,
    "requestOffset": "",
    "requestId": "bf78d613-0977-4616-45a4-a6b47bd4e636",
    "requestABIId": "0c4c62bb-d864-4ed1-4a61-6d2e3065bd30"
  },
  "blockHash": "0x66114113902ee96bab3b9f679c0cb5d6c91d7cdf78030ce7eda99b0401e67195",
  "blockNumber": "62920",
  "openapi": "https://u1my9uxwbm-u1bzt3mvmy-connect.us1-azure.kaleido.io/instances/d9cf87366ee9075d933dc562d4c5d0a6d8b0c580?openapi",
  "apiexerciser": "https://u1my9uxwbm-u1bzt3mvmy-connect.us1-azure.kaleido.io/instances/d9cf87366ee9075d933dc562d4c5d0a6d8b0c580?ui",
  "contractAddress": "0xd9cf87366ee9075d933dc562d4c5d0a6d8b0c580",
  "cumulativeGasUsed": "142597",
  "from": "0xf0afc19d9108b443096f0de4d461093b106b3bcd",
  "gasUsed": "142597",
  "nonce": "0",
  "status": "1",
  "to": null,
  "transactionHash": "0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba",
  "transactionIndex": "0"
}

```
De este método se puede obtener datos clave que le pueden ser de interés al usuario a lo largo de todo el flujo del proceso en la gestión de datos. Algunos de los términos relevantes en la respuesta incluyen:

- **contractAddress:** se refiere a la dirección del contrato inteligente utilizado en la transacción.

- **gasUsed y cumulativeGasUsed:** se refieren a la cantidad de gas utilizada en la transacción. El gas es una unidad de medida utilizada en Ethereum (la plataforma blockchain en la que se basa Kaleido) para calcular el costo de las transacciones.

- **transactionHash:** se refiere al hash único de la transacción en la cadena de bloques.

- **blockHash":** hace referencia al algoritmo que representa la dirección del bloque utilizado en la transacción.

- **"blockNumber":** número del bloque utilizado en la transacción.

### Conexión por Javascript y biblioteca Web3.js

Se puede conectar con un contrato inteligente a través de JavaScript usando una biblioteca como web3.js. Esta biblioteca es compatible con la mayoría de los principales marcos de blockchain, como Ethereum. Esta biblioteca proporciona una API para interactuar con un contrato inteligente a través de una dirección de contrato. Por ejemplo, para leer los valores de un contrato inteligente, se puede usar el método de lectura de contrato de web3.js. Esto permitirá al desarrollador leer los valores de un contrato inteligente, como los parametros que se obtuvieron antes, la dirección del contrato, la versión y otros datos relevantes.

[![27](https://github.com/rozoandrescamilo/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/27.png?raw=true "27")](https://github.com/Consultar-parametros-de-un-smart-contract-desde-API-de-Kaleido/blob/main/img/27.png?raw=true "27")

Página oficial de Web3.js: [https://web3js.org/#/](https://web3js.org/#/ "https://web3js.org/#/")

Documentación Web3.js - Ethereum JavaScript API: [https://web3js.readthedocs.io/en/v1.7.5/](https://web3js.readthedocs.io/en/v1.7.5/ "https://web3js.readthedocs.io/en/v1.7.5/")

Para poder utilizar web3.js y consultar el archivo JSON provisto, primero se debe asegurar de tener instalado web3.js. Puede hacerlo mediante el comando <npm install web3> en la máquina local o remota donde corre Node.js.

Una vez instalado, se puede crear una instancia de web3 que permita conectar a una red Ethereum utilizando el proveedor de Kaleido. 

```javascript
const Web3 = require('web3');
const web3 = new Web3('https://u1my9uxwbm-u1bzt3mvmy-connect.us1-azure.kaleido.io/instances/d9cf87366ee9075d933dc562d4c5d0a6d8b0c580');

```

Después de establecer la conexión se utiliza la biblioteca web3.js para realizar consultas en un archivo JSON, el código utiliza el método <web3.eth.getBlock> para recuperar los parámetros del bloque especificado. Para este caso se utiliza el **transactionHash:**  "0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba".

```javascript
const contractAddress = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').contractAddress;
const gasUsed = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').gasUsed;
const cumulativeGasUsed = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').cumulativeGasUsed;
const blockHash = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').blockHash;
const blockNumber = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').blockNumber;
const openapi = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').openapi;
const apiexerciser = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').apiexerciser;
const from = web3.eth.getTransaction('0x089925e679ebace9b7205001e1db64e2d3db274608053b404f70d9ed895a2aba').from;

```

El resultado se almacena en variables separadas que contienen los datos deseados, como el hash del bloque, el número de bloque, la dirección del contrato, el gas utilizado, etc. Esta información se puede usar para verificar la integridad de los datos, realizar consultas en el contrato, etc.






