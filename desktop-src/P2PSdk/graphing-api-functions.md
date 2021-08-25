---
description: 'Peer Graphing API usa las siguientes funciones:'
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: Funciones de graphing API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26c40770e8fcbc18b08ccb73dcfea5f1f6c4eab65be615ed76d8088ddc90954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776225"
---
# <a name="graphing-api-functions"></a>Funciones de graphing API

Peer Graphing API usa las siguientes funciones:

## <a name="initialization-and-cleanup-functions"></a>Funciones de inicialización y limpieza



| Función                                       | Descripción                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphShutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | Limpia los recursos asignados por la llamada a [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup).                     |
| [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | Indica a la infraestructura de grafos del mismo nivel qué versión de los protocolos del mismo nivel requiere la aplicación que realiza la llamada. |



 

## <a name="graph-creation-and-access-functions"></a>Graph Funciones de creación y acceso



| Función                                   | Descripción                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | Invalida el identificador del gráfico del mismo nivel devuelto por una llamada a [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) o [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)y cierra todas las conexiones de red para el gráfico del mismo nivel especificado. |
| [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | Crea un nuevo gráfico del mismo nivel.                                                                                                                                                                                             |
| [**PeerGraphDelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | Elimina los datos asociados a un gráfico del mismo nivel especificado.                                                                                                                                                              |
| [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | Indica que un gráfico del mismo nivel debe empezar a escuchar las conexiones entrantes.                                                                                                                                          |
| [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | Abre un gráfico del mismo nivel creado previamente por el nodo local o un nodo remoto.                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>Graph y funciones de información de nodo



| Función                                                         | Descripción                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEnumNodes**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | Crea y devuelve un identificador de enumeración utilizado para enumerar los nodos de un gráfico del mismo nivel.                                                                             |
| [**PeerGraphGetNodeInfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | Recupera información sobre un nodo específico.                                                                                                                       |
| [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | Recupera las propiedades actuales del grafo del mismo nivel.                                                                                                                       |
| [**PeerGraphGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | Devuelve el estado actual del gráfico del mismo nivel.                                                                                                                      |
| [**PeerGraphSetNodeAttributes**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | Establece los atributos de la estructura [**DE \_ INFORMACIÓN DEL \_ NODO**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) DEL MISMO NIVEL para el nodo local.                                                                |
| [**PeerGraphSetPresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | Activa o desactiva explícitamente la publicación de registros de presencia para un nodo específico. Esta función puede invalidar la configuración de presencia en las propiedades del gráfico del mismo nivel. |
| [**PeerGraphSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | Establece las propiedades del gráfico del mismo nivel.                                                                                                                                    |



 

## <a name="record-management-functions"></a>Funciones de administración de registros



| Función                                                                     | Descripción                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | Agrega un nuevo registro a un gráfico del mismo nivel. Un registro agregado con esta función se envía a cada nodo de un gráfico del mismo nivel.                          |
| [**PeerGraphDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | Marca un registro como eliminado dentro de un gráfico del mismo nivel.                                                                                      |
| [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | Crea y devuelve un identificador de enumeración utilizado para enumerar los registros de un tipo específico de registro, usuario o ambos.                    |
| [**PeerGraphGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | Recupera un registro específico basado en el identificador de registro especificado.                                                                       |
| [**PeerGraphSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | Busca registros específicos en el gráfico del mismo nivel.                                                                                       |
| [**PeerGraphUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | Actualiza un registro en el gráfico del mismo nivel y, a continuación, desborda el registro a cada nodo del gráfico del mismo nivel.                                       |
| [**PeerGraphValidateDeferredRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | Indica a la infraestructura de grafos del mismo nivel que es el momento de volver a enviar los registros diferidos para que el módulo de seguridad valide. |



 

## <a name="export-and-import-functions"></a>Funciones de exportación e importación



| Función                                                   | Descripción                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | Exporta una base de datos de grafos del mismo nivel a un archivo que puede mover a otro equipo. |
| [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | Importa un archivo que contiene la información de una base de datos de grafos del mismo nivel.             |



 

## <a name="utility-and-support-functions"></a>Funciones de utilidad y soporte técnico



| Función                                                                     | Descripción                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | Libera un identificador de enumeración y libera los recursos asociados a una enumeración.                                           |
| [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | Libera los recursos que devuelven varias de las funciones de Peer Graphing API.                                                           |
| [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | Recupera el número de elementos de una enumeración.                                                                                  |
| [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | Obtiene el siguiente elemento o elementos de una enumeración creada por una llamada a funciones específicas, que devuelven una enumeración del mismo nivel.        |
| [**PeerGraphPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | Convierte el valor de tiempo de referencia mantenido por el grafo del mismo nivel en un valor de tiempo localizado adecuado para mostrarlo en el equipo del mismo nivel. |
| [**PeerGraphUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | Convierte un valor de hora universal del equipo del mismo nivel en un valor de tiempo de gráfico del mismo nivel común.                                       |



 

## <a name="connection-functions"></a>Funciones de conexión



| Función                                                                 | Descripción                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | Cierra una conexión directa especificada.                                                                                                                                                                                                          |
| [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | Intenta realizar una conexión a un nodo especificado en un gráfico del mismo nivel. Esta función inicia una operación asincrónica.                                                                                                                             |
| [**PeerGraphEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | Crea y devuelve un identificador de enumeración utilizado para enumerar las conexiones de un nodo local.                                                                                                                                                   |
| [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | Permite que una aplicación establezca una conexión directa con un nodo en un gráfico del mismo nivel. La conexión solo se puede realizar si el nodo al que se conecta la aplicación se ha suscrito al evento **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION.** |
| [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | Envía datos a un nodo vecino o a un nodo conectado directamente.                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>Funciones de infraestructura de eventos



| Función                                                     | Descripción                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | Recupera eventos del mismo nivel.                                                                                       |
| [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | Registra la solicitud de un mismo nivel para recibir una notificación de los cambios asociados a un grafo del mismo nivel y al tipo de evento.            |
| [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | Solicita que la aplicación ya no sea notificada de los cambios asociados a un grafo del mismo nivel y al tipo de registro. |



 

 

 



