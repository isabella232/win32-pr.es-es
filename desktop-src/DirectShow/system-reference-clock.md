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
# <a name="system-reference-clock"></a>Reloj de referencia del sistema

El objeto Reloj de referencia del sistema implementa un reloj de referencia que devuelve la hora del sistema. Si ninguno de los filtros del gráfico proporciona un reloj de referencia, el administrador de gráficos de filtros usa este componente para sincronizar el gráfico. Cree este objeto mediante una llamada **a CoCreateInstance**.



| Etiqueta | Value |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de clase | CLSID \_ SystemClock                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust,**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos DirectShow](directshow-objects.md)
</dt> <dt>

[Relojes de referencia](reference-clocks.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



