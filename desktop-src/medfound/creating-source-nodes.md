---
description: Creación de nodos de origen
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Creación de nodos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360713"
---
# <a name="creating-source-nodes"></a>Creación de nodos de origen

Un nodo de origen representa una secuencia de un origen multimedia. El nodo de origen debe contener punteros al origen multimedia, al descriptor de presentación y al descriptor de secuencia.

Para agregar un nodo de origen a una topología, haga lo siguiente:

1.  Llame [**a MFCreateTopologyNode con**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) la marca MF **\_ TOPOLOGY \_ SOURCESTREAM \_ NODE** para crear el nodo de origen.
2.  Establezca el [**atributo MF \_ TOPONODE \_ SOURCE**](mf-toponode-source-attribute.md) en el nodo, con un puntero al origen multimedia.
3.  Establezca el [**atributo MF \_ TOPONODE \_ PRESENTATION \_ DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) en el nodo, con un puntero al descriptor de presentación del origen multimedia.
4.  Establezca el [**atributo MF \_ TOPONODE \_ STREAM \_ DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) en el nodo, con un puntero al descriptor de flujo para la secuencia.
5.  Llame [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

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

[Creación de topologías](creating-topologies.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



