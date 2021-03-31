---
description: Exponer los formatos de captura y compresión
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Exponer los formatos de captura y compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806878"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="9c07f-103">Exponer los formatos de captura y compresión</span><span class="sxs-lookup"><span data-stu-id="9c07f-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="9c07f-104">En este artículo se describe cómo devolver los formatos de captura y compresión mediante el método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="9c07f-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="9c07f-105">Este método puede obtener más información sobre los tipos de medios aceptados que la manera tradicional de enumerar los tipos de medios de un PIN, por lo que normalmente se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="9c07f-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="9c07f-106">**GetStreamCaps** puede devolver información sobre los tipos de formatos permitidos para audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c07f-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="9c07f-107">Además, en este artículo se proporciona código de ejemplo que muestra cómo volver a conectar la clavija de entrada de un filtro de transformación para asegurarse de que el filtro puede generar una salida determinada.</span><span class="sxs-lookup"><span data-stu-id="9c07f-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="9c07f-108">El método **GetStreamCaps** devuelve una matriz de pares de estructuras de tipo de medio y funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="9c07f-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="9c07f-109">El tipo de medio es una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y las funciones se representan mediante una estructura de [**audio de \_ flujo \_ \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) de vídeo o una estructura de Cap de configuración de [**flujo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="9c07f-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="9c07f-110">La primera sección de este artículo presenta un ejemplo de vídeo y el segundo presenta un ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="9c07f-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="9c07f-111">Ese artículo contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="9c07f-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="9c07f-112">Capacidades de vídeo</span><span class="sxs-lookup"><span data-stu-id="9c07f-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="9c07f-113">Capacidades de audio</span><span class="sxs-lookup"><span data-stu-id="9c07f-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="9c07f-114">Volver a conectar la entrada para garantizar tipos de salida específicos</span><span class="sxs-lookup"><span data-stu-id="9c07f-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="9c07f-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c07f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c07f-116">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c07f-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



