---
description: Procesamiento de datos en el codificador
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Procesamiento de datos en el codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666c2a2ff2139aadcb489022eb9b324eff1de523551244c2fd12ad0e11f68f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238736"
---
# <a name="processing-data-in-the-encoder"></a>Procesamiento de datos en el codificador

Después de haber negociado el tipo de entrada y el tipo de salida para el MFT del codificador, como se describe en [Negociación](media-type-negotiation-on-the-encoder.md)de tipo multimedia en el codificador , puede empezar a procesar ejemplos de datos multimedia. Los datos se pasan en forma de muestras de medios (interfaz [**DESAMPLESAMPLE)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) y también se reciben de la salida como ejemplos multimedia.

Antes de enviar datos al codificador para su procesamiento, debe asignar un ejemplo multimedia y agregar uno de los búferes multimedia más que contienen datos multimedia que deben codificarse. Llame [**a IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y pase un puntero al ejemplo multimedia asignado. Además del ejemplo multimedia, **ProcessInput** también necesita el identificador de flujo de entrada. Para obtener el identificador de flujo, llame [**a LALETransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Dado que un codificador está diseñado para tener solo una salida, estos identificadores de secuencia siempre tienen el valor 0.

Para obtener datos del codificador, llame [**a LATRANSFORMTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Antes de llamar a [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), debe averiguar si el codificador asigna los ejemplos de medios de salida o debe hacerlo explícitamente. Para ello, llame a [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Esto devuelve información de ejemplo de medios de salida en la [**estructura \_ MFT OUTPUT \_ STREAM \_ INFO.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) Si el codificador asigna ejemplos multimedia, devuelve la marca MFT OUTPUT STREAM PROVIDES SAMPLES en el miembro dwFlags y el \_ \_ miembro \_ \_ **cbSize** contiene cero.  Si el codificador espera que asigne el búfer de salida, cree el ejemplo de medios de salida y el búfer multimedia asociado en función del tamaño devuelto en **cbSize**. Al llamar a [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pase un puntero al ejemplo multimedia recién creado. Durante la sesión de codificación, el codificador rellena los búferes multimedia, señalados por el ejemplo de medios de salida, con los datos codificados.

Para iniciar la sesión de codificación, pase el ejemplo de medios de entrada al codificador mediante una llamada [**a ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). El codificador inicia el procesamiento y los datos y genera uno o varios ejemplos de medios de salida que [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) debe recuperar siempre que devuelva MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT. Si llama a **ProcessInput para** pasar más entrada siempre y cuando haya datos de salida que recuperar, **ProcessInput** produce un error con MF \_ E \_ NOTACCEPTING. El codificador no acepta más entradas hasta que el cliente llama a **ProcessOutput** al menos una vez.

Debe establecer marcas de tiempo y duraciones precisas para todas las muestras de entrada pasadas. Las marcas de tiempo no son estrictamente necesarias, pero ayudan a mantener la sincronización de audio y vídeo. Si no tiene las marcas de tiempo para los ejemplos, es mejor dejarlos fuera que usar valores inseguros.

## <a name="encoder-processing-example"></a>Ejemplo de procesamiento del codificador

En el código de ejemplo siguiente se muestra cómo llamar [**a IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener un ejemplo codificado. Para obtener el contexto completo de este ejemplo, vea [Código de ejemplo de codificador](encoder-example-code.md).


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

[Multiplexor de ASF](asf-multiplexer.md)
</dt> <dt>

[Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> </dl>

 

 



