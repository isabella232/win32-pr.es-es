---
title: Para buscar formatos de audio
description: Para buscar formatos de audio
ms.assetid: f2001ed5-f07d-45a5-a566-45697024870e
keywords:
- flujos, buscar formatos de audio
- secuencias de audio, buscar formatos de audio
- secuencias, formatos de audio
- secuencias de audio, formatos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85897d4d76a3bdb1e99902eb4f52336a3ad0874
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359179"
---
# <a name="to-find-audio-formats"></a><span data-ttu-id="2f52c-107">Para buscar formatos de audio</span><span class="sxs-lookup"><span data-stu-id="2f52c-107">To Find Audio Formats</span></span>

<span data-ttu-id="2f52c-108">En el ejemplo de código siguiente se muestra cómo buscar un formato de audio que coincida con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="2f52c-108">The following example code demonstrates how to find an audio format that matches criteria you specify.</span></span> <span data-ttu-id="2f52c-109">La función **FindAudioFormat** acepta un puntero a una estructura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) que contiene el número de canales, bits por muestra y la velocidad de muestra que desea usar.</span><span class="sxs-lookup"><span data-stu-id="2f52c-109">The **FindAudioFormat** function accepts a pointer to a [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure that contains the number of channels, bits per sample, and sample rate that you want to use.</span></span> <span data-ttu-id="2f52c-110">La función busca el formato que coincide con esos requisitos y tiene la velocidad de bits más alta que no supera el parámetro *dwMaxRate* .</span><span class="sxs-lookup"><span data-stu-id="2f52c-110">The function finds the format that matches those requirements and has the highest bit rate that does not exceed the *dwMaxRate* parameter.</span></span> <span data-ttu-id="2f52c-111">Si establece *fAVSync* en **true**, la función solo valida los formatos que se pueden sincronizar con vídeo.</span><span class="sxs-lookup"><span data-stu-id="2f52c-111">If you set *fAVSync* to **TRUE**, the function only validates formats that can be synchronized with video.</span></span> <span data-ttu-id="2f52c-112">Para simplificar, esta función solo funciona con formatos CBR de 1 paso.</span><span class="sxs-lookup"><span data-stu-id="2f52c-112">For simplicity, this function only works with 1-pass CBR formats.</span></span>


```C++
// This constant is used to determine if an index was found.
#define INVALID_INDEX 0xFFFF

// The FindAudioFormat function finds a compressed audio format that
//  matches the criteria defined by the input parameters.
HRESULT FindAudioFormat(GUID SubType,
                        WAVEFORMATEX* pWaveLimits,
                        DWORD dwMaxRate,
                        BOOL fAVSync,
                        IWMStreamConfig** ppStreamConfig)
{
    HRESULT hr = S_OK;

    IWMProfileManager* pProfileMgr   = NULL;
    IWMCodecInfo3*     pCodecInfo    = NULL;
    IWMStreamConfig*   pStreamConfig = NULL;
    IWMStreamConfig*   pBestMatch    = NULL;
    IWMMediaProps*     pProps        = NULL;
    WM_MEDIA_TYPE*     pType         = NULL;
    DWORD              cbType        = 0;
    WAVEFORMATEX*      pWave         = NULL;

    DWORD index = 0;
    DWORD cEntries = 0;
    DWORD dwBestRate = 0;
    DWORD PacketsPerSecond = 0;

    // This value is beyond the codec indexes 
    // and will be used to verify success.
    DWORD CodecIndex = INVALID_INDEX; 

    // Instantiate a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the codec information interface.
    hr = pProfileMgr->QueryInterface(IID_IWMCodecInfo3, (void**)&pCodecInfo);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of audio codecs for which there is information.
    hr = pCodecInfo->GetCodecInfoCount(WMMEDIATYPE_Audio, &cEntries);
    GOTO_EXIT_IF_FAILED(hr);

    // Find the index of the codec corresponding to the requested subytpe.
    for(index = 0; index < cEntries; index++)
    {
        // Get the first format for each codec. 
        hr = pCodecInfo->GetCodecFormat(WMMEDIATYPE_Audio, index, 0, &pStreamConfig);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the media properties interface.
        hr = pStreamConfig->QueryInterface(IID_IWMMediaProps, (void**)&pProps);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size required for the media type structure.
        hr = pProps->GetMediaType(NULL, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new BYTE[cbType];
        if(pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Check this codec against the one requested.
        if(pType->subtype == SubType)
            CodecIndex = index;
        
        // The subtypes did not match. Clean up for next iteration.
        SAFE_RELEASE(pStreamConfig);
        SAFE_RELEASE(pProps);
        SAFE_ARRAY_DELETE(pType);

        // Break now if needed. Placing the break here avoids having to
        //  release or delete both inside and outside of the loop.
        if(CodecIndex != INVALID_INDEX)
            break;
    } // for index

    // The subtype is invalid if no codec was found that matches it.
    if(CodecIndex == INVALID_INDEX)
    {
        hr = E_INVALIDARG;
        goto Exit;
    }

    // Get the number of formats supported for the codec.
    hr = pCodecInfo->GetCodecFormatCount(WMMEDIATYPE_Audio, 
                                         CodecIndex, 
                                         &cEntries);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through the formats for the codec, looking for matches.
    for(index = 0; index < cEntries; index++)
    {
        // Get the next format.
        hr = pCodecInfo->GetCodecFormat(WMMEDIATYPE_Audio, 
                                        CodecIndex, 
                                        index, 
                                        &pStreamConfig);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the media properties interface.
        hr = pStreamConfig->QueryInterface(IID_IWMMediaProps, (void**)&pProps);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size required for the media type structure.
        hr = pProps->GetMediaType(NULL, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new BYTE[cbType];
        if(pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbType);
        GOTO_EXIT_IF_FAILED(hr);

        // Check that the format data is present.
        if(pType->cbFormat >= sizeof(WAVEFORMATEX))
            pWave = (WAVEFORMATEX*)pType->pbFormat;
        else
        {
            // The returned media type should always have an attached 
            //  WAVEFORMATEX structure.  
            hr = E_UNEXPECTED;
            goto Exit;
        }

        // Start checking data.

        // Do not check particulars unless the bit rate is in range.
        if((pWave->nAvgBytesPerSec * 8) > dwBestRate &&
           (pWave->nAvgBytesPerSec * 8) <= dwMaxRate)
        {
            // Check the limits.
            if((pWave->nChannels == pWaveLimits->nChannels) &&
               (pWave->wBitsPerSample == pWaveLimits->wBitsPerSample) &&
               (pWave->nSamplesPerSec == pWaveLimits->nSamplesPerSec))
            {
                // If audio/video synchronization requested, check the number
                //  of packets per second (Bps / BlockAlign). The bit rate is
                //  greater than 3200 bps, this value must be 5. 
                //  Otherwise this value is 3.
                // This is an ASF requirement.
                if(fAVSync)
                {
                    if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
                           ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
                    {
                        // Release the previous best match.
                        SAFE_RELEASE(pBestMatch);

                        // Set this stream configuration as the new best match.
                        pBestMatch = pStreamConfig;
                        pStreamConfig->AddRef();

                        // Set the best bit rate.
                        dwBestRate = (pWave->nAvgBytesPerSec * 8);

                    }
                } // if fAVSync
                else
                {
                    // Release the previous best match.
                    SAFE_RELEASE(pBestMatch);

                    // Set this stream configuration as the new best match.
                    pBestMatch = pStreamConfig;
                    pStreamConfig->AddRef();

                    // Set the best bit rate.
                    dwBestRate = (pWave->nAvgBytesPerSec * 8);
                } // else
            } // if matching limits
        } // if valid bit rate

        // Clean up for next iteration.
        SAFE_RELEASE(pStreamConfig);
        SAFE_RELEASE(pProps);
        pWave = NULL;
        SAFE_ARRAY_DELETE(pType);
    } // for index

    // If no match was found, the arguments were not valid for the codec.
    if(pBestMatch == NULL)
    {
        hr = E_INVALIDARG;
        goto Exit;
    }

    // Set the pointer to the stream configuration.
    *ppStreamConfig = pBestMatch;
    pBestMatch = NULL;

Exit:
    SAFE_RELEASE(pProfileMgr);
    SAFE_RELEASE(pCodecInfo);
    SAFE_RELEASE(pStreamConfig);
    SAFE_RELEASE(pBestMatch);
    SAFE_RELEASE(pProps);
    SAFE_ARRAY_DELETE(pType);

    return hr;        
}
```



## <a name="related-topics"></a><span data-ttu-id="2f52c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f52c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f52c-114">**Configuración de secuencias de audio**</span><span class="sxs-lookup"><span data-stu-id="2f52c-114">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="2f52c-115">**Para enumerar formatos de códecs**</span><span class="sxs-lookup"><span data-stu-id="2f52c-115">**To Enumerate Codec Formats**</span></span>](to-enumerate-codec-formats.md)
</dt> </dl>

 

 