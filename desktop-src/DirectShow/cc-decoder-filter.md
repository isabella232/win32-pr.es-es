---
description: Filtro del descodificador de CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro del descodificador de CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997712"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="2be71-103">Filtro del descodificador de CC</span><span class="sxs-lookup"><span data-stu-id="2be71-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2be71-104">Este componente se ha quitado de Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="2be71-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="2be71-105">Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2be71-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="2be71-106">El descodificador de la secuencia de CC es un filtro de clase de flujo de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="2be71-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="2be71-107">Aparece en GraphEdit en la categoría "códecs de WDM streaming VBI".</span><span class="sxs-lookup"><span data-stu-id="2be71-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="2be71-108">Acepta las forma de onda de ejemplo entregadas por un filtro de captura y entrega los datos de subtítulos cerrados descodificados en el [descodificador de la línea 21](line-21-decoder-filter.md) y/o en las aplicaciones interesadas.</span><span class="sxs-lookup"><span data-stu-id="2be71-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="2be71-109">Este filtro tiene dos clavijas de entrada, VBI y HWCC.</span><span class="sxs-lookup"><span data-stu-id="2be71-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="2be71-110">El PIN VBI se usa para los datos de VBI sin procesar y el PIN HWCC se usa cuando el filtro de captura realiza la descodificación de VBI en el hardware.</span><span class="sxs-lookup"><span data-stu-id="2be71-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="2be71-111">Cuando los datos se reciben en el PIN de HWCC, el descodificador de CC funciona en modo de "paso a través" y envía los datos directamente al descodificador de la línea 21 sin procesarlos de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="2be71-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="2be71-112">Si el filtro de captura expone un PIN de HWCC, debe estar conectado directamente al pin correspondiente en el descodificador de CC.</span><span class="sxs-lookup"><span data-stu-id="2be71-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="2be71-113">La categoría PIN es **PINNAME \_ video \_ CC \_ Capture**.</span><span class="sxs-lookup"><span data-stu-id="2be71-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="2be71-114">El descodificador de CC tiene hasta ocho clavijas de salida, cada una de las cuales puede seleccionar sus propias líneas y subflujos.</span><span class="sxs-lookup"><span data-stu-id="2be71-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="2be71-115">El primer PIN de salida se conecta al descodificador line-21.</span><span class="sxs-lookup"><span data-stu-id="2be71-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="2be71-116">El filtro descodificador de CC aparece en la categoría de filtro "códecs de WDM streaming VBI" (**AM \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="2be71-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="2be71-117">Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="2be71-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="2be71-118">En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="2be71-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="2be71-119">Para obtener más información, vea [crear filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2be71-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2be71-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2be71-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2be71-121">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2be71-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="2be71-122">Ver subtítulos (CC)</span><span class="sxs-lookup"><span data-stu-id="2be71-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



