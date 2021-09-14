---
description: Relojes de referencia
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Relojes de referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251103"
---
# <a name="reference-clocks"></a>Relojes de referencia

Una función del Administrador de Graph es sincronizar todos los filtros del gráfico con el mismo reloj, denominado reloj *de referencia.*

Cualquier objeto que exponga la [**interfaz IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) puede actuar como reloj de referencia. El reloj de referencia puede proporcionarse mediante un filtro DirectShow, normalmente el representador de audio, que tiene acceso a un temporizador de hardware. Como reserva, filter Graph Manager puede usar la hora del sistema.

Nominalmente, un reloj de referencia mide el tiempo en intervalos de 100 nanosegundos, aunque la precisión real del reloj podría ser menor. Para recuperar la hora actual del reloj, llame al [**método IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) La línea base del reloj(la hora a partir de la que comienza a contar) depende de la implementación, por lo que el valor devuelto por **GetTime** no es intrínsecamente significativo. Lo que importa es la diferencia desde el momento en que el gráfico empezó a ejecutarse.

Aunque la precisión de un reloj de referencia puede variar, se garantiza que las horas devueltas por el [**método GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumentan de forma monótica. En otras palabras, las horas de reloj nunca retrocederán. Si un reloj de referencia genera horas de reloj desde un origen de hardware y el reloj de hardware salta hacia atrás (por ejemplo, si hay un ajuste en el reloj), el método **GetTime** debe seguir devolviendo la última hora notificada hasta que el reloj de hardware se activa. Para obtener más información, [**vea CBaseReferenceClock (Clase).**](cbasereferenceclock.md)

**Reloj de referencia predeterminado**

El Administrador Graph filtros selecciona automáticamente un reloj de referencia cuando se ejecuta el gráfico. Usa el algoritmo siguiente para seleccionar el reloj:

-   Si la aplicación ha seleccionado un reloj (consulte a continuación), use ese reloj.
-   Si el gráfico contiene un filtro de origen en directo que admite [**IReferenceClock,**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)use ese filtro. Para obtener la definición de un origen en directo, vea [Orígenes en directo.](live-sources.md)
-   Si el gráfico NO contiene ningún filtro de origen en directo, use cualquier filtro del gráfico que admita [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), empezando por los representadores y trabajando en sentido ascendente. Prefiere los filtros conectados en lugar de los filtros no conectados. (Si el gráfico representa una secuencia de audio, este paso del algoritmo normalmente seleccionará el filtro del representador de audio).
-   Si ningún filtro proporciona un reloj adecuado, use el reloj de [referencia del](system-reference-clock.md)sistema , que se basa en la hora del sistema.

**Establecimiento del reloj de referencia**

Una aplicación puede seleccionar un reloj llamando al [**método IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en filter Graph Manager. Debe hacerlo solo si tiene una razón determinada para preferir otro reloj.

Puede indicar al Administrador de Graph que no use un reloj de referencia llamando a [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) con el valor **NULL**. Por ejemplo, puede hacerlo para procesar ejemplos lo antes posible. Para restaurar el reloj de referencia predeterminado, llame al [**método IFilterGraph::SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) en filter Graph Manager.

Cada vez que cambia el reloj de referencia, filter Graph Manager notifica a cada filtro mediante una llamada a su [**método IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) Las aplicaciones nunca deben llamar a este método en filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecimiento del Graph reloj](setting-the-graph-clock.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



