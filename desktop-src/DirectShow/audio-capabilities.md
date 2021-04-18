---
description: Capacidades de audio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Capacidades de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538049"
---
# <a name="audio-capabilities"></a><span data-ttu-id="bd3b6-103">Capacidades de audio</span><span class="sxs-lookup"><span data-stu-id="bd3b6-103">Audio Capabilities</span></span>

<span data-ttu-id="bd3b6-104">En cuanto a las capacidades de audio, [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) devuelve una matriz de pares de estructuras de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y de [**\_ configuración de flujo de \_ \_ audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="bd3b6-104">For audio capabilities, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns an array of pairs of [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) and [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structures.</span></span> <span data-ttu-id="bd3b6-105">Al igual que con el vídeo, puede utilizarlo para exponer todos los tipos de funciones de audio en el PIN, como la velocidad de datos y si es compatible con mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-105">As with video, you can use this to expose all kinds of audio capabilities on the pin, such as data rate and whether it supports mono or stereo.</span></span>

<span data-ttu-id="bd3b6-106">Para ver ejemplos relacionados con GetStreamCaps, consulte capacidades de [vídeo](video-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b6-106">For video-related examples relating to GetStreamCaps, see [Video Capabilities](video-capabilities.md).</span></span>

<span data-ttu-id="bd3b6-107">Supongamos que admite el formato de onda de modulación por pulsos (PCM) (tal y como se representa en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ) en las tarifas de muestreo de 11.025, 22.050 y 44.100 muestras por segundo, todo ello en mono o estéreo de 8 o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-107">Suppose you support pulse code modulation (PCM) wave format (as represented by the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure) at sampling rates of 11,025, 22,050, and 44,100 samples per second, all at 8- or 16-bit mono or stereo.</span></span> <span data-ttu-id="bd3b6-108">En este caso, se ofrecen dos pares de estructuras.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-108">In this case, you would offer two pairs of structures.</span></span> <span data-ttu-id="bd3b6-109">El primer par tendrá una estructura de la capacidad de configuración de flujo de audio que indica que admite un mínimo de 11.025 a un máximo de 22.050 muestras por segundo con una granularidad de 11.025 muestras por segundo (la granularidad es la diferencia entre los valores admitidos). un mínimo de 8 bits a un máximo de 16 bits por muestra con una granularidad de 8 bits por muestra; y un máximo de dos canales como máximo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bd3b6-109">The first pair would have an **AUDIO\_STREAM\_CONFIG\_CAPS** capability structure saying you support a minimum of 11,025 to a maximum of 22,050 samples per second with a granularity of 11,025 samples per second (granularity is the difference between supported values); an 8-bit minimum to a 16-bit maximum bits per sample with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="bd3b6-110">El tipo de medio del primer par sería el formato PCM predeterminado en ese intervalo, quizás 22 kilohercios (kHz), estéreo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-110">The first pair's media type would be your default PCM format in that range, perhaps 22 kilohertz (kHz), 16-bit stereo.</span></span> <span data-ttu-id="bd3b6-111">El segundo par sería una funcionalidad que muestra 44.100 para las muestras mínima y máxima por segundo. bits de 8 bits (mínimo) y 16 bits (máximo) por muestra, con una granularidad de 8 bits por muestra. y un máximo de dos canales como máximo.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-111">Your second pair would be a capability showing 44,100 for both minimum and maximum samples per second; 8-bit (minimum) and 16-bit (maximum) bits per sample, with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="bd3b6-112">El tipo de medio sería el formato predeterminado 44 kHz, quizás 44 kHz de 16 bits estéreo.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-112">The media type would be your default 44 kHz format, perhaps 44 kHz 16-bit stereo.</span></span>

<span data-ttu-id="bd3b6-113">Si admite formatos de onda no PCM, el tipo de medio devuelto por este método puede mostrar los formatos que no son PCM que admite (con una velocidad de muestra predeterminada, una velocidad de bits y canales) y la estructura de capacidades que acompaña a ese tipo de medio puede describir qué tasas de ejemplo, velocidades de bits y canales admite.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-113">If you support non-PCM wave formats, the media type returned by this method can show which non-PCM formats you support (with a default sample rate, bit rate, and channels) and the capabilities structure accompanying that media type can describe which other sample rates, bit rates, and channels you support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd3b6-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd3b6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd3b6-115">Exponer los formatos de captura y compresión</span><span class="sxs-lookup"><span data-stu-id="bd3b6-115">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
