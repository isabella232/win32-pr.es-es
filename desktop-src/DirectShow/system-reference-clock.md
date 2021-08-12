---
description: Reloj de referencia del sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Reloj de referencia del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651845"
---
# <a name="system-reference-clock"></a>Reloj de referencia del sistema

El objeto Reloj de referencia del sistema implementa un reloj de referencia que devuelve la hora del sistema. Si ninguno de los filtros del gráfico proporciona un reloj de referencia, el administrador de gráficos de filtros usa este componente para sincronizar el gráfico. Cree este objeto mediante una llamada **a CoCreateInstance**.



| Etiqueta | Value |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de clase | CLSID \_ SystemClock                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Objetos](directshow-objects.md)
</dt> <dt>

[Relojes de referencia](reference-clocks.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



