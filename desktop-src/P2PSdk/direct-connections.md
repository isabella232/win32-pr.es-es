---
description: Las infraestructuras de gráficos del mismo nivel y de agrupación del mismo nivel permiten a las aplicaciones conectarse directamente a un nodo (gráficos) o miembro (agrupación) y, a continuación, intercambiar datos directamente con el nodo. Esta conexión se denomina conexión directa.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Conexiones directas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667449"
---
# <a name="direct-connections"></a>Conexiones directas

Las infraestructuras de gráficos del mismo nivel y de agrupación del mismo nivel permiten a las aplicaciones conectarse directamente a un nodo (gráficos) o miembro (agrupación) y, a continuación, intercambiar datos directamente con el nodo. Esta conexión se denomina **conexión directa**.

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Conexiones directas mediante la infraestructura de gráficos del mismo nivel

Antes de que se pueda establecer una conexión directa entre dos nodos de un gráfico, ambos nodos deben estar registrados para el evento de **\_ \_ \_ \_ conexión directa de evento de grafo del mismo nivel** . Para recibir datos a través de una conexión directa, los nodos también se deben registrar para el evento de **datos de entrada de \_ eventos de gráficos \_ \_ \_ del mismo nivel** .

**Del mismo nivel \_ La \_ \_ \_ conexión directa de eventos de gráfico** es un evento que notifica a una aplicación si un intento de conexión directa se realiza correctamente o no. El estado real de éxito o error de una llamada a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) se devuelve en la estructura de datos de [**\_ \_ eventos \_ del grafo del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .

Para crear una conexión directa, una aplicación llama a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)y, a continuación, pasa un identificador al gráfico, un puntero a la identidad del otro nodo que participa en la conexión y un puntero a una estructura de direcciones IPv6 para el nodo participante. La identidad del nodo y la dirección IPv6 que se especifican en la llamada a **PeerGraphOpenDirectConnection** deben estar registradas para el evento de **\_ \_ \_ \_ datos entrantes del evento del elemento del mismo nivel** o no pueden recibir datos enviados por un elemento del mismo nivel que realiza la llamada. Cuando se realiza correctamente, **PeerGraphOpenDirectConnection** devuelve un identificador de conexión de 64 bits. Sin embargo, el elemento del mismo nivel debe esperar al evento de **\_ \_ \_ \_ conexión directa del evento de grupo del mismo nivel** antes de que el identificador de conexión directa pueda identificarse como válido.

Una vez que se establece una conexión y se confirma un identificador de conexión válido, una aplicación puede llamar a [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) para enviar los datos a través de la conexión especificada por el identificador de conexión válido al elemento del mismo nivel que lo participa, si el elemento del mismo nivel participante se registra para el evento de **datos de entrada de \_ eventos de gráficos \_ \_ \_ del mismo nivel** . Los datos opacos están disponibles como una estructura de [**\_ datos del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_data) en los [**\_ \_ \_ datos entrantes del evento del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) devueltos por el evento de datos de entrada de **eventos de \_ gráficos del \_ \_ \_ mismo** nivel.

Cuando no se necesita una conexión, una aplicación llama a [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) con el identificador de gráfico y el identificador de conexión.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Conexiones directas mediante la infraestructura de agrupación del mismo nivel

Las conexiones directas dentro de la infraestructura de agrupación del mismo nivel se administran de forma similar a la infraestructura de gráficos del mismo nivel.

Antes de que se pueda establecer una conexión directa entre dos miembros de un grupo, ambos miembros deben registrarse para el evento de **\_ \_ \_ \_ conexión directa de evento de grupo del mismo nivel** . Si un miembro del grupo desea recibir datos a través de una conexión directa, el miembro del grupo también debe registrarse para el evento de **\_ \_ \_ \_ datos entrantes del evento de grupo del mismo nivel** .

**Del mismo nivel \_ La \_ \_ \_ conexión directa de eventos de grupo** es un evento que notifica a una aplicación si un intento de conexión directa se realiza correctamente o no. El estado real de éxito o error de una llamada a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) se devuelve en la estructura [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .

Para crear una conexión directa, una aplicación llama a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)y, a continuación, pasa un identificador al grupo, un puntero a la identidad del otro miembro que participará en esta conexión y un puntero a una estructura de dirección IPv6 para el miembro participante. El miembro cuya identidad y dirección IPv6 se especifican en la llamada a **PeerGroupOpenDirectConnection** debe estar registrado para el evento de datos de **entrada de \_ eventos de grupo \_ \_ \_ del mismo nivel** , o bien el miembro no puede recibir datos enviados por un elemento del mismo nivel de llamada. **PeerGroupOpenDirectConnection** devuelve un identificador de conexión de 64 bits cuando se realiza correctamente. Sin embargo, un elemento del mismo nivel debe esperar a que se produzca el evento de **\_ \_ \_ \_ conexión directa del evento del grafo del mismo nivel** antes de que el identificador de conexión directa pueda identificarse como válido.

Una vez que se establece una conexión y se confirma un identificador de conexión válido, una aplicación puede llamar a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) para enviar datos a través de una conexión especificada por el identificador de conexión válido al elemento del mismo nivel participante, si el elemento del mismo nivel participante está registrado para el evento de **datos de entrada del \_ evento de grupo \_ \_ \_ del mismo nivel** . Los datos opacos están disponibles como una estructura de [**\_ datos del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_data) en los [**\_ \_ \_ datos entrantes del evento del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) devueltos por el evento de datos de entrada de **eventos de \_ Grupo del \_ \_ \_ mismo** nivel.

Cuando no se necesita la conexión, la aplicación llama a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) con el identificador de grupo y el identificador de conexión.

## <a name="example-of-a-direct-connection-for-graphing"></a>Ejemplo de conexión directa para gráficos


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



 

 



