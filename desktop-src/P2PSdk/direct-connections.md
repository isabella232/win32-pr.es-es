---
description: Las infraestructuras de agrupación y grafos del mismo nivel permiten a las aplicaciones conectarse directamente a un nodo (graphing) o miembro (agrupación) y, a continuación, intercambiar datos directamente con el nodo. Esta conexión se denomina conexión directa.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Conexiones directas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f06fde65cf7597ccbec7f2968dbbf7662b4a6491ae59e6aa66b8baa587dc1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011633"
---
# <a name="direct-connections"></a>Conexiones directas

Las infraestructuras de agrupación y grafos del mismo nivel permiten a las aplicaciones conectarse directamente a un nodo (graphing) o miembro (agrupación) y, a continuación, intercambiar datos directamente con el nodo. Esta conexión se denomina conexión **directa.**

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Conexiones directas mediante la infraestructura de grafos del mismo nivel

Para poder establecer una conexión directa entre dos nodos de un grafo, ambos nodos deben registrarse para el evento **DE CONEXIÓN DIRECTA DE EVENTOS DE GRAPH \_ \_ \_ \_ DEL** MISMO NIVEL. Para recibir datos a través de una conexión directa, los nodos también deben registrarse para el evento **PEER \_ GRAPH EVENT \_ \_ INCOMING \_ DATA.**

**PEER \_ GRAPH \_ EVENT DIRECT CONNECTION \_ \_ es** un evento que notifica a una aplicación si un intento de conexión directa se realiza correctamente o no. El estado real correcto o erróneo de una llamada a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) se devuelve en la [**estructura PEER GRAPH EVENT \_ \_ \_ DATA.**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data)

Para crear una conexión directa, una aplicación llama a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)y, a continuación, pasa un identificador al gráfico, un puntero a la identidad del otro nodo que participa en la conexión y un puntero a una estructura de direcciones IPv6 para el nodo participante. La identidad del nodo y la dirección IPv6 especificadas en la llamada a **PeerGraphOpenDirectConnection** deben registrarse para el evento **PEER GRAPH EVENT \_ \_ \_ INCOMING \_ DATA** o no pueden recibir datos enviados por un elemento del mismo nivel que realiza la llamada. Cuando se realiza **correctamente, PeerGraphOpenDirectConnection** devuelve un identificador de conexión de 64 bits. Sin embargo, el elemento del mismo nivel debe esperar al evento DE CONEXIÓN DIRECTA **DEL EVENTO DEL \_ \_ MISMO \_ \_ GRUPO** ANTES de que el identificador de conexión directa se pueda identificar como válido.

Una vez que se realiza una conexión y se confirma un identificador de conexión válido, una aplicación puede llamar a [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) para enviar los datos a través de la conexión especificada por el identificador de conexión válido al elemento del mismo nivel participante, si el elemento del mismo nivel participante está registrado para el evento **PEER GRAPH EVENT \_ \_ \_ INCOMING \_ DATA.** Los datos opacos están disponibles como una estructura [**DE \_**](/windows/desktop/api/P2P/ns-p2p-peer_data) DATOS DEL MISMO NIVEL en los DATOS ENTRANTES DEL EVENTO DEL MISMO NIVEL devueltos por el evento DE **DATOS \_ \_ ENTRANTES DEL EVENTO DE GRAFO \_ \_ DEL** MISMO NIVEL. [**\_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data)

Cuando no se necesita una conexión, una aplicación llama a [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) con el identificador de grafo y el identificador de conexión.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Conexiones directas mediante la infraestructura de agrupación del mismo nivel

Las conexiones directas dentro de la infraestructura de agrupación del mismo nivel se controlan de forma similar a la infraestructura de grafos del mismo nivel.

Antes de que se pueda establecer una conexión directa entre dos miembros de un grupo, ambos miembros deben registrarse para el evento **DE CONEXIÓN DIRECTA DE EVENTOS DEL \_ \_ MISMO \_ \_** NIVEL. Si un miembro del grupo desea recibir datos a través de una conexión directa, el miembro del grupo también debe registrarse para el evento **PEER \_ GROUP EVENT \_ \_ INCOMING \_ DATA.**

**PEER \_ GROUP \_ EVENT DIRECT CONNECTION \_ \_ es** un evento que notifica a una aplicación si un intento de conexión directa se realiza correctamente o no. El estado real correcto o erróneo de una llamada a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) se devuelve en [**la PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) estructura.

Para crear una conexión directa, una aplicación llama a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)y, a continuación, pasa un identificador al grupo, un puntero a la identidad del otro miembro que participará en esta conexión y un puntero a una estructura de direcciones IPv6 para el miembro participante. El miembro cuya identidad y dirección IPv6 se especifican en la llamada a **PeerGroupOpenDirectConnection** debe estar registrado para el evento **PEER GROUP EVENT \_ \_ \_ INCOMING \_ DATA** o el miembro no puede recibir datos enviados por un elemento del mismo nivel que realiza la llamada. **PeerGroupOpenDirectConnection devuelve** un identificador de conexión de 64 bits cuando se realiza correctamente. Sin embargo, un elemento del mismo nivel debe esperar a que se genera el evento **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION** antes de que el identificador de conexión directa se pueda identificar como válido.

Una vez que se realiza una conexión y se confirma un identificador de conexión válido, una aplicación puede llamar a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) para enviar datos a través de una conexión especificada por el identificador de conexión válido al elemento del mismo nivel participante, si el elemento del mismo nivel participante está registrado para el evento **PEER GROUP EVENT \_ \_ \_ INCOMING \_ DATA.** Los datos opacos están disponibles como una estructura [**DE \_**](/windows/desktop/api/P2P/ns-p2p-peer_data) DATOS DEL MISMO NIVEL en los DATOS ENTRANTES DE EVENTOS DEL MISMO NIVEL devueltos por el evento DE **DATOS \_ \_ ENTRANTES DEL EVENTO \_ DEL \_** MISMO GRUPO. [**\_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data)

Cuando la conexión no es necesaria, la aplicación llama a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) con el identificador de grupo y el identificador de conexión.

## <a name="example-of-a-direct-connection-for-graphing"></a>Ejemplo de una conexión directa para el grafo


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



