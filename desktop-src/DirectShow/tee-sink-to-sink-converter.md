---
description: Convertidor Tee/Sink-to-Sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertidor Tee/Sink-to-Sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678257"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="3c398-103">Convertidor Tee/Sink-to-Sink</span><span class="sxs-lookup"><span data-stu-id="3c398-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="3c398-104">El convertidor Tee/Sink-to-Sink es un filtro basado en KsProxy y en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="3c398-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="3c398-105">Se usa en gráficos de filtro de televisión de vídeo analógico donde se representan o capturan datos de VBI.</span><span class="sxs-lookup"><span data-stu-id="3c398-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="3c398-106">El filtro se conecta ascendente al filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) y proporciona un medio eficaz para duplicar secuencias de datos en modo kernel sin las transiciones costosas entre el modo kernel y el usuario.</span><span class="sxs-lookup"><span data-stu-id="3c398-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="3c398-107">Proporciona cada bloque de datos recibido a todos los pin de salida, y el códec de bajada es responsable de buscar los datos de VBI específicos que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="3c398-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="3c398-108">El convertidor Tee/Sink-to-Sink aparece en la categoría de filtro "dispositivos de transmisión por secuencias WDM y divisora" ( \_ KSCATEGORY \_ ).</span><span class="sxs-lookup"><span data-stu-id="3c398-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="3c398-109">Dado que se trata de un filtro en modo kernel, las aplicaciones no pueden crearlo directamente mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3c398-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="3c398-110">En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="3c398-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="3c398-111">Para obtener más información, vea [crear filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3c398-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c398-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c398-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c398-113">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c398-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
