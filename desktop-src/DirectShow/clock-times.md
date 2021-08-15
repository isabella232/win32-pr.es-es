---
description: Horas de reloj
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de reloj
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0075dc2d8c2273c8ade612244f0f7d551996756e55000043ffe3bc952227fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402075"
---
# <a name="clock-times"></a>Horas de reloj

DirectShow define dos horas de reloj relacionadas: la hora de referencia y la hora de transmisión.

-   *La hora de* referencia es la hora absoluta devuelta por el reloj de referencia. (Vea [Relojes de referencia).](reference-clocks.md)
-   *El tiempo de* secuencia se define en relación con el momento en que el gráfico empezó a ejecutarse por última vez.
    -   Mientras se ejecuta el gráfico, el tiempo de secuencia es igual a la hora de referencia menos la hora de inicio.
    -   Mientras el gráfico está en pausa, el tiempo de secuencia permanece en el momento de la secuencia cuando se ha pausado.
    -   Después de una operación de búsqueda, el tiempo de transmisión se restablece en cero.
    -   Mientras se detiene el gráfico, el tiempo de transmisión no está definido.

Cuando un ejemplo multimedia tiene una marca de tiempo *t*, significa que la muestra debe representarse en tiempo de transmisión *t*. Por esta razón, el tiempo de transmisión también se denomina tiempo *de presentación.*

Cuando una aplicación llama [**a IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico de filtros, el Administrador de filtros Graph llama a [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) en cada filtro. Para compensar la ligera cantidad de tiempo que tardan los filtros en empezar a ejecutarse, el Administrador de filtros Graph especifica una hora de inicio ligeramente en el futuro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Marcas de tiempo](time-stamps.md)
</dt> </dl>

 

 



