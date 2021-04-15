---
description: Los subprocesos streaming y Application
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Los subprocesos streaming y Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432e613ff0322377c042e796d84ef7affdda99c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547019"
---
# <a name="the-streaming-and-application-threads"></a>Los subprocesos streaming y Application

Cualquier aplicación de DirectShow contiene al menos dos subprocesos importantes: el subproceso de la aplicación y uno o más subprocesos de streaming. Los ejemplos se entregan en los subprocesos de streaming y los cambios de estado se producen en el subproceso de la aplicación. Un filtro de origen o analizador crea el subproceso de streaming principal. Otros filtros pueden crear subprocesos de trabajo que proporcionan ejemplos, y también se consideran subprocesos de transmisión por secuencias.

Algunos métodos se llaman en el subproceso de la aplicación, mientras que otros se llaman en un subproceso de streaming. Por ejemplo:

-   Subprocesos de streaming: [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Subproceso de aplicación: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   O bien: [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Tener un subproceso de streaming independiente permite que los datos fluyan a través del gráfico mientras el subproceso de la aplicación espera la entrada del usuario. Sin embargo, el peligro de varios subprocesos es que un filtro puede crear recursos cuando se pausa (en el subproceso de aplicación), utilizarlos dentro de un método de transmisión por secuencias y destruirlos cuando se detiene (también en el subproceso de la aplicación). Si no tiene cuidado, el subproceso de streaming podría intentar usar los recursos una vez destruidos. La solución consiste en proteger los recursos mediante secciones críticas y sincronizar los métodos de streaming con los cambios de estado.

Un filtro necesita una sección crítica para proteger el estado del filtro. La clase [**CBaseFilter**](cbasefilter.md) tiene una variable miembro para esta sección crítica, [**CBaseFilter:: m \_ Plock**](cbasefilter-m-plock.md). Esta sección crítica se denomina bloqueo de filtro. Además, cada pin de entrada necesita una sección crítica para proteger los recursos utilizados por el subproceso de streaming. Estas secciones críticas se denominan bloqueos de streaming; debe declararlos en la clase de PIN derivada. Es más fácil usar la clase [**CCritSec**](ccritsec.md) , que ajusta un objeto de **\_ sección crítica** de Windows y se puede bloquear mediante la clase [**CAutoLock**](cautolock.md) . La clase **CCritSec** también proporciona algunas funciones de depuración útiles. Para obtener más información, vea [funciones críticas de depuración de sección](critical-section-debugging-functions.md).

Cuando un filtro se detiene o se vacía, debe sincronizar el subproceso de aplicación con el subproceso de streaming. Para evitar el interbloqueo, primero debe desbloquear el subproceso de streaming, que podría estar bloqueado por varias razones:

-   Está esperando obtener un ejemplo dentro del método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , porque todos los ejemplos del asignador están en uso.
-   Está esperando a que se devuelva otro filtro desde un método de transmisión por secuencias, como **Receive**.
-   Está esperando dentro de uno de sus propios métodos de streaming, para que algún recurso esté disponible.
-   Es un filtro de representador que espera el tiempo de presentación del ejemplo siguiente
-   Se trata de un filtro de representador que espera dentro del método **Receive** mientras está en pausa.

Por lo tanto, cuando el filtro se detiene o se vacía, debe hacer lo siguiente:

-   Libere cualquier ejemplo que esté reteniendo por cualquier motivo. Al hacerlo, se desbloquea el método **getBuffer** .
-   Vuelva de cualquier método de streaming lo más rápido posible. Si un método de transmisión por secuencias está esperando un recurso, debe dejar de esperar de inmediato.
-   Empieza a rechazar muestras en **recepción**, de modo que el subproceso de streaming no tiene acceso a más recursos. (La clase [**CBaseInputPin**](cbaseinputpin.md) lo controla automáticamente).
-   El método **Stop** debe desasignar todos los asignadores del filtro. (La clase **CBaseInputPin** lo controla automáticamente).

El vaciado y la detención se producen en el subproceso de la aplicación. Un filtro se detiene en respuesta al método [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) . Filter Graph Manager emite el comando STOP en orden ascendente, empezando por los representadores y trabajando hacia atrás hasta los filtros de origen. El comando STOP se produce completamente dentro del método **CBaseFilter:: Stop** del filtro. Cuando el método devuelve, el filtro debe estar en estado detenido.

Normalmente, el vaciado se produce debido a un comando Seek. Un comando de vaciado se inicia desde el filtro de origen o analizador y se desplaza hacia abajo. El vaciado se produce en dos fases: el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informa a un filtro para descartar todos los datos pendientes y entrantes; el método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) señala el filtro para aceptar los datos de nuevo. El vaciado requiere dos fases porque la llamada **BeginFlush** se encuentra en el subproceso de la aplicación, durante el cual el subproceso de streaming sigue entregando datos. Por lo tanto, algunos ejemplos pueden llegar después de la llamada a **BeginFlush** . El filtro debe descartarlos. Se garantiza que las muestras que llegan después de la llamada a **EndFlush** son nuevas y deben entregarse.

Las secciones siguientes contienen ejemplos de código que muestran cómo implementar los métodos de filtro más importantes, como **pausar**, **recibir**, etc., de modo que se eviten los interbloqueos y las condiciones de carrera. Sin embargo, cada filtro tiene requisitos diferentes, por lo que tendrá que adaptar estos ejemplos a su filtro concreto.

> [!Note]  
> Las clases base [**CTransformFilter**](ctransformfilter.md) y [**CTransInPlaceFilter**](ctransinplacefilter.md) controlan muchos de los problemas que se describen en este artículo. Si está escribiendo un filtro de transformación y el filtro no espera en los eventos dentro de un método de transmisión por secuencias, o si contiene muestras fuera de la **recepción**, estas clases base deben ser suficientes.

 

 

 



