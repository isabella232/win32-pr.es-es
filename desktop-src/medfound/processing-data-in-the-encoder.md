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
# <a name="processing-data-in-the-encoder"></a><span data-ttu-id="d2430-103">Procesamiento de datos en el codificador</span><span class="sxs-lookup"><span data-stu-id="d2430-103">Processing Data in the Encoder</span></span>

<span data-ttu-id="d2430-104">Después de haber negociado el tipo de entrada y el tipo de salida de la MFT del codificador, tal y como se describe en [negociación de tipos multimedia en el codificador](media-type-negotiation-on-the-encoder.md), puede empezar a procesar muestras de datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d2430-104">After you have negotiated the input type and output type for the encoder MFT, as described in [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md), you can start processing media data samples.</span></span> <span data-ttu-id="d2430-105">Los datos se pasan en forma de muestras de medios (interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) y también se reciben del resultado como muestras de medios.</span><span class="sxs-lookup"><span data-stu-id="d2430-105">The data is passed in form of media samples ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) and also received from the output as media samples.</span></span>

<span data-ttu-id="d2430-106">Antes de enviar datos al codificador para su procesamiento, debe asignar un ejemplo multimedia y agregar uno o varios búferes multimedia que contengan los datos multimedia que deben codificarse.</span><span class="sxs-lookup"><span data-stu-id="d2430-106">Before sending data to the encoder for processing, you must allocate a media sample and add one of more media buffers containing media data that needs to be encoded.</span></span> <span data-ttu-id="d2430-107">Llame a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y pase un puntero al ejemplo de medios asignados.</span><span class="sxs-lookup"><span data-stu-id="d2430-107">Call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and pass a pointer to the allocated media sample.</span></span> <span data-ttu-id="d2430-108">Además del ejemplo multimedia, **ProcessInput** también necesita el identificador del flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="d2430-108">In addition to the media sample, **ProcessInput** also needs the input stream identifier.</span></span> <span data-ttu-id="d2430-109">Para obtener el identificador de flujo, llame a [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span><span class="sxs-lookup"><span data-stu-id="d2430-109">To get the stream identifier, call [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span></span> <span data-ttu-id="d2430-110">Dado que un codificador está diseñado para tener solo una salida y una, estos identificadores de flujo siempre tienen el valor 0.</span><span class="sxs-lookup"><span data-stu-id="d2430-110">Because an encoder is designed to have only one and one output, these stream identifiers always have the value of 0.</span></span>

<span data-ttu-id="d2430-111">Para obtener datos del codificador, llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="d2430-111">To get data from the encoder, call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="d2430-112">Antes de llamar a [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), debe averiguar si el codificador asigna los ejemplos de medios de salida o debe hacerlo explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d2430-112">Before you call [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), you need to find out whether the encoder allocates the output media samples or you must do so explicitly.</span></span> <span data-ttu-id="d2430-113">Para ello, llame a [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span><span class="sxs-lookup"><span data-stu-id="d2430-113">To do this, call [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span></span> <span data-ttu-id="d2430-114">Esto devuelve información de ejemplo multimedia de salida en la estructura de [**información del flujo de salida de MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) .</span><span class="sxs-lookup"><span data-stu-id="d2430-114">This returns output media sample information in the [**MFT\_OUTPUT\_STREAM\_INFO**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) structure.</span></span> <span data-ttu-id="d2430-115">Si el codificador asigna ejemplos de medios, devuelve el flujo de salida de \_ MFT \_ proporciona \_ la \_ marca samples en el miembro **dwFlags** y el miembro **cbSize** contiene cero.</span><span class="sxs-lookup"><span data-stu-id="d2430-115">If the encoder allocates media samples, it returns the MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES flag in the **dwFlags** member and the **cbSize** member contains zero.</span></span> <span data-ttu-id="d2430-116">Si el codificador espera que asigne el búfer de salida, cree el ejemplo multimedia de salida y el búfer de medios asociado en función del tamaño devuelto en **cbSize**.</span><span class="sxs-lookup"><span data-stu-id="d2430-116">If the encoder expects you to allocate the output buffer, create the output media sample and the associated media buffer based on the size returned in **cbSize**.</span></span> <span data-ttu-id="d2430-117">Cuando llame a [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pase un puntero al ejemplo multimedia que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="d2430-117">When you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pass a pointer to the newly created media sample.</span></span> <span data-ttu-id="d2430-118">Durante la sesión de codificación, el codificador llena los búferes multimedia, señalados por el ejemplo multimedia de salida, con los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="d2430-118">During the encoding session, the encoder fills the media buffers, pointed by the output media sample, with the encoded data.</span></span>

<span data-ttu-id="d2430-119">Para iniciar la sesión de codificación, pase el ejemplo de medios de entrada al codificador mediante una llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="d2430-119">To start the encoding session, pass the input media sample to the encoder by calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="d2430-120">El codificador comienza el procesamiento y los datos, y genera uno o más ejemplos de medios de salida que se deben recuperar mediante [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) siempre que devuelva la \_ transformación MF E \_ \_ necesite \_ más \_ entrada.</span><span class="sxs-lookup"><span data-stu-id="d2430-120">The encoder starts processing and the data and produces one or more output media samples that must be retrieved by [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) as long as it returns MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT.</span></span> <span data-ttu-id="d2430-121">Si llama a **ProcessInput** para pasar más entradas mientras haya datos de salida que se van a recuperar, **ProcessInput** producirá un error con MF \_ E \_ NOTACCEPTING.</span><span class="sxs-lookup"><span data-stu-id="d2430-121">If you call **ProcessInput** to pass more input as long as there is output data to be retrieved, **ProcessInput** fails with MF\_E\_NOTACCEPTING.</span></span> <span data-ttu-id="d2430-122">El codificador no acepta más entradas hasta que el cliente llama a **ProcessOutput** al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="d2430-122">The encoder does not accept any more input until the client calls **ProcessOutput** at least once.</span></span>

<span data-ttu-id="d2430-123">Debe establecer las marcas de tiempo y duraciones precisas para todos los ejemplos de entrada pasados.</span><span class="sxs-lookup"><span data-stu-id="d2430-123">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="d2430-124">Las marcas de tiempo no son estrictamente necesarias pero ayudan a mantener la sincronización de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2430-124">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="d2430-125">Si no dispone de las marcas de tiempo para los ejemplos, es mejor dejarlas de usar valores inciertos.</span><span class="sxs-lookup"><span data-stu-id="d2430-125">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="encoder-processing-example"></a><span data-ttu-id="d2430-126">Ejemplo de procesamiento del codificador</span><span class="sxs-lookup"><span data-stu-id="d2430-126">Encoder Processing Example</span></span>

<span data-ttu-id="d2430-127">En el ejemplo de código siguiente se muestra cómo llamar a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener un ejemplo codificado.</span><span class="sxs-lookup"><span data-stu-id="d2430-127">The following example code shows how to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get an encoded sample.</span></span> <span data-ttu-id="d2430-128">Para obtener el contexto completo de este ejemplo, vea [código de ejemplo del codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="d2430-128">For the complete context of this example, see [Encoder Example Code](encoder-example-code.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d2430-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2430-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2430-130">Multiplexor ASF</span><span class="sxs-lookup"><span data-stu-id="d2430-130">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="d2430-131">Crear instancias de una MFT del codificador</span><span class="sxs-lookup"><span data-stu-id="d2430-131">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="d2430-132">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="d2430-132">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



