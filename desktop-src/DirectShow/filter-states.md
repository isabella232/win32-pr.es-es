---
description: Estados de filtro
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Estados de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 487b2f5e71cfebd8a9c7282679aa39b2264f0460dd72ad23e1b2b26926e0c979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015743"
---
# <a name="filter-states"></a>Estados de filtro

Los filtros tienen tres estados posibles: detenido, en pausa y en ejecución. El propósito del estado en pausa es proporcionar datos en el gráfico, de modo que un comando de ejecución responda inmediatamente. El Administrador de Graph controla todas las transiciones de estado. Cuando una aplicación llama a [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)o [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), filter Graph Manager llama al método [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) correspondiente en todos los filtros. Las transiciones entre detenido y en ejecución siempre pasan por el estado en pausa, por lo que si la aplicación llama a **Ejecutar** en un gráfico detenido, el Administrador de filtros Graph pausa el gráfico antes de ejecutarlo.

Para la mayoría de los filtros, los estados en ejecución y en pausa son idénticos. Considere el siguiente gráfico de filtros:

Representador > transformación > origen

Supongamos por ahora que el filtro de origen no es un origen de captura en directo. Cuando el filtro de origen se detiene, crea un subproceso que genera nuevos datos y los escribe en ejemplos multimedia lo antes posible. El subproceso "inserta" los ejemplos de bajada mediante una llamada [**a IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el pin de entrada del filtro de transformación. El filtro de transformación recibe los ejemplos en el subproceso del filtro de origen. Puede usar un subproceso de trabajo para entregar los ejemplos al representador, pero normalmente los entrega en el mismo subproceso. Mientras el representador está en pausa, espera a recibir un ejemplo. Una vez que recibe uno, bloquea y mantiene ese ejemplo indefinidamente. Si es un representador de vídeo, muestra el ejemplo como una imagen de póster y vuelve a dibujar la imagen según sea necesario.

En este punto, la secuencia está totalmente preparada para la representación. Si el gráfico permanece en pausa, las muestras se "acumularán" en el gráfico detrás de la primera muestra, hasta que todos los filtros se bloqueen en [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Sin embargo, no se pierde ningún dato. Una vez desbloqueado el subproceso de origen, simplemente se reanuda desde el punto en que se bloqueó.

El filtro de origen y el filtro de transformación omiten la transición de en pausa a en ejecución: simplemente siguen procesando los datos lo más rápido posible. Pero cuando se ejecuta el representador, comienza a representar ejemplos. En primer lugar, representa el ejemplo que tenía mientras estaba en pausa. A continuación, cada vez que recibe un nuevo ejemplo, calcula el tiempo de presentación de la muestra. (Para obtener más información, [vea Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)). El representador contiene cada muestra hasta el tiempo de presentación, momento en el que representa la muestra. Mientras espera el tiempo de presentación, se bloquea en el [**método Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o recibe nuevos ejemplos en un subproceso de trabajo con una cola. Los filtros ascendentes desde el representador no participan en la programación.

Los orígenes en directo, como los dispositivos de captura, son una excepción a esta arquitectura general. Con un origen en directo, no es adecuado proporcionar datos de antemano. La aplicación puede pausar el gráfico y, a continuación, esperar mucho tiempo antes de ejecutarlo. El gráfico no debe representar muestras "obsoletas". Por lo tanto, un origen en directo no genera muestras mientras está en pausa, solo mientras se ejecuta. Para señalar este hecho al Administrador de Graph, el método [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) del filtro de origen devuelve VFW \_ S \_ CANT \_ CUE. Este código de retorno indica que el filtro ha cambiado al estado en pausa, aunque el representador no haya recibido ningún dato.

Cuando se detiene un filtro, rechaza las muestras que se le han entregado. Los filtros de origen apagan sus subprocesos de streaming y otros filtros apagan los subprocesos de trabajo que puedan haber creado. Los pines desasignan sus asignadores.

### <a name="state-transitions"></a>Transiciones de estado

El Administrador de Graph realiza todas las transiciones de estado en orden ascendente, empezando desde el representador y trabajando hacia atrás hasta el filtro de origen. Esta ordenación es necesaria para evitar que se cierren las muestras y evitar que el grafo interbloquee. Las transiciones de estado más cruciales se encuentran entre pausadas y detenidas:

-   Detenido en pausa: a medida que se pausa cada filtro, está listo para recibir muestras del filtro siguiente. El filtro de origen es el último en pausar. Crea el subproceso de streaming y comienza a entregar ejemplos. Dado que todos los filtros de nivel inferior están en pausa, ningún filtro rechaza ninguna muestra. El Administrador de Graph no completa la transición hasta que todos los representador del gráfico han recibido un ejemplo (a excepción de los orígenes en directo, como se describió anteriormente).
-   Pausado en detenido: cuando se detiene un filtro, libera las muestras que contiene, lo que desbloquea los filtros ascendentes que esperan en [**GetBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) Si el filtro está esperando un recurso dentro del [**método Receive,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) deja de esperar y devuelve de **Receive**, que desbloquea el filtro de llamada. Por lo tanto, cuando filter Graph Manager detiene el siguiente filtro ascendente, ese filtro no se bloquea en **GetBuffer** o **Receive** y puede responder al comando stop. El filtro ascendente podría entregar algunos ejemplos adicionales antes de obtener el comando stop, pero el filtro de nivel inferior simplemente los rechaza, porque ya se ha detenido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



