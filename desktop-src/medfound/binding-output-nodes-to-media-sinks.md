---
description: Enlazar nodos de salida a receptores multimedia
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Enlazar nodos de salida a receptores multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475843"
---
# <a name="binding-output-nodes-to-media-sinks"></a>Enlazar nodos de salida a receptores multimedia

En este tema se describe cómo inicializar los nodos de salida en una topología si usa el cargador de topologías fuera de la sesión multimedia. Inicialmente, un nodo de salida contiene uno de los siguientes elementos:

-   Puntero [**DE TIPO IMFStreamSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
-   Puntero [**DE LA ACTIVIDAD DE LA**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ACTIVIDAD.

En el último caso, el puntero [**DE HECHOActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) se debe convertir en un puntero [**DE TIPO IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) antes de que el cargador de topologías resuelva la topología. En la mayoría de los escenarios, el proceso funciona de la siguiente manera:

1.  La aplicación pone en cola una topología parcial en la sesión multimedia.
2.  Para todos los nodos de salida, la sesión multimedia convierte los punteros [**DE LAACTIVATE EN**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) [**PUNTEROS DE BOTÓNSTREAMSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) Este proceso se denomina *enlazar el* nodo de salida a un receptor multimedia.
3.  La sesión multimedia envía la topología modificada al [**método IMFTopoLoader::Load.**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load)

Sin embargo, si usa el cargador de topologías directamente (fuera de la petición de medios), la aplicación debe enlazar los nodos de salida antes de llamar a [**LA CARGATOPOLOADER::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load). Para enlazar un nodo de salida, haga lo siguiente:

1.  Llame [**a IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) para obtener el puntero de objeto del nodo.
2.  Consulte el puntero de objeto para la [**interfaz DESTREAMSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) Si esta llamada se realiza correctamente, no hay nada más que hacer, así que omita los pasos restantes.
3.  Si el paso anterior no se pudo realizar, consulte el puntero de objeto para la [**interfaz DESACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
4.  Cree el receptor de medios mediante una llamada [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Especifique **IID \_ IMFMediaSink para** obtener un puntero a la interfaz [**DEGMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor multimedia.
5.  Consulte el nodo para el atributo [**MF \_ TOPONODE \_ STREAMID.**](mf-toponode-streamid-attribute.md) El valor de este atributo es el identificador del receptor de flujo para este nodo. Si el **atributo MF \_ TOPONODE \_ STREAMID** no está establecido, el identificador de flujo predeterminado es cero.
6.  Es posible que el receptor de flujo adecuado ya exista en el receptor de medios. Para comprobarlo, llame [**a IMFMediaSink::GetStreamSinkById en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) el receptor multimedia. Si el receptor de flujo existe, el método devuelve un puntero a su [**interfaz DESTREAMSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) Si se produce un error en esta llamada, intente agregar un nuevo receptor de flujo mediante una llamada a [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Si se producirá un error en ambas llamadas, significa que el receptor multimedia no admite el identificador de flujo solicitado y este nodo de topología no está configurado correctamente. Devuelve un código de error y omite el paso siguiente.
7.  Llame [**a IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), pasando el puntero [**DE LANSTREAMSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del paso anterior. Esta llamada reemplaza el puntero de objeto del nodo, de modo que el nodo contiene un puntero al receptor de flujo, en lugar de un puntero al objeto de activación.

El código siguiente muestra cómo enlazar un nodo de salida.


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
> En este ejemplo se usa [la función SafeRelease para](saferelease.md) liberar punteros de interfaz.

 

En el ejemplo siguiente se muestra cómo enlazar todos los nodos de salida de una topología. En este ejemplo se usa [**el método IMFTopology::GetOutputNodeCollection para**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) obtener una colección de nodos de salida de la topología. A continuación, llama a la función que se muestra en el ejemplo anterior en cada uno de esos nodos a su vez.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de topología avanzada](advanced-topology-building.md)
</dt> <dt>

[Receptores multimedia](media-sinks.md)
</dt> <dt>

[**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



