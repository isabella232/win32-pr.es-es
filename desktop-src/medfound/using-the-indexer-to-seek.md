---
description: El indexador ASF es un componente de capa WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistemas avanzados (ASF). En este tema se proporciona información sobre el uso del indexador de ASF para buscar dentro de un archivo ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Usar el indexador para buscar dentro de un archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c674aa809c858856abf0c0e84c5d854b399c6fbc125ac9210e19b695380bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887245"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Usar el indexador para buscar dentro de un archivo ASF

El *indexador* ASF es un componente de capa WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistemas avanzados (ASF). En este tema se proporciona información sobre el uso del indexador de ASF para buscar dentro de un archivo ASF.

-   [Inicialización del indexador para la búsqueda](#initializing-the-indexer-for-seeking)
-   [Obtener la posición de búsqueda.](#getting-the-seek-position)
-   [Temas relacionados](#related-topics)

Para obtener información sobre la estructura de un archivo ASF, vea [ASF File Structure](asf-file-structure.md).

## <a name="initializing-the-indexer-for-seeking"></a>Inicialización del indexador para la búsqueda

Para inicializar el indexador de ASF para buscar:

1.  Llame [**a MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para crear una nueva instancia del indexador de ASF.
2.  Llame [**a IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar el indexador. Este método obtiene información del encabezado ASF para determinar qué secuencias de ASF se indexa. De forma predeterminada, el objeto de indexador está configurado para la búsqueda.
3.  Llame [**a IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) para buscar el desplazamiento del índice en el archivo ASF.
4.  Llame a [**la función MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) para crear una secuencia de bytes para leer el índice. La entrada a esta función es un puntero a una secuencia de bytes que contiene el archivo ASF y el desplazamiento del índice (del paso anterior).
5.  Llame [**a IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) para establecer la secuencia de bytes de índice en el indexador.

El siguiente código muestra estos pasos:


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a>Obtener la posición de búsqueda.

1.  Para averiguar si una secuencia determinada está indexada, llame a [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus). Si la secuencia está indexada, el *parámetro pfIsIndexed* recibe el valor **TRUE**; de lo contrario, recibe el **valor FALSE.**
2.  De forma predeterminada, el indexador usa la búsqueda hacia delante. Para la búsqueda inversa (es decir, buscar desde el final del archivo), llame a [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) y establezca la marca **READ FOR \_ \_ \_ \_ REVERSEPLAYBACK del INDEXER de MFASF.** De lo contrario, omita este paso.
3.  Si la secuencia está indexada, obtenga la posición de búsqueda durante un tiempo de presentación especificado llamando a [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue). Este método lee el índice de ASF y busca la entrada de índice más cercana a la hora solicitada. El método devuelve el desplazamiento de bytes del paquete de datos especificado por la entrada de índice. El desplazamiento de bytes es relativo al inicio del objeto de datos de ASF.

El [**método GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) toma un puntero a la estructura [**ASF INDEX \_ \_ IDENTIFIER.**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) Esta estructura especifica un tipo de índice y un identificador de flujo. Actualmente, el tipo de índice debe ser \_ GUID NULL, que especifica la indexación basada en el tiempo.

El código siguiente obtiene una posición de búsqueda, dado un identificador de flujo y un tiempo de presentación de destino. Si la llamada se realiza correctamente, devuelve el desplazamiento de datos en el parámetro *pwDataOffset* y el tiempo de búsqueda real aproximado en *phnsApproxSeekTime*.


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexador de ASF](asf-index-object.md)
</dt> </dl>

 

 



