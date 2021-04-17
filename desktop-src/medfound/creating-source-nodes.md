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
# <a name="creating-source-nodes"></a>Crear nodos de origen

Un nodo de origen representa una secuencia de un origen de medios. El nodo de origen debe contener punteros al origen de medios, el descriptor de presentación y el descriptor de flujo.

Para agregar un nodo de origen a una topología, haga lo siguiente:

1.  Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca de nodo de la **\_ topología MF \_ SOURCESTREAM \_** para crear el nodo de origen.
2.  Establezca el atributo de [**\_ \_ origen MF TOPONODE**](mf-toponode-source-attribute.md) en el nodo, con un puntero al origen de medios.
3.  Establezca el atributo de [**\_ \_ \_ descriptor de presentación MF TOPONODE**](mf-toponode-presentation-descriptor-attribute.md) en el nodo, con un puntero al descriptor de presentación del origen multimedia.
4.  Establezca el atributo de [**\_ \_ \_ descriptor de secuencia MF TOPONODE**](mf-toponode-stream-descriptor-attribute.md) en el nodo, con un puntero al descriptor de flujo para la secuencia.
5.  Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de origen.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear topologías](creating-topologies.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



