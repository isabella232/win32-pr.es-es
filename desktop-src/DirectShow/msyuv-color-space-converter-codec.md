---
description: MSYUV es un códec de convertidor de espacio de colores YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: MSYUV codec del convertidor de espacio de colores
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690915"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="7a30d-103">MSYUV codec del convertidor de espacio de colores</span><span class="sxs-lookup"><span data-stu-id="7a30d-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="7a30d-104">MSYUV es un códec de convertidor de espacio de colores YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="7a30d-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="7a30d-105">Permite la reproducción de datos de origen de vídeo en formatos YUV en clientes cuyo adaptador de pantalla de vídeo no se puede usar para conversiones de YUV a RGB en hardware.</span><span class="sxs-lookup"><span data-stu-id="7a30d-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="7a30d-106">El códec participa en los gráficos de filtros a través del filtro de contenedor de [descompresor de AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7a30d-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="7a30d-107">Las cámaras de conferencia digital con interfaces 1394 o USB pueden generar datos de imagen en varios formatos YUV.</span><span class="sxs-lookup"><span data-stu-id="7a30d-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="7a30d-108">Si el hardware de pantalla no es compatible con la conversión de YUV a RGB incorporada, o si no se puede usar la funcionalidad de conversión de hardware por algún otro motivo, los datos de la imagen YUV se deben convertir al formato RGB antes de enviarlos al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a30d-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="7a30d-109">Debido al requisito del [representador de vídeo](video-renderer-filter.md)para un tipo de entrada RGB en el momento de la conexión, este filtro podría insertarse en un gráfico de nivel superior desde el representador de vídeo durante la creación automática del gráfico.</span><span class="sxs-lookup"><span data-stu-id="7a30d-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="7a30d-110">En concreto, si el generador de gráficos detecta un formato YUV en el tipo de medio del PIN de salida del filtro de nivel superior, el generador de gráficos insertará el descompresor de AVI, que, a continuación, cargará el códec MSYUV y lo configurará inicialmente para realizar la conversión a RGB.</span><span class="sxs-lookup"><span data-stu-id="7a30d-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="7a30d-111">Después de que el gráfico pase por primera vez a un estado de ejecución o en pausa, el filtro de representador de vídeo puede detectar si el adaptador de pantalla de vídeo puede realizar la conversión en hardware.</span><span class="sxs-lookup"><span data-stu-id="7a30d-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="7a30d-112">Si es posible, se notifica al descompresor de AVI y vuelve a configurar MSYUV para que funcione en "modo de paso a través", que hace que el códec omita la conversión y copie los datos de imagen YUV directamente en una superficie de superposición de DirectDraw en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a30d-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="7a30d-113">Dado que los representadores de mezcla de vídeo (VMR-7 y VMR-9) nunca usan GDI, no requieren un tipo RGB en el momento de la conexión y el convertidor de espacio de colores MSYUV nunca se inserta antes de la VMR en un gráfico.</span><span class="sxs-lookup"><span data-stu-id="7a30d-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="7a30d-114">MSYUV convierte los formatos YUV empaquetados en RGB, tal como se muestra en la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="7a30d-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="7a30d-115">Formatos de entrada: UYVY, YUY2, YVYU</span><span class="sxs-lookup"><span data-stu-id="7a30d-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="7a30d-116">Formatos de salida: RGB 8, RGB 16, RGB 24, RGB 32</span><span class="sxs-lookup"><span data-stu-id="7a30d-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="7a30d-117">El códec de convertidor de espacio de colores MSYUV es un códec de administrador de compresión de vídeo (VCM).</span><span class="sxs-lookup"><span data-stu-id="7a30d-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="7a30d-118">Se usa en DirectShow a través del filtro de [descompresor de AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7a30d-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="7a30d-119">Para un convertidor de colores de uso general, use el [**convertidor de colores DSP**](../medfound/colorconverter.md).</span><span class="sxs-lookup"><span data-stu-id="7a30d-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a30d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a30d-120">Requirements</span></span>



| <span data-ttu-id="7a30d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a30d-121">Requirement</span></span> | <span data-ttu-id="7a30d-122">Value</span><span class="sxs-lookup"><span data-stu-id="7a30d-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a30d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a30d-123">DLL</span></span><br/> | <dl> <span data-ttu-id="7a30d-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a30d-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a30d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a30d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a30d-126">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a30d-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
