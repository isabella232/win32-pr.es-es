---
description: Trabajar con ejemplos de medios
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Trabajar con ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003318"
---
# <a name="working-with-media-samples"></a><span data-ttu-id="939e9-103">Trabajar con ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="939e9-103">Working with Media Samples</span></span>

<span data-ttu-id="939e9-104">En este tema se describe cómo utilizar la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para manipular objetos de ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="939e9-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="939e9-105">Para obtener información general sobre los ejemplos de medios, consulte [ejemplos de medios](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="939e9-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="939e9-106">Para crear un nuevo ejemplo multimedia, llame a la función [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) .</span><span class="sxs-lookup"><span data-stu-id="939e9-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="939e9-107">Inicialmente, la lista de búferes del ejemplo está vacía.</span><span class="sxs-lookup"><span data-stu-id="939e9-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="939e9-108">Para agregar un búfer al final de la lista, llame a [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="939e9-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="939e9-109">En el código siguiente se muestra cómo crear un ejemplo y agregarle un búfer.</span><span class="sxs-lookup"><span data-stu-id="939e9-109">The following code shows how to create a sample and add a buffer to it.</span></span>


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="939e9-110">La manera recomendada de obtener los búferes del ejemplo es llamar a [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span><span class="sxs-lookup"><span data-stu-id="939e9-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="939e9-111">Este método devuelve un búfer continguous único.</span><span class="sxs-lookup"><span data-stu-id="939e9-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="939e9-112">Para recorrer en iteración los búferes de la lista, empiece por llamar a [**IMFSample:: GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span><span class="sxs-lookup"><span data-stu-id="939e9-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="939e9-113">Este método devuelve el número de búferes.</span><span class="sxs-lookup"><span data-stu-id="939e9-113">This method returns the number of buffers.</span></span> <span data-ttu-id="939e9-114">Después, llame a [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) y especifique el índice del búfer que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="939e9-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="939e9-115">Los búferes se indizan desde cero.</span><span class="sxs-lookup"><span data-stu-id="939e9-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="939e9-116">En el código siguiente se muestra cómo recorrer en iteración los búferes de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="939e9-116">The following code shows how to iterate through the buffers in a sample.</span></span>


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



<span data-ttu-id="939e9-117">Los ejemplos tienen una marca de tiempo y una duración.</span><span class="sxs-lookup"><span data-stu-id="939e9-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="939e9-118">La marca de tiempo indica cuándo se deben representar los datos en el ejemplo, con respecto al reloj de presentación.</span><span class="sxs-lookup"><span data-stu-id="939e9-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="939e9-119">La duración es el período de tiempo durante el que se deben representar los datos.</span><span class="sxs-lookup"><span data-stu-id="939e9-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="939e9-120">Normalmente, el componente que genera los datos establece la marca de tiempo y la duración iniciales.</span><span class="sxs-lookup"><span data-stu-id="939e9-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="939e9-121">Estos valores podrían ser modificados por la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="939e9-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="939e9-122">Para establecer la marca de tiempo, llame a [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="939e9-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="939e9-123">Para establecer la duración, llame a [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="939e9-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="939e9-124">Los ejemplos también pueden tener atributos, que contienen información adicional sobre el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="939e9-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="939e9-125">Para obtener una lista de los atributos de ejemplo, vea [atributos de ejemplo](sample-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="939e9-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="939e9-126">Para establecer y recuperar atributos, use la [**interfaz IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), que hereda [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="939e9-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="939e9-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="939e9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="939e9-128">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="939e9-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="939e9-129">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="939e9-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



