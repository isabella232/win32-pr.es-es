---
description: Formato de secuencia
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688211"
---
# <a name="stream-format"></a><span data-ttu-id="2d1e5-103">Formato de secuencia</span><span class="sxs-lookup"><span data-stu-id="2d1e5-103">Stream Format</span></span>

<span data-ttu-id="2d1e5-104">Tanto el controlador MSDV como el controlador UVC pueden generar dos formatos DV: vídeo de audio entrelazado o vídeo.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="2d1e5-105">Audio entrelazado: vídeo es el formato original del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="2d1e5-106">El formato de solo vídeo contiene los mismos datos, pero los ejemplos se marcan como sin datos de audio.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="2d1e5-107">El formato de solo vídeo existe principalmente para la compatibilidad con aplicaciones que usan vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="2d1e5-108">Para obtener más información, consulte [archivos AVI de tipo 1 frente a tipo-2](type-1-vs--type-2-dv-avi-files.md).</span><span class="sxs-lookup"><span data-stu-id="2d1e5-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="2d1e5-109">**Controlador MSDV**</span><span class="sxs-lookup"><span data-stu-id="2d1e5-109">**MSDV Driver**</span></span>

<span data-ttu-id="2d1e5-110">El controlador MSDV tiene dos clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="2d1e5-111">El primer PIN de salida envía datos intercalados y el segundo solo envía datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="2d1e5-112">Solo se puede conectar un PIN de salida a la vez.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="2d1e5-113">Para seleccionar un formato, conecte el PIN de salida adecuado.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="2d1e5-114">Puede usar la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en el PIN de salida para buscar el formato.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="2d1e5-115">**Controlador UVC**</span><span class="sxs-lookup"><span data-stu-id="2d1e5-115">**UVC Driver**</span></span>

<span data-ttu-id="2d1e5-116">A diferencia del controlador MSDV, el controlador UVC proporciona ambos formatos del mismo pin.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="2d1e5-117">El formato predeterminado es solo vídeo.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-117">The default format is video-only.</span></span> <span data-ttu-id="2d1e5-118">Para seleccionar el formato, use la interfaz **IAMStreamConfig** en el terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="2d1e5-119">Llame al método **GetStreamCaps** para enumerar los tipos de medios en el terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="2d1e5-120">Para cada tipo de medio, si el tipo principal coincide con el formato deseado, llame a **SetFormat** y pase dicho tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="2d1e5-121">Formato</span><span class="sxs-lookup"><span data-stu-id="2d1e5-121">Format</span></span>                      | <span data-ttu-id="2d1e5-122">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="2d1e5-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="2d1e5-123">Audio y vídeo intercalados</span><span class="sxs-lookup"><span data-stu-id="2d1e5-123">Interleaved audio and video</span></span> | <span data-ttu-id="2d1e5-124">MEDIATYPE \_ intercalado</span><span class="sxs-lookup"><span data-stu-id="2d1e5-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="2d1e5-125">Solo vídeo</span><span class="sxs-lookup"><span data-stu-id="2d1e5-125">Video only</span></span>                  | <span data-ttu-id="2d1e5-126">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="2d1e5-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="2d1e5-127">La función siguiente establece el formato basado en el GUID de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="2d1e5-128">El controlador MSDV también admite **IAMStreamConfig**, por lo que puede escribir código que funcione para ambos tipos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d1e5-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d1e5-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d1e5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d1e5-130">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="2d1e5-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



