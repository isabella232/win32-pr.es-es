---
title: Resolución del temporizador
description: Resolución del temporizador
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- temporizadores multimedia, resolución
- temporizadores, resolución
- resolución mínima del temporizador
- resolución máxima del temporizador
- temporizadores multimedia, resolución máxima
- temporizadores, resolución máxima
- temporizadores multimedia, resolución mínima
- temporizadores, resolución mínima
- timeGetDevCaps función)
- timeBeginPeriod función)
- timeEndPeriod función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "103772528"
---
# <a name="timer-resolution"></a><span data-ttu-id="760d9-114">Resolución del temporizador</span><span class="sxs-lookup"><span data-stu-id="760d9-114">Timer Resolution</span></span>

<span data-ttu-id="760d9-115">Para determinar las resoluciones de temporizador mínima y máxima admitidas por los servicios de temporizador, utilice la función [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="760d9-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="760d9-116">Esta función rellena los miembros **wPeriodMin** y **wPeriodMax** de la estructura [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) con las resoluciones mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="760d9-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="760d9-117">Este intervalo puede variar entre equipos y plataformas de Windows.</span><span class="sxs-lookup"><span data-stu-id="760d9-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="760d9-118">Después de determinar las resoluciones de temporizador disponibles mínima y máxima, debe establecer la resolución mínima que desea que use la aplicación.</span><span class="sxs-lookup"><span data-stu-id="760d9-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="760d9-119">Use las funciones [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) y [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) para establecer y borrar esta resolución.</span><span class="sxs-lookup"><span data-stu-id="760d9-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="760d9-120">Debe hacer coincidir cada llamada a **timeBeginPeriod** con una llamada a **timeEndPeriod**, especificando la misma resolución mínima en ambas llamadas.</span><span class="sxs-lookup"><span data-stu-id="760d9-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="760d9-121">Una aplicación puede realizar varias llamadas a **timeBeginPeriod** , siempre y cuando cada llamada coincida con una llamada a **timeEndPeriod**.</span><span class="sxs-lookup"><span data-stu-id="760d9-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="760d9-122">En [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) y [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), el parámetro *uPeriod* indica la resolución mínima del temporizador, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="760d9-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="760d9-123">Puede especificar cualquier valor de resolución del temporizador en el intervalo admitido por el temporizador.</span><span class="sxs-lookup"><span data-stu-id="760d9-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="760d9-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="760d9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="760d9-125">Acerca de los temporizadores multimedia</span><span class="sxs-lookup"><span data-stu-id="760d9-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




