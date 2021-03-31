---
description: En este tema se muestra cómo escribir un índice para un archivo de formato de sistema avanzado (ASF).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Usar el indexador para escribir un nuevo índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811527"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="f5c1d-103">Usar el indexador para escribir un nuevo índice</span><span class="sxs-lookup"><span data-stu-id="f5c1d-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="f5c1d-104">En este tema se muestra cómo escribir un índice para un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="f5c1d-105">Este es el procedimiento general para crear un índice ASF:</span><span class="sxs-lookup"><span data-stu-id="f5c1d-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="f5c1d-106">Inicialice una nueva instancia del objeto de indexador ASF, tal como se describe en [creación y configuración de indexador](indexer-creation-and-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="f5c1d-107">Opcionalmente, configure el indexador.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="f5c1d-108">Envíe paquetes de datos ASF al indexador.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="f5c1d-109">Confirme el índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-109">Commit the index.</span></span>
5.  <span data-ttu-id="f5c1d-110">Obtiene el índice completado del indexador y lo escribe en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="f5c1d-111">Configuración del indexador</span><span class="sxs-lookup"><span data-stu-id="f5c1d-111">Configure the Indexer</span></span>

<span data-ttu-id="f5c1d-112">Para usar el indexador para escribir un nuevo objeto de índice, el objeto de indexador debe tener la marca MFASF \_ Indexer \_ Escriba el \_ nuevo \_ conjunto de índices con una llamada a [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) antes de que se inicialice con [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="f5c1d-113">Cuando el indexador está configurado para escribir un índice, el autor de la llamada elige las secuencias que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="f5c1d-114">De forma predeterminada, el indexador intenta crear un objeto de índice para todas las secuencias.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="f5c1d-115">El intervalo de tiempo predeterminado es de un segundo.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-115">The default time interval is one second.</span></span>

<span data-ttu-id="f5c1d-116">[**IMFASFIndexer:: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) se puede usar para invalidar la opción predeterminada del objeto indexador de secuencias y tipos de índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="f5c1d-117">En el ejemplo de código siguiente se muestra la inicialización de un \_ \_ descriptor de índice ASF y un \_ identificador de índice ASF \_ antes de llamar a [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



<span data-ttu-id="f5c1d-118">El identificador de índice debe tener su tipo de índice GUID establecido en GUID \_ null para indicar que el tipo de índice se basará en el tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="f5c1d-119">El identificador de índice también se debe inicializar con el número de secuencia de la secuencia ASF que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="f5c1d-120">Una vez establecido el identificador de índice, úselo para inicializar el descriptor de índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="f5c1d-121">La estructura del descriptor de índice tiene miembros que se deben establecer antes de la llamada a [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="f5c1d-122">**Identifier** es una estructura [**de \_ \_ identificador de índice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) que identifica el número de secuencia y el tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="f5c1d-123">**cPerEntryBytes** es el número de bytes que se usan para cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="f5c1d-124">Si el valor es MFASFINDEXER \_ por \_ \_ bytes de entrada \_ dinámicos, las entradas de índice tienen un tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="f5c1d-125">**dwInterval** es el intervalo de indización.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="f5c1d-126">Un valor de MFASFINDEXER \_ sin \_ \_ intervalo fijo indica que no hay ningún intervalo de indexación fijo.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="f5c1d-127">Enviar paquetes de datos ASF al indexador</span><span class="sxs-lookup"><span data-stu-id="f5c1d-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="f5c1d-128">Dado que el indexador es un objeto de nivel WMContainer, debe usarse junto con el multiplexor durante la generación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="f5c1d-129">Los paquetes devueltos de [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) se pueden enviar al objeto de indexador a través de llamadas a [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , donde se crean entradas de índice para cada paquete enviado.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="f5c1d-130">En el código siguiente se muestra cómo se puede hacer esto:</span><span class="sxs-lookup"><span data-stu-id="f5c1d-130">The following code demonstrates how this may be done:</span></span>


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



<span data-ttu-id="f5c1d-131">Para obtener más información, consulte [generación de nuevos paquetes de datos ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="f5c1d-132">Confirmar el índice</span><span class="sxs-lookup"><span data-stu-id="f5c1d-132">Commit the Index</span></span>

<span data-ttu-id="f5c1d-133">Una vez que se haya creado una entrada de índice en el último paquete, se debe confirmar el índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="f5c1d-134">Esto se hace con una llamada a [**IMFASFIndexer:: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span><span class="sxs-lookup"><span data-stu-id="f5c1d-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="f5c1d-135">**CommitIndex** toma un puntero al objeto ContentInfo que describe el contenido del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="f5c1d-136">La confirmación del índice finaliza la indexación y actualiza el encabezado con información nueva sobre el tamaño del archivo y la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="f5c1d-137">Obtener el índice completado</span><span class="sxs-lookup"><span data-stu-id="f5c1d-137">Get the Completed Index</span></span>

<span data-ttu-id="f5c1d-138">Para obtener el índice completado del indexador, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5c1d-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="f5c1d-139">Llame a [**IMFASFIndexer:: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) para obtener el tamaño del índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="f5c1d-140">Llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para crear un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="f5c1d-141">Puede asignar un búfer lo suficientemente grande como para contener todo el índice, de asignar un búfer más pequeño y obtener el índice en fragmentos.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="f5c1d-142">Llame a [**IMFASFIndexer:: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) para obtener los datos de índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="f5c1d-143">En la primera llamada, establezca el parámetro *cbOffsetWithinIndex* en cero.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="f5c1d-144">Si obtiene el índice en fragmentos, incremente *cbOffsetWithinIndex* cada vez por el tamaño de los datos de la llamada anterior.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="f5c1d-145">Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a los datos de índice y el tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="f5c1d-146">Escriba los datos del índice en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="f5c1d-147">Llame a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="f5c1d-148">Repita los pasos 3 a 6 hasta que haya escrito todo el índice.</span><span class="sxs-lookup"><span data-stu-id="f5c1d-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="f5c1d-149">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="f5c1d-149">The following code shows these steps:</span></span>


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="f5c1d-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5c1d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c1d-151">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="f5c1d-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



