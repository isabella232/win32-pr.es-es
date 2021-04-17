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
# <a name="system-reference-clock"></a>Reloj de referencia del sistema

El objeto de reloj de referencia del sistema implementa un reloj de referencia que devuelve la hora del sistema. Si ninguno de los filtros del gráfico proporciona un reloj de referencia, el administrador de gráficos de filtro utiliza este componente para sincronizar el gráfico. Cree este objeto llamando a **CoCreateInstance**.



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de clase | CLSID \_ SystemClock                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de DirectShow](directshow-objects.md)
</dt> <dt>

[Relojes de referencia](reference-clocks.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



