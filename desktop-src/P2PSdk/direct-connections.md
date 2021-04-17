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
# <a name="direct-connections"></a><span data-ttu-id="6b533-104">Conexiones directas</span><span class="sxs-lookup"><span data-stu-id="6b533-104">Direct Connections</span></span>

<span data-ttu-id="6b533-105">Las infraestructuras de gráficos del mismo nivel y de agrupación del mismo nivel permiten a las aplicaciones conectarse directamente a un nodo (gráficos) o miembro (agrupación) y, a continuación, intercambiar datos directamente con el nodo.</span><span class="sxs-lookup"><span data-stu-id="6b533-105">The Peer Graphing and Peer Grouping Infrastructures allow applications to connect directly to one node (Graphing) or member (Grouping), and then exchange data directly with the node.</span></span> <span data-ttu-id="6b533-106">Esta conexión se denomina **conexión directa**.</span><span class="sxs-lookup"><span data-stu-id="6b533-106">This connection is called a **direct connection**.</span></span>

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a><span data-ttu-id="6b533-107">Conexiones directas mediante la infraestructura de gráficos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="6b533-107">Direct Connections using the Peer Graphing Infrastructure</span></span>

<span data-ttu-id="6b533-108">Antes de que se pueda establecer una conexión directa entre dos nodos de un gráfico, ambos nodos deben estar registrados para el evento de **\_ \_ \_ \_ conexión directa de evento de grafo del mismo nivel** .</span><span class="sxs-lookup"><span data-stu-id="6b533-108">Before a direct connection can be established between two nodes in a graph, both nodes must be registered for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="6b533-109">Para recibir datos a través de una conexión directa, los nodos también se deben registrar para el evento de **datos de entrada de \_ eventos de gráficos \_ \_ \_ del mismo nivel** .</span><span class="sxs-lookup"><span data-stu-id="6b533-109">To receive data over a direct connection, the nodes must also be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="6b533-110">**Del mismo nivel \_ La \_ \_ \_ conexión directa de eventos de gráfico** es un evento que notifica a una aplicación si un intento de conexión directa se realiza correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="6b533-110">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="6b533-111">El estado real de éxito o error de una llamada a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) se devuelve en la estructura de datos de [**\_ \_ eventos \_ del grafo del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .</span><span class="sxs-lookup"><span data-stu-id="6b533-111">The actual success or failure status of a call to [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) is returned in the [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure.</span></span>

<span data-ttu-id="6b533-112">Para crear una conexión directa, una aplicación llama a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)y, a continuación, pasa un identificador al gráfico, un puntero a la identidad del otro nodo que participa en la conexión y un puntero a una estructura de direcciones IPv6 para el nodo participante.</span><span class="sxs-lookup"><span data-stu-id="6b533-112">To create a direct connection, an application calls [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), and then passes a handle to the graph, a pointer to the identity of the other node that is participating in the connection, and a pointer to an IPv6 address structure for the participating node.</span></span> <span data-ttu-id="6b533-113">La identidad del nodo y la dirección IPv6 que se especifican en la llamada a **PeerGraphOpenDirectConnection** deben estar registradas para el evento de **\_ \_ \_ \_ datos entrantes del evento del elemento del mismo nivel** o no pueden recibir datos enviados por un elemento del mismo nivel que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="6b533-113">The node identity and IPv6 address that are specified in the call to **PeerGraphOpenDirectConnection** must be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event, or it cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="6b533-114">Cuando se realiza correctamente, **PeerGraphOpenDirectConnection** devuelve un identificador de conexión de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6b533-114">When successful, **PeerGraphOpenDirectConnection** returns a 64-bit connection ID.</span></span> <span data-ttu-id="6b533-115">Sin embargo, el elemento del mismo nivel debe esperar al evento de **\_ \_ \_ \_ conexión directa del evento de grupo del mismo nivel** antes de que el identificador de conexión directa pueda identificarse como válido.</span><span class="sxs-lookup"><span data-stu-id="6b533-115">However, the peer must wait for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="6b533-116">Una vez que se establece una conexión y se confirma un identificador de conexión válido, una aplicación puede llamar a [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) para enviar los datos a través de la conexión especificada por el identificador de conexión válido al elemento del mismo nivel que lo participa, si el elemento del mismo nivel participante se registra para el evento de **datos de entrada de \_ eventos de gráficos \_ \_ \_ del mismo nivel** .</span><span class="sxs-lookup"><span data-stu-id="6b533-116">After a connection is made and a valid connection ID is confirmed, an application can call [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) to send the data across the connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="6b533-117">Los datos opacos están disponibles como una estructura de [**\_ datos del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_data) en los [**\_ \_ \_ datos entrantes del evento del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) devueltos por el evento de datos de entrada de **eventos de \_ gráficos del \_ \_ \_ mismo** nivel.</span><span class="sxs-lookup"><span data-stu-id="6b533-117">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="6b533-118">Cuando no se necesita una conexión, una aplicación llama a [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) con el identificador de gráfico y el identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="6b533-118">When a connection is not needed, an application calls [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) with the graph handle and the connection ID.</span></span>

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a><span data-ttu-id="6b533-119">Conexiones directas mediante la infraestructura de agrupación del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="6b533-119">Direct Connections using the Peer Grouping Infrastructure</span></span>

<span data-ttu-id="6b533-120">Las conexiones directas dentro de la infraestructura de agrupación del mismo nivel se administran de forma similar a la infraestructura de gráficos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="6b533-120">Direct connections within the Peer Grouping Infrastructure are handled similar to the Peer Graphing Infrastructure.</span></span>

<span data-ttu-id="6b533-121">Antes de que se pueda establecer una conexión directa entre dos miembros de un grupo, ambos miembros deben registrarse para el evento de **\_ \_ \_ \_ conexión directa de evento de grupo del mismo nivel** .</span><span class="sxs-lookup"><span data-stu-id="6b533-121">Before a direct connection can be established between two members in a group, both members must register for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="6b533-122">Si un miembro del grupo desea recibir datos a través de una conexión directa, el miembro del grupo también debe registrarse para el evento de **\_ \_ \_ \_ datos entrantes del evento de grupo del mismo nivel** .</span><span class="sxs-lookup"><span data-stu-id="6b533-122">If a group member wants to receive data over a direct connection, the group member must also register for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="6b533-123">**Del mismo nivel \_ La \_ \_ \_ conexión directa de eventos de grupo** es un evento que notifica a una aplicación si un intento de conexión directa se realiza correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="6b533-123">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** is an event that is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="6b533-124">El estado real de éxito o error de una llamada a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) se devuelve en la estructura [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .</span><span class="sxs-lookup"><span data-stu-id="6b533-124">The actual success or failure status of a call to [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) is returned in the [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure.</span></span>

<span data-ttu-id="6b533-125">Para crear una conexión directa, una aplicación llama a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)y, a continuación, pasa un identificador al grupo, un puntero a la identidad del otro miembro que participará en esta conexión y un puntero a una estructura de dirección IPv6 para el miembro participante.</span><span class="sxs-lookup"><span data-stu-id="6b533-125">To create a direct connection, an application calls [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), and then passes a handle to the group, a pointer to the identity of the other member that will participate in this connection, and a pointer to an IPv6 address structure for the participating member.</span></span> <span data-ttu-id="6b533-126">El miembro cuya identidad y dirección IPv6 se especifican en la llamada a **PeerGroupOpenDirectConnection** debe estar registrado para el evento de datos de **entrada de \_ eventos de grupo \_ \_ \_ del mismo nivel** , o bien el miembro no puede recibir datos enviados por un elemento del mismo nivel de llamada.</span><span class="sxs-lookup"><span data-stu-id="6b533-126">The member whose identity and IPv6 address are specified in the call to **PeerGroupOpenDirectConnection** must be registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event, or the member cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="6b533-127">**PeerGroupOpenDirectConnection** devuelve un identificador de conexión de 64 bits cuando se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b533-127">**PeerGroupOpenDirectConnection** returns a 64-bit connection ID when successful.</span></span> <span data-ttu-id="6b533-128">Sin embargo, un elemento del mismo nivel debe esperar a que se produzca el evento de **\_ \_ \_ \_ conexión directa del evento del grafo del mismo nivel** antes de que el identificador de conexión directa pueda identificarse como válido.</span><span class="sxs-lookup"><span data-stu-id="6b533-128">However, a peer must wait for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event to be raised before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="6b533-129">Una vez que se establece una conexión y se confirma un identificador de conexión válido, una aplicación puede llamar a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) para enviar datos a través de una conexión especificada por el identificador de conexión válido al elemento del mismo nivel participante, si el elemento del mismo nivel participante está registrado para el evento de **datos de entrada del \_ evento de grupo \_ \_ \_ del mismo nivel** .</span><span class="sxs-lookup"><span data-stu-id="6b533-129">After a connection is made and a valid connection ID is confirmed, then an application can call [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) to send data across a connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="6b533-130">Los datos opacos están disponibles como una estructura de [**\_ datos del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_data) en los [**\_ \_ \_ datos entrantes del evento del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) devueltos por el evento de datos de entrada de **eventos de \_ Grupo del \_ \_ \_ mismo** nivel.</span><span class="sxs-lookup"><span data-stu-id="6b533-130">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="6b533-131">Cuando no se necesita la conexión, la aplicación llama a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) con el identificador de grupo y el identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="6b533-131">When the connection is not needed, the application calls [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) with the group handle and the connection ID.</span></span>

## <a name="example-of-a-direct-connection-for-graphing"></a><span data-ttu-id="6b533-132">Ejemplo de conexión directa para gráficos</span><span class="sxs-lookup"><span data-stu-id="6b533-132">Example of a Direct Connection for Graphing</span></span>


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



 

 



