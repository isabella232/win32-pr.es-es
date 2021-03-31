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
# <a name="creating-output-nodes"></a><span data-ttu-id="6629f-103">Crear nodos de salida</span><span class="sxs-lookup"><span data-stu-id="6629f-103">Creating Output Nodes</span></span>

<span data-ttu-id="6629f-104">Un nodo de salida representa un receptor de flujo en un receptor de multimedia.</span><span class="sxs-lookup"><span data-stu-id="6629f-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="6629f-105">Hay dos maneras de inicializar un nodo de salida:</span><span class="sxs-lookup"><span data-stu-id="6629f-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="6629f-106">Desde un puntero al receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6629f-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="6629f-107">Desde un puntero a un objeto de activación para el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6629f-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="6629f-108">Si va a cargar la topología dentro de la ruta de acceso a los medios protegidos (PMP), debe usar un objeto de activación para que el receptor de medios pueda crearse dentro del proceso protegido.</span><span class="sxs-lookup"><span data-stu-id="6629f-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="6629f-109">El primer enfoque (con un puntero al receptor de la secuencia) no funciona con el PMP.</span><span class="sxs-lookup"><span data-stu-id="6629f-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="6629f-110">Creación de un nodo de salida a partir de un receptor de flujo</span><span class="sxs-lookup"><span data-stu-id="6629f-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="6629f-111">Para crear un nodo de salida a partir de un receptor de flujo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6629f-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="6629f-112">Cree una instancia del receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6629f-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="6629f-113">Use la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor de medios para obtener un puntero al receptor de flujo deseado.</span><span class="sxs-lookup"><span data-stu-id="6629f-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="6629f-114">(La interfaz **IMFMediaSink** tiene varios métodos que devuelven punteros a un receptor de flujo).</span><span class="sxs-lookup"><span data-stu-id="6629f-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="6629f-115">Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de salida** de la topología para crear el nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="6629f-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="6629f-116">Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase un puntero a la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6629f-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="6629f-117">Establezca el atributo [**MF \_ TOPONODE \_ noshutdown \_ on \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) en **false** (opcional pero recomendado).</span><span class="sxs-lookup"><span data-stu-id="6629f-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="6629f-118">Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.</span><span class="sxs-lookup"><span data-stu-id="6629f-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="6629f-119">En el ejemplo siguiente se crea e inicializa un nodo de salida a partir de un receptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="6629f-119">The following example creates and initializes an output node from a stream sink.</span></span>


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



<span data-ttu-id="6629f-120">Cuando la aplicación cierra la sesión multimedia, la sesión de medios cierra automáticamente el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6629f-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="6629f-121">Por lo tanto, no se puede volver a usar el receptor de medios con otra instancia de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="6629f-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="6629f-122">Crear un nodo de salida a partir de un objeto de activación</span><span class="sxs-lookup"><span data-stu-id="6629f-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="6629f-123">Cualquier receptor de medios de confianza debe proporcionar un objeto de activación para que se pueda crear el receptor de medios en el proceso protegido.</span><span class="sxs-lookup"><span data-stu-id="6629f-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="6629f-124">Para obtener más información, consulte [objetos de activación](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6629f-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="6629f-125">La función concreta que crea el objeto de activación dependerá del receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6629f-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="6629f-126">Para crear un nodo de salida a partir de un objeto de activación, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6629f-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="6629f-127">Cree el objeto de activación y obtenga un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="6629f-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="6629f-128">Llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con la marca **MF del \_ \_ \_ nodo de salida** de la topología para crear el nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="6629f-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="6629f-129">Opcionalmente, establezca el atributo [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) en el nodo para especificar el identificador de flujo del receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6629f-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="6629f-130">Si se omite este atributo, el nodo utiliza de forma predeterminada el receptor de flujo 0.</span><span class="sxs-lookup"><span data-stu-id="6629f-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="6629f-131">Establezca el atributo [**MF \_ TOPONODE \_ noshutdown \_ on \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) en **true** (opcional pero recomendado).</span><span class="sxs-lookup"><span data-stu-id="6629f-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="6629f-132">Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) y pase el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="6629f-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="6629f-133">Llame a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para agregar el nodo a la topología.</span><span class="sxs-lookup"><span data-stu-id="6629f-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="6629f-134">En el ejemplo siguiente se crea e inicializa un nodo de salida a partir de un objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="6629f-134">The following example creates and initializes an output node from an activation object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6629f-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6629f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6629f-136">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="6629f-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="6629f-137">Crear topologías</span><span class="sxs-lookup"><span data-stu-id="6629f-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="6629f-138">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="6629f-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="6629f-139">Topologías</span><span class="sxs-lookup"><span data-stu-id="6629f-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



