---
description: Crear nodos de transformación
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Crear nodos de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc6cc0aff2d429cee2d9d3b175c57dacd773dc865f702e043386127b9104833d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346905"
---
# <a name="creating-transform-nodes"></a>Crear nodos de transformación

Un nodo de transformación representa una Media Foundation transformación (MFT), como un descodificador o codificador. Hay varias maneras de inicializar un nodo de transformación:

-   De un puntero a MFT.
-   Desde un CLSID para el MFT.
-   De un puntero a un objeto de activación para el MFT.

Si va a cargar la topología dentro de la ruta de acceso de medios protegidos (PMP), debe usar el CLSID o un objeto de activación para que el MFT se pueda crear dentro del proceso protegido. El primer enfoque (mediante un puntero a MFT) no funciona con el PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Creación de un nodo de transformación a partir de un MFT

Para crear un nodo de transformación a partir de un MFT, haga lo siguiente:

1.  Cree una instancia de MFT y obtenga un puntero a la interfaz [**DETRANSFORMtransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del MFT.
2.  Llame [**a MFCreateTopologyNode con**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) la marca MF **\_ TOPOLOGY TRANSFORM \_ \_ NODE** para crear el nodo de transformación.
3.  Llame [**a IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el [**puntero DETRANSFORMTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
4.  Llame [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de un MFT.


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

1.  Busque el CLSID del MFT. Puede usar la [**función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) para buscar los CLSID de LAS MFT por categoría, como descodificadores o codificadores. También puede conocer el CLSID de un MFT determinado que desea usar (por ejemplo, si implementó su propio MFT personalizado).
2.  Llame [**a MFCreateTopologyNode con**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) la marca MF **\_ TOPOLOGY TRANSFORM \_ \_ NODE** para crear el nodo de transformación.
3.  Establezca el **atributo MF \_ TOPONODE \_ TRANSFORM \_ OBJECTID** en el nodo. El valor del atributo es el CLSID.
4.  Llame [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

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

Algunas MTA proporcionan objetos de activación. Por ejemplo, la [**función MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) devuelve un objeto de activación para el codificador Windows Media Audio (WMA). La función exacta depende de MFT. No todos los MFT proporcionan un objeto de activación. Para obtener más información, vea [Activation Objects](activation-objects.md).

También puede obtener un objeto de activación de MFT llamando a la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Para crear un nodo de transformación a partir de un objeto de activación, haga lo siguiente:

1.  Cree el objeto de activación y obtenga un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del objeto de activación.
2.  Llame [**a MFCreateTopologyNode con**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) la marca MF **\_ TOPOLOGY TRANSFORM \_ \_ NODE** para crear el nodo de transformación.
3.  Llame [**a IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**DE LAACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
4.  Llame [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.

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

[Creación de topologías](creating-topologies.md)
</dt> <dt>

[Topologías](topologies.md)
</dt> <dt>

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



