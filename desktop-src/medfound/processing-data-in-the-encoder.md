---
description: Procesamiento de datos en el codificador
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Procesamiento de datos en el codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715507"
---
# <a name="processing-data-in-the-encoder"></a>Procesamiento de datos en el codificador

Después de haber negociado el tipo de entrada y el tipo de salida de la MFT del codificador, tal y como se describe en [negociación de tipos multimedia en el codificador](media-type-negotiation-on-the-encoder.md), puede empezar a procesar muestras de datos multimedia. Los datos se pasan en forma de muestras de medios (interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) y también se reciben del resultado como muestras de medios.

Antes de enviar datos al codificador para su procesamiento, debe asignar un ejemplo multimedia y agregar uno o varios búferes multimedia que contengan los datos multimedia que deben codificarse. Llame a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y pase un puntero al ejemplo de medios asignados. Además del ejemplo multimedia, **ProcessInput** también necesita el identificador del flujo de entrada. Para obtener el identificador de flujo, llame a [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Dado que un codificador está diseñado para tener solo una salida y una, estos identificadores de flujo siempre tienen el valor 0.

Para obtener datos del codificador, llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Antes de llamar a [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), debe averiguar si el codificador asigna los ejemplos de medios de salida o debe hacerlo explícitamente. Para ello, llame a [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Esto devuelve información de ejemplo multimedia de salida en la estructura de [**información del flujo de salida de MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Si el codificador asigna ejemplos de medios, devuelve el flujo de salida de \_ MFT \_ proporciona \_ la \_ marca samples en el miembro **dwFlags** y el miembro **cbSize** contiene cero. Si el codificador espera que asigne el búfer de salida, cree el ejemplo multimedia de salida y el búfer de medios asociado en función del tamaño devuelto en **cbSize**. Cuando llame a [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pase un puntero al ejemplo multimedia que se acaba de crear. Durante la sesión de codificación, el codificador llena los búferes multimedia, señalados por el ejemplo multimedia de salida, con los datos codificados.

Para iniciar la sesión de codificación, pase el ejemplo de medios de entrada al codificador mediante una llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). El codificador comienza el procesamiento y los datos, y genera uno o más ejemplos de medios de salida que se deben recuperar mediante [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) siempre que devuelva la \_ transformación MF E \_ \_ necesite \_ más \_ entrada. Si llama a **ProcessInput** para pasar más entradas mientras haya datos de salida que se van a recuperar, **ProcessInput** producirá un error con MF \_ E \_ NOTACCEPTING. El codificador no acepta más entradas hasta que el cliente llama a **ProcessOutput** al menos una vez.

Debe establecer las marcas de tiempo y duraciones precisas para todos los ejemplos de entrada pasados. Las marcas de tiempo no son estrictamente necesarias pero ayudan a mantener la sincronización de audio y vídeo. Si no dispone de las marcas de tiempo para los ejemplos, es mejor dejarlas de usar valores inciertos.

## <a name="encoder-processing-example"></a>Ejemplo de procesamiento del codificador

En el ejemplo de código siguiente se muestra cómo llamar a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener un ejemplo codificado. Para obtener el contexto completo de este ejemplo, vea [código de ejemplo del codificador](encoder-example-code.md).


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multiplexor ASF](asf-multiplexer.md)
</dt> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



