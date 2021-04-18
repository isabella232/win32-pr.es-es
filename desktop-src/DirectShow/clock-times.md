---
description: Horas de reloj
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de reloj
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422790"
---
# <a name="clock-times"></a>Horas de reloj

DirectShow define dos horas de reloj relacionadas: tiempo de referencia y tiempo de secuencia.

-   El *tiempo de referencia* es la hora absoluta devuelta por el reloj de referencia. (Consulte [relojes de referencia](reference-clocks.md)).
-   La hora de la *secuencia* se define en relación con la última vez que se inició la ejecución del gráfico.
    -   Mientras se ejecuta el gráfico, el tiempo de secuencia es igual a la hora de referencia menos a la hora de inicio.
    -   Mientras el gráfico está en pausa, el tiempo de flujo permanece en el momento de la secuencia cuando se pausó.
    -   Después de una operación de búsqueda, el tiempo de secuencia se restablece en cero.
    -   Mientras se detiene el gráfico, el tiempo de secuencia no está definido.

Cuando un ejemplo multimedia tiene una marca de tiempo *t*, significa que el ejemplo se debe representar en el momento del flujo *t*. Por esta razón, el tiempo de flujo también se denomina *tiempo de presentación*.

Cuando una aplicación llama a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico de filtros, el administrador de gráficos de filtros llama a [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) en cada filtro. Para compensar el ligero tiempo necesario para que los filtros empiecen a ejecutarse, el administrador de gráficos de filtro especifica una hora de inicio ligeramente en el futuro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Marcas de tiempo](time-stamps.md)
</dt> </dl>

 

 



