---
description: Estados de filtro
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Estados de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d61f66e1446d97d289f7e489f116f747f339d9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652323"
---
# <a name="filter-states"></a>Estados de filtro

Los filtros tienen tres Estados posibles: detenido, en pausa y en ejecución. El propósito del estado de pausa es indicar los datos en el gráfico, de modo que un comando de ejecución responda inmediatamente. El administrador de gráficos de filtro controla todas las transiciones de estado. Cuando una aplicación llama a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)o [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), el administrador de gráficos de filtro llama al método [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) correspondiente en todos los filtros. Las transiciones entre Stopped y Running siempre pasan por el estado de pausa, por lo que si la aplicación llama a **ejecutada** en un gráfico detenido, el administrador de gráficos de filtro pausa el gráfico antes de ejecutarlo.

Para la mayoría de los filtros, los Estados en ejecución y en pausa son idénticos. Considere el siguiente gráfico de filtros:

> representador de transformación de > de origen

Supongamos por ahora que el filtro de origen no es un origen de captura en directo. Cuando el filtro de origen se pausa, crea un subproceso que genera nuevos datos y los escribe en los ejemplos multimedia lo más rápido posible. El subproceso "envía" los ejemplos inferiores llamando a [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada del filtro de transformación. El filtro de transformación recibe los ejemplos en el subproceso del filtro de origen. Puede usar un subproceso de trabajo para entregar los ejemplos al representador, pero normalmente los entrega en el mismo subproceso. Mientras el representador está en pausa, espera a recibir un ejemplo. Una vez que recibe uno, lo bloquea y contiene ese ejemplo indefinidamente. Si se trata de un representador de vídeo, muestra el ejemplo como una imagen de póster y vuelve a dibujar la imagen según sea necesario.

En este momento, el flujo está totalmente preparado y listo para la representación. Si el gráfico permanece en pausa, los ejemplos se "amontonarán" en el gráfico detrás del primer ejemplo, hasta que todos los filtros se bloqueen en la [**recepción**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Sin embargo, no se pierden datos. Una vez desbloqueado el subproceso de origen, simplemente se reanuda desde el punto en el que se bloqueó.

El filtro de origen y el filtro de transformación omiten la transición de en pausa a en ejecución; simplemente continúan procesando los datos lo más rápido posible. Pero cuando se ejecuta el representador, se inician los ejemplos de representación. En primer lugar, representa el ejemplo que se mantiene mientras estaba en pausa. Después, cada vez que recibe un nuevo ejemplo, calcula el tiempo de presentación del ejemplo. (Para obtener más información, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md)). El representador contiene cada ejemplo hasta el momento de la presentación, momento en el que representa el ejemplo. Mientras espera el tiempo de presentación, se bloquea en el método [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o recibe nuevos ejemplos en un subproceso de trabajo con una cola. Los filtros ascendentes del representador no están implicados en la programación.

Los orígenes en directo, como los dispositivos de captura, son una excepción a esta arquitectura general. Con un origen en directo, no es adecuado señalar ningún dato de antemano. La aplicación podría pausar el gráfico y esperar mucho tiempo antes de ejecutarlo. El gráfico no debe presentar muestras "obsoletas". Por lo tanto, un origen en directo no genera ninguna muestra mientras se está en pausa, solo durante la ejecución. Para indicar este hecho al administrador de gráficos de filtro, el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) del filtro de origen devuelve la pila de no \_ \_ peralte de VFW \_ . Este código de retorno indica que el filtro ha cambiado al estado en pausa, aunque el representador no haya recibido ningún dato.

Cuando se detiene un filtro, se rechazan todos los ejemplos que se le hayan entregado. Los filtros de origen apagan los subprocesos de streaming y otros filtros apagan los subprocesos de trabajo que pueden haber creado. Los pin anulan la confirmación de los asignadores.

### <a name="state-transitions"></a>Transiciones de estado

Filter Graph Manager realiza todas las transiciones de estado en orden ascendente, comenzando por el representador y trabajando hacia atrás hasta el filtro de origen. Esta ordenación es necesaria para evitar que se quiten las muestras y evitar que el gráfico se interbloquee. Las transiciones de estado más cruciales están entre pausada y detenida:

-   Detenido para pausarse: a medida que cada filtro se pausa, está listo para recibir muestras del filtro siguiente. El filtro de origen es el último que se va a pausar. Crea el subproceso de streaming y comienza a entregar ejemplos. Dado que todos los filtros de nivel inferior están en pausa, ningún filtro rechaza ningún ejemplo. El administrador de gráficos de filtro no completa la transición hasta que todos los representadores del grafo hayan recibido un ejemplo (con la excepción de los orígenes en directo, como se describió anteriormente).
-   Pausado para detenerse: cuando se detiene un filtro, libera cualquier ejemplo que contiene, lo que desbloquea los filtros ascendentes que esperan en [**getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Si el filtro está esperando un recurso dentro del método [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , deja de esperar y vuelve de **Receive**, que desbloquea el filtro de llamada. Por lo tanto, cuando el administrador de gráficos de filtro detiene el siguiente filtro ascendente, ese filtro no se bloquea en **getBuffer** ni en **Receive**, y puede responder al comando STOP. El filtro de nivel superior podría ofrecer algunos ejemplos adicionales antes de obtener el comando de detención, pero el filtro de bajada simplemente los rechaza, porque ya se ha detenido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



