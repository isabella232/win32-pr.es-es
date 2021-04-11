---
description: Filtro de códec de elemento WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro de códec de elemento WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361558"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="9f9fc-103">Filtro de códec de elemento WST</span><span class="sxs-lookup"><span data-stu-id="9f9fc-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f9fc-104">Este componente se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="9f9fc-105">Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="9f9fc-106">A partir de Windows Vista, este filtro se sustituye por el filtro VBICodec, que se documenta en la documentación de las tecnologías de Microsoft TV.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="9f9fc-107">El teletexto estándar mundial (elemento WST) es el estándar europeo para la transmisión de datos mediante VBI en señales de televisión analógica PAL.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="9f9fc-108">Los servicios de subtítulos y de datos se proporcionan mediante este estándar.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="9f9fc-109">El códec elemento WST es un filtro de modo kernel que recibe muestras de VBI sin procesar y, opcionalmente, muestras de teletexto descodificadas del filtro de captura a través del filtro de [convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md) .</span><span class="sxs-lookup"><span data-stu-id="9f9fc-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="9f9fc-110">Este códec descodifica y/o duplica los datos de teletexto descodificados y con corrección de errores de reenvío para el filtro de [descodificador de elemento WST](wst-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9f9fc-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="9f9fc-111">El códec elemento WST se corresponde con el filtro del descodificador de CC para las transmisiones NTSC.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="9f9fc-112">El descodificador de elemento WST corresponde al [descodificador de línea 21](line-21-decoder-filter.md) para NTSC; Estos filtros crean los mapas de bits que se envían al mezclador de superposición o al representador de mezcla de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="9f9fc-113">Este filtro tiene dos clavijas de entrada, VBI y HWCC.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="9f9fc-114">El PIN VBI se usa para los datos de VBI sin procesar y el PIN HWCC se usa cuando el filtro de captura realiza la descodificación de VBI en el hardware.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="9f9fc-115">Cuando los datos se reciben en el PIN HWCC, el códec elemento WST funciona en modo de "paso a través" y envía los datos directamente al descodificador elemento WST sin procesarlos de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="9f9fc-116">Si el filtro de captura expone un PIN HWCC, debe estar conectado directamente al pin correspondiente en el códec elemento WST.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="9f9fc-117">El filtro de códecs de elemento WST aparece en la categoría de filtro "códecs de WDM streaming VBI" (**AM \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="9f9fc-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="9f9fc-118">Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="9f9fc-119">En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="9f9fc-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="9f9fc-120">Para obtener más información, vea [crear filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9f9fc-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f9fc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f9fc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f9fc-122">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f9fc-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="9f9fc-123">Ver teletexto estándar del mundo</span><span class="sxs-lookup"><span data-stu-id="9f9fc-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



