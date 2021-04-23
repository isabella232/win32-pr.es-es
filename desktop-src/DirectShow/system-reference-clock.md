---
description: Reloj de referencia del sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Reloj de referencia del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909493"
---
# <a name="system-reference-clock"></a><span data-ttu-id="12102-103">Reloj de referencia del sistema</span><span class="sxs-lookup"><span data-stu-id="12102-103">System Reference Clock</span></span>

<span data-ttu-id="12102-104">El objeto Reloj de referencia del sistema implementa un reloj de referencia que devuelve la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="12102-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="12102-105">Si ninguno de los filtros del gráfico proporciona un reloj de referencia, el administrador de gráficos de filtros usa este componente para sincronizar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="12102-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="12102-106">Cree este objeto mediante una llamada **a CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="12102-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="12102-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="12102-107">Label</span></span> | <span data-ttu-id="12102-108">Value</span><span class="sxs-lookup"><span data-stu-id="12102-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12102-109">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="12102-109">Class Identifier</span></span> | <span data-ttu-id="12102-110">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="12102-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="12102-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="12102-111">Interfaces</span></span>       | <span data-ttu-id="12102-112">[**IAMClockAdjust,**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="12102-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="12102-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12102-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12102-114">Objetos DirectShow</span><span class="sxs-lookup"><span data-stu-id="12102-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="12102-115">Relojes de referencia</span><span class="sxs-lookup"><span data-stu-id="12102-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="12102-116">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="12102-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



