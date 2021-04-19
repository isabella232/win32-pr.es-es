---
description: El indexador ASF es un componente de nivel WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistema avanzado (ASF). En este tema se proporciona información acerca del uso del indexador ASF para buscar en un archivo ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Uso del indexador para buscar en un archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715785"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a><span data-ttu-id="6d927-104">Uso del indexador para buscar en un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="6d927-104">Using the Indexer to Seek Within an ASF File</span></span>

<span data-ttu-id="6d927-105">El *indexador* ASF es un componente de nivel WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="6d927-105">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="6d927-106">En este tema se proporciona información acerca del uso del indexador ASF para buscar en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6d927-106">This topic provides information about using the ASF indexer to seek within an ASF file.</span></span>

-   [<span data-ttu-id="6d927-107">Inicializar el indizador para buscar</span><span class="sxs-lookup"><span data-stu-id="6d927-107">Initializing the Indexer for Seeking</span></span>](#initializing-the-indexer-for-seeking)
-   [<span data-ttu-id="6d927-108">Obtener la posición de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6d927-108">Getting the Seek Position.</span></span>](#getting-the-seek-position)
-   [<span data-ttu-id="6d927-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d927-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="6d927-110">Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="6d927-110">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="initializing-the-indexer-for-seeking"></a><span data-ttu-id="6d927-111">Inicializar el indizador para buscar</span><span class="sxs-lookup"><span data-stu-id="6d927-111">Initializing the Indexer for Seeking</span></span>

<span data-ttu-id="6d927-112">Para inicializar el indizador ASF para búsquedas:</span><span class="sxs-lookup"><span data-stu-id="6d927-112">To initialize the ASF indexer for seeking:</span></span>

1.  <span data-ttu-id="6d927-113">Llame a [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para crear una nueva instancia del indexador ASF.</span><span class="sxs-lookup"><span data-stu-id="6d927-113">Call [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) to create a new instance of the ASF indexer.</span></span>
2.  <span data-ttu-id="6d927-114">Llame a [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar el indizador.</span><span class="sxs-lookup"><span data-stu-id="6d927-114">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer.</span></span> <span data-ttu-id="6d927-115">Este método obtiene información del encabezado ASF para determinar qué secuencias ASF están indizadas.</span><span class="sxs-lookup"><span data-stu-id="6d927-115">This method gets information from the ASF header to determine which ASF streams are indexed.</span></span> <span data-ttu-id="6d927-116">De forma predeterminada, el objeto de indexador está configurado para búsquedas.</span><span class="sxs-lookup"><span data-stu-id="6d927-116">By default, the indexer object is configured for seeking.</span></span>
3.  <span data-ttu-id="6d927-117">Llame a [**IMFASFIndexer:: GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) para buscar el desplazamiento del índice en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6d927-117">Call [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) to find the offset of the index within the ASF file.</span></span>
4.  <span data-ttu-id="6d927-118">Llame a la función [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) para crear una secuencia de bytes para leer el índice.</span><span class="sxs-lookup"><span data-stu-id="6d927-118">Call the [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) function to create a byte stream for reading the index.</span></span> <span data-ttu-id="6d927-119">La entrada a esta función es un puntero a una secuencia de bytes que contiene el archivo ASF y el desplazamiento del índice (del paso anterior).</span><span class="sxs-lookup"><span data-stu-id="6d927-119">The input to this function is a pointer to a byte stream that contains the ASF file, and the offset of the index (from the previous step).</span></span>
5.  <span data-ttu-id="6d927-120">Llame a [**IMFASFIndexer:: SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) para establecer la secuencia de bytes de índice en el indizador.</span><span class="sxs-lookup"><span data-stu-id="6d927-120">Call [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) to set the index byte stream on the indexer.</span></span>

<span data-ttu-id="6d927-121">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6d927-121">The following code shows these steps:</span></span>


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



## <a name="getting-the-seek-position"></a><span data-ttu-id="6d927-122">Obtener la posición de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6d927-122">Getting the Seek Position.</span></span>

1.  <span data-ttu-id="6d927-123">Para averiguar si una secuencia determinada está indizada, llame a [**IMFASFIndexer:: GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span><span class="sxs-lookup"><span data-stu-id="6d927-123">To find out if a particular stream is indexed, call [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span></span> <span data-ttu-id="6d927-124">Si la secuencia está indizada, el parámetro *pfIsIndexed* recibe el valor **true**; en caso contrario, recibe el valor **false**.</span><span class="sxs-lookup"><span data-stu-id="6d927-124">If the stream is indexed, the *pfIsIndexed* parameter receives the value **TRUE**; otherwise it receives the value **FALSE**.</span></span>
2.  <span data-ttu-id="6d927-125">De forma predeterminada, el indexador utiliza búsquedas hacia delante.</span><span class="sxs-lookup"><span data-stu-id="6d927-125">By default, the indexer uses forward seeking.</span></span> <span data-ttu-id="6d927-126">Para la búsqueda inversa (es decir, la búsqueda desde el final del archivo), llame a [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) y establezca la **lectura del \_ indexador MFASF \_ \_ para \_** la marca REVERSEPLAYBACK.</span><span class="sxs-lookup"><span data-stu-id="6d927-126">For reverse seeking (that is, seeking from the end of the file), call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) and set the **MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK** flag.</span></span> <span data-ttu-id="6d927-127">De lo contrario, omita este paso.</span><span class="sxs-lookup"><span data-stu-id="6d927-127">Otherwise, skip this step.</span></span>
3.  <span data-ttu-id="6d927-128">Si la secuencia está indizada, obtenga la posición de búsqueda de un tiempo de presentación especificado llamando a [**IMFASFIndexer:: GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span><span class="sxs-lookup"><span data-stu-id="6d927-128">If the stream is indexed, get the seek position for a specified presentation time by calling [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span></span> <span data-ttu-id="6d927-129">Este método lee el índice ASF y encuentra la entrada de índice más cercana a la hora solicitada.</span><span class="sxs-lookup"><span data-stu-id="6d927-129">This method reads the ASF index and finds the index entry that is closest to the requested time.</span></span> <span data-ttu-id="6d927-130">El método devuelve el desplazamiento de bytes del paquete de datos especificado por la entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="6d927-130">The method returns the byte offset of the data packet specified by the index entry.</span></span> <span data-ttu-id="6d927-131">El desplazamiento de bytes es relativo al inicio del objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6d927-131">The byte offset is relative to the start of the ASF Data Object.</span></span>

<span data-ttu-id="6d927-132">El método [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) toma un puntero a la estructura del [**\_ \_ identificador de índice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) .</span><span class="sxs-lookup"><span data-stu-id="6d927-132">The [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) method takes a pointer to the [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure.</span></span> <span data-ttu-id="6d927-133">Esta estructura especifica un tipo de índice y un identificador de flujo.</span><span class="sxs-lookup"><span data-stu-id="6d927-133">This structure specifies an index type and a stream identifier.</span></span> <span data-ttu-id="6d927-134">Actualmente, el tipo de índice debe ser GUID \_ null, que especifica la indexación basada en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="6d927-134">Currently, the index type must be GUID\_NULL, which specifies time-based indexing.</span></span>

<span data-ttu-id="6d927-135">El código siguiente obtiene una posición de búsqueda, dado un identificador de flujo y el tiempo de presentación del destino.</span><span class="sxs-lookup"><span data-stu-id="6d927-135">The following code gets a seek position, given a stream identifier and target presentation time.</span></span> <span data-ttu-id="6d927-136">Si la llamada se realiza correctamente, devuelve el desplazamiento de datos en el parámetro *pcbDataOffset* y el tiempo de búsqueda real aproximado en *phnsApproxSeekTime*.</span><span class="sxs-lookup"><span data-stu-id="6d927-136">If the call succeeds, it returns the data offset in the *pcbDataOffset* parameter and the approximate actual seek time in *phnsApproxSeekTime*.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6d927-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d927-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d927-138">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="6d927-138">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



