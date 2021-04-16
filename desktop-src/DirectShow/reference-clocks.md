---
description: Relojes de referencia
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Relojes de referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677094"
---
# <a name="reference-clocks"></a>Relojes de referencia

Una función del administrador de gráficos de filtros es sincronizar todos los filtros del gráfico con el mismo reloj, denominado el *reloj de referencia*.

Cualquier objeto que exponga la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) puede actuar como el reloj de referencia. El reloj de referencia puede proporcionarse mediante un filtro de DirectShow, normalmente el representador de audio, que tiene acceso a un temporizador de hardware. Como reserva, el administrador de gráficos de filtro puede usar la hora del sistema.

Nominalmente, un reloj de referencia mide el tiempo en intervalos de 100 segundos, aunque la precisión real del reloj puede ser menor. Para recuperar la hora actual del reloj, llame al método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) . La línea de base del reloj (el tiempo desde el que empieza el recuento) depende de la implementación, por lo que el valor devuelto por **getTime** no es inherentemente significativo. Lo que importa es la diferencia entre el momento en que el gráfico empezó a ejecutarse.

Aunque la precisión de un reloj de referencia puede variar, se garantiza que las horas devueltas por el método [**getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumenten de forma continuada. En otras palabras, las horas de reloj nunca se retroceden. Si un reloj de referencia está generando horas de reloj desde un origen de hardware y el reloj de hardware salta hacia atrás (por ejemplo, si hay un ajuste en el reloj), el método **getTime** debe continuar devolviendo la última hora detectada hasta que el reloj de hardware se ponga al día. Para obtener más información, consulte [**clase CBaseReferenceClock**](cbasereferenceclock.md).

**Reloj de referencia predeterminado**

Filter Graph Manager selecciona automáticamente un reloj de referencia cuando se ejecuta el gráfico. Usa el siguiente algoritmo para seleccionar el reloj:

-   Si la aplicación ha seleccionado un reloj (vea más abajo), use ese reloj.
-   Si el gráfico contiene un filtro de origen activo que admite [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), use ese filtro. Para ver la definición de un origen en directo, vea [orígenes en directo](live-sources.md).
-   Si el gráfico no contiene ningún filtro de código fuente activo, use cualquier filtro del gráfico que admita [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), empezando por los representadores y el flujo de trabajo ascendente. Prefiere filtros conectados a través de filtros no conectados. (Si el gráfico representa una secuencia de audio, este paso del algoritmo normalmente seleccionará el filtro de representador de audio).
-   Si ningún filtro proporciona un reloj adecuado, use el [reloj de referencia del sistema](system-reference-clock.md), que se basa en la hora del sistema.

**Establecer el reloj de referencia**

Una aplicación puede seleccionar un reloj llamando al método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en el administrador de gráficos de filtro. Solo debe hacerlo si tiene una razón determinada para preferir otro reloj.

Puede indicar al administrador de gráficos de filtro que no use un reloj de referencia mediante una llamada a [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) con el valor **null**. Por ejemplo, podría hacer esto para procesar los ejemplos lo más rápido posible. Para restaurar el reloj de referencia predeterminado, llame al método [**IFilterGraph:: SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) en el administrador de gráficos de filtro.

Cada vez que cambia el reloj de referencia, el administrador de gráficos de filtro notifica a cada filtro mediante una llamada a su método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) . Las aplicaciones nunca deben llamar a este método en los filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el reloj del gráfico](setting-the-graph-clock.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



