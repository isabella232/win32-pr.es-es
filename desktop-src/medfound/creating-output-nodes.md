---
description: Creación de nodos de salida
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Creación de nodos de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af2842458fb360374d34583b15bfbf5005b2f2bbdd8b32332bc6756ca4e8157
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943025"
---
# <a name="creating-output-nodes"></a>Creación de nodos de salida

Un nodo de salida representa un receptor de flujo en un receptor multimedia. Hay dos maneras de inicializar un nodo de salida:

-   Desde un puntero al receptor de flujo.
-   Desde un puntero a un objeto de activación para el receptor multimedia.

Si va a cargar la topología dentro de la ruta de acceso de medios protegidos (PMP), debe usar un objeto de activación para que el receptor de medios se pueda crear dentro del proceso protegido. El primer enfoque (mediante un puntero al receptor de flujo) no funciona con el PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Creación de un nodo de salida a partir de un receptor de flujo

Para crear un nodo de salida a partir de un receptor de flujo, haga lo siguiente:

1.  Cree una instancia del receptor de medios.
2.  Use la interfaz [**DEMIMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor multimedia para obtener un puntero al receptor de flujo deseado. (La **interfaz IMFMediaSink** tiene varios métodos que devuelven punteros a un receptor de flujo).
3.  Llame [**a MFCreateTopologyNode con**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) la marca MF **\_ TOPOLOGY OUTPUT \_ \_ NODE** para crear el nodo de salida.
4.  Llame [**a IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase un puntero a la interfaz [**DESTREAMSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del receptor de secuencias.
5.  Establezca el [**atributo MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) en **FALSE** (opcional pero recomendado).
6.  Llame [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de salida desde un receptor de flujo.


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



Cuando la aplicación cierra la sesión multimedia, la sesión multimedia apaga automáticamente el receptor multimedia. Por lo tanto, no puede volver a usar el receptor de medios con otra instancia de la sesión multimedia.

## <a name="creating-an-output-node-from-an-activation-object"></a>Crear un nodo de salida a partir de un objeto de activación

Cualquier receptor de medios de confianza debe proporcionar un objeto de activación, para que el receptor de medios se pueda crear dentro del proceso protegido. Para obtener más información, vea [Activation Objects](activation-objects.md). La función concreta que crea el objeto de activación dependerá del receptor de medios.

Para crear un nodo de salida a partir de un objeto de activación, haga lo siguiente:

1.  Cree el objeto de activación y obtenga un puntero a la interfaz [**DEACTIVATE del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) objeto de activación.
2.  Llame [**a MFCreateTopologyNode con**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) la marca MF **\_ TOPOLOGY OUTPUT \_ \_ NODE** para crear el nodo de salida.
3.  Opcionalmente, establezca el atributo [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) en el nodo para especificar el identificador de flujo del receptor de flujo. Si omite este atributo, el nodo usa de forma predeterminada el receptor de flujo 0.
4.  Establezca el [**atributo MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) en **TRUE** (opcional pero recomendado).
5.  Llame [**a IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el [**puntero IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
6.  Llame [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de salida a partir de un objeto de activación.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Creación de topologías](creating-topologies.md)
</dt> <dt>

[Receptores multimedia](media-sinks.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



