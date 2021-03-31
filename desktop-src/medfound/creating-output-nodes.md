---
description: Crear nodos de salida
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Crear nodos de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907573"
---
# <a name="creating-output-nodes"></a>Crear nodos de salida

Un nodo de salida representa un receptor de flujo en un receptor de multimedia. Hay dos maneras de inicializar un nodo de salida:

-   Desde un puntero al receptor de la secuencia.
-   Desde un puntero a un objeto de activación para el receptor de medios.

Si va a cargar la topología dentro de la ruta de acceso a los medios protegidos (PMP), debe usar un objeto de activación para que el receptor de medios pueda crearse dentro del proceso protegido. El primer enfoque (con un puntero al receptor de la secuencia) no funciona con el PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Creación de un nodo de salida a partir de un receptor de flujo

Para crear un nodo de salida a partir de un receptor de flujo, haga lo siguiente:

1.  Cree una instancia del receptor de medios.
2.  Use la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor de medios para obtener un puntero al receptor de flujo deseado. (La interfaz **IMFMediaSink** tiene varios métodos que devuelven punteros a un receptor de flujo).
3.  Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de salida** de la topología para crear el nodo de salida.
4.  Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase un puntero a la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del receptor de la secuencia.
5.  Establezca el atributo [**MF \_ TOPONODE \_ noshutdown \_ on \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) en **false** (opcional pero recomendado).
6.  Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de salida a partir de un receptor de flujo.


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



Cuando la aplicación cierra la sesión multimedia, la sesión de medios cierra automáticamente el receptor de medios. Por lo tanto, no se puede volver a usar el receptor de medios con otra instancia de la sesión multimedia.

## <a name="creating-an-output-node-from-an-activation-object"></a>Crear un nodo de salida a partir de un objeto de activación

Cualquier receptor de medios de confianza debe proporcionar un objeto de activación para que se pueda crear el receptor de medios en el proceso protegido. Para obtener más información, consulte [objetos de activación](activation-objects.md). La función concreta que crea el objeto de activación dependerá del receptor de medios.

Para crear un nodo de salida a partir de un objeto de activación, haga lo siguiente:

1.  Cree el objeto de activación y obtenga un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del objeto de activación.
2.  Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de salida** de la topología para crear el nodo de salida.
3.  Opcionalmente, establezca el atributo [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) en el nodo para especificar el identificador de flujo del receptor de la secuencia. Si se omite este atributo, el nodo utiliza de forma predeterminada el receptor de flujo 0.
4.  Establezca el atributo [**MF \_ TOPONODE \_ noshutdown \_ on \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) en **true** (opcional pero recomendado).
5.  Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
6.  Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

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

[Crear topologías](creating-topologies.md)
</dt> <dt>

[Receptores de medios](media-sinks.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



