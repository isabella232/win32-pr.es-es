---
description: Crear nodos de origen
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Crear nodos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705417"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="84504-103">Crear nodos de origen</span><span class="sxs-lookup"><span data-stu-id="84504-103">Creating Source Nodes</span></span>

<span data-ttu-id="84504-104">Un nodo de origen representa una secuencia de un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="84504-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="84504-105">El nodo de origen debe contener punteros al origen de medios, el descriptor de presentación y el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="84504-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="84504-106">Para agregar un nodo de origen a una topología, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="84504-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="84504-107">Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca de nodo de la **\_ topología MF \_ SOURCESTREAM \_** para crear el nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="84504-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="84504-108">Establezca el atributo de [**\_ \_ origen MF TOPONODE**](mf-toponode-source-attribute.md) en el nodo, con un puntero al origen de medios.</span><span class="sxs-lookup"><span data-stu-id="84504-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="84504-109">Establezca el atributo de [**\_ \_ \_ descriptor de presentación MF TOPONODE**](mf-toponode-presentation-descriptor-attribute.md) en el nodo, con un puntero al descriptor de presentación del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="84504-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="84504-110">Establezca el atributo de [**\_ \_ \_ descriptor de secuencia MF TOPONODE**](mf-toponode-stream-descriptor-attribute.md) en el nodo, con un puntero al descriptor de flujo para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="84504-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="84504-111">Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.</span><span class="sxs-lookup"><span data-stu-id="84504-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="84504-112">En el ejemplo siguiente se crea e inicializa un nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="84504-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="84504-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84504-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84504-114">Crear topologías</span><span class="sxs-lookup"><span data-stu-id="84504-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="84504-115">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="84504-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="84504-116">Topologías</span><span class="sxs-lookup"><span data-stu-id="84504-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="84504-117">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="84504-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



