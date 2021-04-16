---
description: Enlazar nodos de salida a receptores de medios
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Enlazar nodos de salida a receptores de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547331"
---
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="ef737-103">Enlazar nodos de salida a receptores de medios</span><span class="sxs-lookup"><span data-stu-id="ef737-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="ef737-104">En este tema se describe cómo inicializar los nodos de salida en una topología, si usa el cargador de topología fuera de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="ef737-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="ef737-105">Inicialmente, un nodo de salida contiene uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef737-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="ef737-106">Puntero [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ef737-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="ef737-107">Puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="ef737-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="ef737-108">En el último caso, el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) debe convertirse en un puntero [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) antes de que el cargador de topología resuelva la topología.</span><span class="sxs-lookup"><span data-stu-id="ef737-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="ef737-109">En la mayoría de los escenarios, el proceso funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ef737-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="ef737-110">La aplicación pone en cola una topología parcial en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="ef737-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="ef737-111">En todos los nodos de salida, la sesión multimedia convierte punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en punteros [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ef737-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="ef737-112">Este proceso se denomina *enlazar* el nodo de salida a un receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="ef737-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="ef737-113">La sesión multimedia envía la topología modificada al método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="ef737-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="ef737-114">Sin embargo, si usa el cargador de topología directamente (fuera del sesiones de medios), la aplicación debe enlazar los nodos de salida antes de llamar a [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span><span class="sxs-lookup"><span data-stu-id="ef737-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="ef737-115">Para enlazar un nodo de salida, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ef737-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="ef737-116">Llame a [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) para obtener el puntero de objeto del nodo.</span><span class="sxs-lookup"><span data-stu-id="ef737-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="ef737-117">Consulte el puntero de objeto para la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ef737-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="ef737-118">Si esta llamada se realiza correctamente, no hay nada más que hacer, así que omita los pasos restantes.</span><span class="sxs-lookup"><span data-stu-id="ef737-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="ef737-119">Si se produjo un error en el paso anterior, consulte el puntero del objeto para la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="ef737-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="ef737-120">Cree el receptor de medios mediante una llamada a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="ef737-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="ef737-121">Especifique **IID \_ IMFMediaSink** para obtener un puntero a la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="ef737-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="ef737-122">Consulte el nodo del atributo [**\_ \_ STREAMID de MF TOPONODE**](mf-toponode-streamid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ef737-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="ef737-123">El valor de este atributo es el identificador del receptor de flujo para este nodo.</span><span class="sxs-lookup"><span data-stu-id="ef737-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="ef737-124">Si no se establece el atributo **MF \_ TOPONODE \_ STREAMID** , el identificador de secuencia predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="ef737-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="ef737-125">Es posible que ya exista el receptor de flujo adecuado en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="ef737-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="ef737-126">Para comprobarlo, llame a [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="ef737-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="ef737-127">Si el receptor de flujo existe, el método devuelve un puntero a su interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ef737-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="ef737-128">Si se produce un error en esta llamada, intente agregar un nuevo receptor de flujo llamando a [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="ef737-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="ef737-129">Si se produce un error en ambas llamadas, significa que el receptor multimedia no admite el identificador de flujo solicitado y que este nodo de topología no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef737-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="ef737-130">Devuelva un código de error y omita el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="ef737-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="ef737-131">Llame a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), pasando el puntero [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="ef737-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="ef737-132">Esta llamada reemplaza el puntero de objeto del nodo, de modo que el nodo contiene un puntero al receptor de la secuencia, en lugar de un puntero al objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="ef737-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="ef737-133">En el código siguiente se muestra cómo enlazar un nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="ef737-133">The following code shows how to bind an output node.</span></span>


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="ef737-134">En este ejemplo se usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="ef737-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="ef737-135">En el ejemplo siguiente se muestra cómo enlazar todos los nodos de salida en una topología.</span><span class="sxs-lookup"><span data-stu-id="ef737-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="ef737-136">En este ejemplo se usa el método [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) para obtener una colección de nodos de salida de la topología.</span><span class="sxs-lookup"><span data-stu-id="ef737-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="ef737-137">A continuación, llama a la función mostrada en el ejemplo anterior en cada uno de esos nodos a su vez.</span><span class="sxs-lookup"><span data-stu-id="ef737-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ef737-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef737-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef737-139">Creación de topologías avanzadas</span><span class="sxs-lookup"><span data-stu-id="ef737-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="ef737-140">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="ef737-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="ef737-141">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="ef737-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



