---
description: Usar el filtro Smart Tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Usar el filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667849"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="608e5-103">Usar el filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="608e5-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="608e5-104">Si un filtro de captura tiene clavijas de captura y vista previa independientes, puede capturar desde uno mientras obtiene una vista previa del otro.</span><span class="sxs-lookup"><span data-stu-id="608e5-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="608e5-105">Pero si el filtro no tiene ningún PIN de vista previa, puede hacer lo mismo incluyendo el filtro [Smart Tee](smart-tee-filter.md) en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="608e5-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="608e5-106">Este filtro divide los datos del PIN de captura en dos flujos idénticos, uno para la captura y otro para la vista previa.</span><span class="sxs-lookup"><span data-stu-id="608e5-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="608e5-107">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="608e5-107">The following diagram illustrates this process.</span></span>

![gráfico de captura con filtro Smart Tee](images/vidcap05.png)

<span data-ttu-id="608e5-109">El método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta automáticamente el filtro de forma inteligente si es necesario.</span><span class="sxs-lookup"><span data-stu-id="608e5-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="608e5-110">Sin embargo, si usa métodos de **IGraphBuilder** para compilar el gráfico, y no **RenderStream**, puede que tenga que insertar el filtro de tee inteligente.</span><span class="sxs-lookup"><span data-stu-id="608e5-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="608e5-111">Antes de representar PIN en el filtro de captura, compruebe si el filtro tiene un PIN de vista previa o un PIN de puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="608e5-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="608e5-112">En caso contrario, y desea obtener una vista previa, agregue el filtro Smart Tee al gráfico y conéctelo al pin de captura en el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="608e5-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="608e5-113">Puede tratar un PIN de puerto de vídeo (VP) como un tipo de PIN de vista previa, por lo que un filtro con el código de VP no necesita un filtro Smart tee.</span><span class="sxs-lookup"><span data-stu-id="608e5-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="608e5-114">Sin embargo, los VP PIN tienen otros requisitos especiales.</span><span class="sxs-lookup"><span data-stu-id="608e5-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="608e5-115">Para obtener más información, consulte [pines del puerto de vídeo](video-port-pins.md).</span><span class="sxs-lookup"><span data-stu-id="608e5-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="608e5-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="608e5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="608e5-117">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="608e5-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="608e5-118">Combinación de captura de vídeo y vista previa</span><span class="sxs-lookup"><span data-stu-id="608e5-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="608e5-119">Trabajar con categorías de PIN</span><span class="sxs-lookup"><span data-stu-id="608e5-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



