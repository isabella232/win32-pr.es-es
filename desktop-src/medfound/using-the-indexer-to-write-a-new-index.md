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
# <a name="using-the-indexer-to-write-a-new-index"></a>Usar el indexador para escribir un nuevo índice

En este tema se muestra cómo escribir un índice para un archivo de formato de sistema avanzado (ASF).

Este es el procedimiento general para crear un índice ASF:

1.  Inicialice una nueva instancia del objeto de indexador ASF, tal como se describe en [creación y configuración de indexador](indexer-creation-and-configuration.md).
2.  Opcionalmente, configure el indexador.
3.  Envíe paquetes de datos ASF al indexador.
4.  Confirme el índice.
5.  Obtiene el índice completado del indexador y lo escribe en una secuencia.

## <a name="configure-the-indexer"></a>Configuración del indexador

Para usar el indexador para escribir un nuevo objeto de índice, el objeto de indexador debe tener la marca MFASF \_ Indexer \_ Escriba el \_ nuevo \_ conjunto de índices con una llamada a [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) antes de que se inicialice con [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).

Cuando el indexador está configurado para escribir un índice, el autor de la llamada elige las secuencias que se van a indizar. De forma predeterminada, el indexador intenta crear un objeto de índice para todas las secuencias. El intervalo de tiempo predeterminado es de un segundo.

[**IMFASFIndexer:: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) se puede usar para invalidar la opción predeterminada del objeto indexador de secuencias y tipos de índice.

En el ejemplo de código siguiente se muestra la inicialización de un \_ \_ descriptor de índice ASF y un \_ identificador de índice ASF \_ antes de llamar a [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).


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



El identificador de índice debe tener su tipo de índice GUID establecido en GUID \_ null para indicar que el tipo de índice se basará en el tiempo de presentación. El identificador de índice también se debe inicializar con el número de secuencia de la secuencia ASF que se va a indizar. Una vez establecido el identificador de índice, úselo para inicializar el descriptor de índice.

La estructura del descriptor de índice tiene miembros que se deben establecer antes de la llamada a [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus). **Identifier** es una estructura [**de \_ \_ identificador de índice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) que identifica el número de secuencia y el tipo de índice. **cPerEntryBytes** es el número de bytes que se usan para cada entrada de índice. Si el valor es MFASFINDEXER \_ por \_ \_ bytes de entrada \_ dinámicos, las entradas de índice tienen un tamaño variable. **dwInterval** es el intervalo de indización. Un valor de MFASFINDEXER \_ sin \_ \_ intervalo fijo indica que no hay ningún intervalo de indexación fijo.

## <a name="send-asf-data-packets-to-the-indexer"></a>Enviar paquetes de datos ASF al indexador

Dado que el indexador es un objeto de nivel WMContainer, debe usarse junto con el multiplexor durante la generación de paquetes.

Los paquetes devueltos de [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) se pueden enviar al objeto de indexador a través de llamadas a [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , donde se crean entradas de índice para cada paquete enviado.

En el código siguiente se muestra cómo se puede hacer esto:


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



Para obtener más información, consulte [generación de nuevos paquetes de datos ASF](generating-new-asf-data-packets.md).

## <a name="commit-the-index"></a>Confirmar el índice

Una vez que se haya creado una entrada de índice en el último paquete, se debe confirmar el índice. Esto se hace con una llamada a [**IMFASFIndexer:: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex). **CommitIndex** toma un puntero al objeto ContentInfo que describe el contenido del archivo ASF. La confirmación del índice finaliza la indexación y actualiza el encabezado con información nueva sobre el tamaño del archivo y la búsqueda.

## <a name="get-the-completed-index"></a>Obtener el índice completado

Para obtener el índice completado del indexador, realice los pasos siguientes:

1.  Llame a [**IMFASFIndexer:: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) para obtener el tamaño del índice.
2.  Llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para crear un búfer multimedia. Puede asignar un búfer lo suficientemente grande como para contener todo el índice, de asignar un búfer más pequeño y obtener el índice en fragmentos.
3.  Llame a [**IMFASFIndexer:: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) para obtener los datos de índice. En la primera llamada, establezca el parámetro *cbOffsetWithinIndex* en cero. Si obtiene el índice en fragmentos, incremente *cbOffsetWithinIndex* cada vez por el tamaño de los datos de la llamada anterior.
4.  Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a los datos de índice y el tamaño de los datos.
5.  Escriba los datos del índice en el archivo ASF.
6.  Llame a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer multimedia.
7.  Repita los pasos 3 a 6 hasta que haya escrito todo el índice.

El siguiente código muestra estos pasos:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexador ASF](asf-index-object.md)
</dt> </dl>

 

 



