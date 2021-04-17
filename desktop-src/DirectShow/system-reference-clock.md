---
description: Reloj de referencia del sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Reloj de referencia del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678187"
---
# <a name="system-reference-clock"></a><span data-ttu-id="f73ba-103">Reloj de referencia del sistema</span><span class="sxs-lookup"><span data-stu-id="f73ba-103">System Reference Clock</span></span>

<span data-ttu-id="f73ba-104">El objeto de reloj de referencia del sistema implementa un reloj de referencia que devuelve la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="f73ba-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="f73ba-105">Si ninguno de los filtros del gráfico proporciona un reloj de referencia, el administrador de gráficos de filtro utiliza este componente para sincronizar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="f73ba-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="f73ba-106">Cree este objeto llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="f73ba-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73ba-107">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="f73ba-107">Class Identifier</span></span> | <span data-ttu-id="f73ba-108">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="f73ba-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="f73ba-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f73ba-109">Interfaces</span></span>       | <span data-ttu-id="f73ba-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="f73ba-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f73ba-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f73ba-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f73ba-112">Objetos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="f73ba-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="f73ba-113">Relojes de referencia</span><span class="sxs-lookup"><span data-stu-id="f73ba-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="f73ba-114">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="f73ba-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



