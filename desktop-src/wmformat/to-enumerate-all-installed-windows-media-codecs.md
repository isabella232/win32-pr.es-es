---
title: Para enumerar todos los códecs de Windows Media instalados
description: Para enumerar todos los códecs de Windows Media instalados
ms.assetid: 651c8624-0b66-4d0e-a25f-6c4b1a94e849
keywords:
- secuencias, enumerar códecs de Windows Media instalados
- códecs, enumeraciones
- secuencias, índices de códecs
- códecs, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db9a35913dde13f563ee57d54ee5e7de87d82cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714235"
---
# <a name="to-enumerate-all-installed-windows-media-codecs"></a><span data-ttu-id="c5f27-107">Para enumerar todos los códecs de Windows Media instalados</span><span class="sxs-lookup"><span data-stu-id="c5f27-107">To Enumerate All Installed Windows Media Codecs</span></span>

<span data-ttu-id="c5f27-108">Las interfaces de información de códec utilizan índices de códec para identificar códecs individuales.</span><span class="sxs-lookup"><span data-stu-id="c5f27-108">The codec information interfaces all use codec indexes to identify individual codecs.</span></span> <span data-ttu-id="c5f27-109">Los códecs se indexan de forma independiente para audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="c5f27-109">Codecs are indexed independently for audio and for video.</span></span> <span data-ttu-id="c5f27-110">Dentro de un tipo de códec, los índices van desde 0 hasta uno menos que el número de códecs de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="c5f27-110">Within one type of codec, indexes range from 0, to one less than the number of codecs of that type.</span></span>

<span data-ttu-id="c5f27-111">En el ejemplo de código siguiente se muestra cómo obtener el índice asociado a cada códec.</span><span class="sxs-lookup"><span data-stu-id="c5f27-111">The following example code shows how to get the index associated with each codec.</span></span> <span data-ttu-id="c5f27-112">Para compilar este código en la aplicación, incluya stdio. h.</span><span class="sxs-lookup"><span data-stu-id="c5f27-112">To compile this code in your application, include stdio.h.</span></span>


```C++
HRESULT GetCodecNames(IWMCodecInfo3* pCodecInfo)
{
    HRESULT hr = S_OK;
    DWORD   cCodecs  = 0;
    WCHAR*  pwszCodecName  = NULL;
    DWORD   cchCodecName     = 0;
    
    // Retrieve the number of supported audio codecs on the system.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Audio, &cCodecs);

    if(SUCCEEDED(hr))
        printf("Number of audio codecs: %d\n\n", cCodecs);
    else
    {
        printf("Could not get the count of audio codecs.\n");
        return hr;
    }

    // Loop through all the audio codecs.
    for(DWORD dwCodecIndex = 0; dwCodecIndex < cCodecs; dwCodecIndex++)
    {
        // Get the codec name:
        // First, get the size of the name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Audio, 
                                      dwCodecIndex, 
                                      NULL, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the size of the codec name.\n");
            return hr;
        }

        // Allocate a string of the appropriate size.
        pwszCodecName = new WCHAR[cchCodecName];
        if(pwszCodecName == NULL)
        {
            printf("Could not allocate memory.\n");
            return E_OUTOFMEMORY;
        }

        // Retrieve the codec name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Audio, 
                                      dwCodecIndex, 
                                      pwszCodecName, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            delete[] pwszCodecName;
            printf("Could not get the codec name.\n");
            return hr;
        }

        // Print the codec name.
        printf("%d %S\n", dwCodecIndex, pwszCodecName);

        // Clean up for the next iteration.
        delete[] pwszCodecName;
        pwszCodecName = NULL;
        cchCodecName  = 0;
    }

    // Retrieve the number of supported video codecs on the system.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Video, &cCodecs);

    if(SUCCEEDED(hr))
        printf("\n\nNumber of video codecs: %d.\n\n", cCodecs);
    else
    {
        printf("Could not get the count of video codecs.\n");
        return hr;
    }

    // Loop through all the video codecs.
    for(dwCodecIndex = 0; dwCodecIndex < cCodecs; dwCodecIndex++)
    {
        // Get the codec name:
        // First, get the size of the name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Video, 
                                      dwCodecIndex, 
                                      NULL, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the size of the codec name.\n");
            return hr;
        }

        // Allocate a string of the appropriate size.
        pwszCodecName = new WCHAR[cchCodecName];
        if(pwszCodecName == NULL)
        {
            printf("Could not allocate memory.\n");
            return E_OUTOFMEMORY;
        }

        // Retrieve the codec name.
        hr = pCodecInfo->GetCodecName(WMMEDIATYPE_Video, 
                                      dwCodecIndex, 
                                      pwszCodecName, 
                                      &cchCodecName);
        if(FAILED(hr))
        {
            printf("Could not get the codec name.\n");
            return hr;
        }

        // Print the codec name.
        printf("%d %S\n", dwCodecIndex, pwszCodecName);

        delete[] pwszCodecName;
        pwszCodecName = NULL;
        cchCodecName  = 0;
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="c5f27-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5f27-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f27-114">**Obtención de información de configuración de la secuencia de códecs**</span><span class="sxs-lookup"><span data-stu-id="c5f27-114">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




