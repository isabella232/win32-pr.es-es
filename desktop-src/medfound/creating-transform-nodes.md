---
description: Crear nodos de transformación
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Crear nodos de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539610"
---
# <a name="creating-transform-nodes"></a>Crear nodos de transformación

Un nodo de transformación representa una Media Foundation transformación (MFT), como un descodificador o un codificador. Hay varias maneras de inicializar un nodo de transformación:

-   Desde un puntero a la MFT.
-   Desde un CLSID para MFT.
-   Desde un puntero a un objeto de activación para la MFT.

Si va a cargar la topología dentro de la ruta de acceso a medios protegidos (PMP), debe usar el CLSID o un objeto de activación para que se pueda crear el MFT dentro del proceso protegido. El primer enfoque (con un puntero a la MFT) no funciona con el PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Crear un nodo de transformación desde un MFT

Para crear un nodo de transformación a partir de una MFT, haga lo siguiente:

1.  Cree una instancia de MFT y obtenga un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de MFT.
2.  Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de transformación de topología** para crear el nodo de transformación.
3.  Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .
4.  Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de una MFT.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a>Crear un nodo de transformación a partir de un CLSID

Para crear un nodo de transformación a partir de un CLSID, haga lo siguiente:

1.  Busque el CLSID de la MFT. Puede usar la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) para buscar los CLSID de MFTs por categoría, como descodificadores o codificadores. También puede conocer el CLSID de un MFT determinado que desea usar (por ejemplo, si implementó su propio MFT personalizado).
2.  Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de transformación de topología** para crear el nodo de transformación.
3.  Establezca el atributo **MF \_ TOPONODE \_ Transform \_ objectId** en el nodo. El valor del atributo es el CLSID.
4.  Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de un CLSID.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a>Crear un nodo de transformación a partir de un objeto de activación

Algunos MFTs proporcionan objetos de activación. Por ejemplo, la función [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) devuelve un objeto de activación para el codificador Windows Media Audio (WMA). La función exacta depende de la MFT. No todos los MFT proporcionan un objeto de activación. Para obtener más información, consulte [objetos de activación](activation-objects.md).

También puede obtener un objeto de activación de MFT llamando a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Para crear un nodo de transformación a partir de un objeto de activación, haga lo siguiente:

1.  Cree el objeto de activación y obtenga un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del objeto de activación.
2.  Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de transformación de topología** para crear el nodo de transformación.
3.  Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de un objeto de activación.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear topologías](creating-topologies.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



