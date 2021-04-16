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
# <a name="creating-transform-nodes"></a><span data-ttu-id="9035b-103">Crear nodos de transformación</span><span class="sxs-lookup"><span data-stu-id="9035b-103">Creating Transform Nodes</span></span>

<span data-ttu-id="9035b-104">Un nodo de transformación representa una Media Foundation transformación (MFT), como un descodificador o un codificador.</span><span class="sxs-lookup"><span data-stu-id="9035b-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="9035b-105">Hay varias maneras de inicializar un nodo de transformación:</span><span class="sxs-lookup"><span data-stu-id="9035b-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="9035b-106">Desde un puntero a la MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="9035b-107">Desde un CLSID para MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="9035b-108">Desde un puntero a un objeto de activación para la MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="9035b-109">Si va a cargar la topología dentro de la ruta de acceso a medios protegidos (PMP), debe usar el CLSID o un objeto de activación para que se pueda crear el MFT dentro del proceso protegido.</span><span class="sxs-lookup"><span data-stu-id="9035b-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="9035b-110">El primer enfoque (con un puntero a la MFT) no funciona con el PMP.</span><span class="sxs-lookup"><span data-stu-id="9035b-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="9035b-111">Crear un nodo de transformación desde un MFT</span><span class="sxs-lookup"><span data-stu-id="9035b-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="9035b-112">Para crear un nodo de transformación a partir de una MFT, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9035b-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="9035b-113">Cree una instancia de MFT y obtenga un puntero a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="9035b-114">Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de transformación de topología** para crear el nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="9035b-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="9035b-115">Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="9035b-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="9035b-116">Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.</span><span class="sxs-lookup"><span data-stu-id="9035b-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="9035b-117">En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de una MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-117">The following example creates and initializes a transform node from an MFT.</span></span>


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



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="9035b-118">Crear un nodo de transformación a partir de un CLSID</span><span class="sxs-lookup"><span data-stu-id="9035b-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="9035b-119">Para crear un nodo de transformación a partir de un CLSID, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9035b-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="9035b-120">Busque el CLSID de la MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="9035b-121">Puede usar la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) para buscar los CLSID de MFTs por categoría, como descodificadores o codificadores.</span><span class="sxs-lookup"><span data-stu-id="9035b-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="9035b-122">También puede conocer el CLSID de un MFT determinado que desea usar (por ejemplo, si implementó su propio MFT personalizado).</span><span class="sxs-lookup"><span data-stu-id="9035b-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="9035b-123">Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de transformación de topología** para crear el nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="9035b-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="9035b-124">Establezca el atributo **MF \_ TOPONODE \_ Transform \_ objectId** en el nodo.</span><span class="sxs-lookup"><span data-stu-id="9035b-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="9035b-125">El valor del atributo es el CLSID.</span><span class="sxs-lookup"><span data-stu-id="9035b-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="9035b-126">Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.</span><span class="sxs-lookup"><span data-stu-id="9035b-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="9035b-127">En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de un CLSID.</span><span class="sxs-lookup"><span data-stu-id="9035b-127">The following example creates and initializes a transform node from a CLSID.</span></span>


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



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="9035b-128">Crear un nodo de transformación a partir de un objeto de activación</span><span class="sxs-lookup"><span data-stu-id="9035b-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="9035b-129">Algunos MFTs proporcionan objetos de activación.</span><span class="sxs-lookup"><span data-stu-id="9035b-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="9035b-130">Por ejemplo, la función [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) devuelve un objeto de activación para el codificador Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="9035b-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="9035b-131">La función exacta depende de la MFT.</span><span class="sxs-lookup"><span data-stu-id="9035b-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="9035b-132">No todos los MFT proporcionan un objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="9035b-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="9035b-133">Para obtener más información, consulte [objetos de activación](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9035b-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="9035b-134">También puede obtener un objeto de activación de MFT llamando a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="9035b-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="9035b-135">Para crear un nodo de transformación a partir de un objeto de activación, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9035b-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="9035b-136">Cree el objeto de activación y obtenga un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="9035b-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="9035b-137">Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de transformación de topología** para crear el nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="9035b-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="9035b-138">Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="9035b-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="9035b-139">Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.</span><span class="sxs-lookup"><span data-stu-id="9035b-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="9035b-140">En el ejemplo siguiente se crea e inicializa un nodo de transformación a partir de un objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="9035b-140">The following example creates and initializes a transform node from an activation object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9035b-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9035b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9035b-142">Crear topologías</span><span class="sxs-lookup"><span data-stu-id="9035b-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="9035b-143">Topologías</span><span class="sxs-lookup"><span data-stu-id="9035b-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="9035b-144">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9035b-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



