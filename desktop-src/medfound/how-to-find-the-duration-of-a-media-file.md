---
description: Cómo buscar la duración de un archivo multimedia.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Cómo buscar la duración de un archivo multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547363"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="e0834-103">Cómo buscar la duración de un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="e0834-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="e0834-104">Para buscar la duración de un archivo multimedia, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0834-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="e0834-105">Utilice el [solucionador de origen](source-resolver.md) para crear un origen de medios que pueda analizar el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="e0834-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="e0834-106">Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="e0834-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="e0834-107">Este método devuelve el descriptor de presentación que describe el contenido del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="e0834-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="e0834-108">Consulte en el descriptor de presentación el atributo de [ \_ \_ duración MF PD](mf-pd-duration-attribute.md) llamando al método [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) .</span><span class="sxs-lookup"><span data-stu-id="e0834-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="e0834-109">El valor del atributo, si está presente, es la duración del archivo en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e0834-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e0834-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0834-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0834-111">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="e0834-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



