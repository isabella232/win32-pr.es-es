---
description: Horas de reloj
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de reloj
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273012"
---
# <a name="clock-times"></a>Horas de reloj

DirectShow define dos horas de reloj relacionadas: hora de referencia y hora de secuencia.

-   *La hora de* referencia es la hora absoluta devuelta por el reloj de referencia. (Vea [Relojes de referencia).](reference-clocks.md)
-   *El tiempo de* transmisión se define en relación con el momento en que el gráfico empezó a ejecutarse por última vez.
    -   Mientras se ejecuta el gráfico, el tiempo de transmisión es igual a la hora de referencia menos la hora de inicio.
    -   Mientras el gráfico está en pausa, el tiempo de transmisión permanece en el momento de la secuencia cuando se ha pausado.
    -   Después de una operación de búsqueda, el tiempo de transmisión se restablece a cero.
    -   Mientras se detiene el gráfico, el tiempo de transmisión no está definido.

Cuando un ejemplo multimedia tiene una marca de tiempo *t*, significa que el ejemplo debe representarse en el tiempo de transmisión *t*. Por esta razón, el tiempo de transmisión también se denomina tiempo *de presentación.*

Cuando una aplicación llama a [**IMediaControl::Run para**](/windows/desktop/api/Control/nf-control-imediacontrol-run) ejecutar el gráfico de filtros, filter Graph Manager llama a [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) en cada filtro. Para compensar la ligera cantidad de tiempo que tardan los filtros en empezar a ejecutarse, el Administrador de filtros Graph Especifica una hora de inicio ligeramente en el futuro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Marcas de tiempo](time-stamps.md)
</dt> </dl>

 

 



