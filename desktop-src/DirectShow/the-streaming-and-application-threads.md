---
description: Subprocesos de streaming y aplicación
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Subprocesos de streaming y aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90916c14395a21aa5c53481c96b03fb6bbb2a8d4162cf996ef18ac15ce5e856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583125"
---
# <a name="the-streaming-and-application-threads"></a>Subprocesos de streaming y aplicación

Cualquier DirectShow aplicación contiene al menos dos subprocesos importantes: el subproceso de aplicación y uno o varios subprocesos de streaming. Los ejemplos se entregan en los subprocesos de streaming y los cambios de estado se suceden en el subproceso de la aplicación. El subproceso de streaming principal se crea mediante un filtro de origen o analizador. Otros filtros pueden crear subprocesos de trabajo que entregan ejemplos, y también se consideran subprocesos de streaming.

Algunos métodos se llaman en el subproceso de aplicación, mientras que otros se llaman en un subproceso de streaming. Por ejemplo:

-   Subprocesos de streaming: [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Subproceso de aplicación: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Cualquiera: [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Tener un subproceso de streaming independiente permite que los datos fluyan a través del gráfico mientras el subproceso de la aplicación espera la entrada del usuario. Sin embargo, el peligro de varios subprocesos es que un filtro pueda crear recursos cuando se detiene (en el subproceso de aplicación), usarlos dentro de un método de streaming y destruirlos cuando se detenga (también en el subproceso de aplicación). Si no tiene cuidado, el subproceso de streaming podría intentar usar los recursos después de destruirlos. La solución es proteger los recursos mediante secciones críticas y sincronizar los métodos de streaming con los cambios de estado.

Un filtro necesita una sección crítica para proteger el estado del filtro. La [**clase CBaseFilter**](cbasefilter.md) tiene una variable miembro para esta sección crítica, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md). Esta sección crítica se denomina bloqueo de filtro. Además, cada pin de entrada necesita una sección crítica para proteger los recursos usados por el subproceso de streaming. Estas secciones críticas se denominan bloqueos de streaming. debe declararlos en la clase de pin derivada. Es más fácil usar la [**clase CCritSec,**](ccritsec.md) que encapsula un objeto **Windows CRITICAL \_ SECTION** y se puede bloquear mediante la [**clase CAutoLock.**](cautolock.md) La **clase CCritSec** también proporciona algunas funciones de depuración útiles. Para obtener más información, vea [Funciones críticas de depuración de secciones](critical-section-debugging-functions.md).

Cuando un filtro se detiene o se vacía, debe sincronizar el subproceso de aplicación con el subproceso de streaming. Para evitar el interbloqueo, primero debe desbloquear el subproceso de streaming, que podría bloquearse por varias razones:

-   Está esperando obtener un ejemplo dentro del método [**IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) porque todos los ejemplos del asignador están en uso.
-   Está esperando a que otro filtro vuelva de un método de streaming, como **Receive**.
-   Está esperando dentro de uno de sus propios métodos de streaming para que algún recurso esté disponible.
-   Es un filtro de representador que espera el tiempo de presentación del ejemplo siguiente.
-   Es un filtro de representador que espera dentro del **método Receive** mientras está en pausa.

Por lo tanto, cuando el filtro se detiene o se vacía, debe hacer lo siguiente:

-   Libere cualquier ejemplo que esté manteniendo por cualquier motivo. Al hacerlo, se desbloquea el **método GetBuffer.**
-   Vuelva de cualquier método de streaming lo antes posible. Si un método de streaming está esperando un recurso, debe dejar de esperar inmediatamente.
-   Empiece a rechazar ejemplos en **Recibir** para que el subproceso de streaming no acceda a más recursos. (La [**clase CBaseInputPin**](cbaseinputpin.md) controla esto automáticamente).
-   El **método Stop** debe desasignar todos los asignadores del filtro. (La **clase CBaseInputPin** controla esto automáticamente).

El vaciado y la detención se suceden en el subproceso de la aplicación. Un filtro se detiene en respuesta al [**método IMediaControl::Stop.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) Filter Graph Manager emite el comando stop en orden ascendente, empezando desde los representadores y trabajando hacia atrás hasta los filtros de origen. El comando stop se produce completamente dentro del método **CBaseFilter::Stop del** filtro. Cuando el método vuelve, el filtro debe estar en estado detenido.

Normalmente, el vaciado se produce debido a un comando seek. Un comando flush se inicia desde el filtro de origen o analizador y se desplaza de bajada. El vaciado se produce en dos fases: el método [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informa a un filtro para descartar todos los datos pendientes y entrantes; El [**método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) indica al filtro que acepte de nuevo los datos. El vaciado requiere dos fases porque la llamada **a BeginFlush** está en el subproceso de aplicación, durante el cual el subproceso de streaming sigue entregando datos. Por lo tanto, algunos ejemplos pueden llegar después de **la llamada a BeginFlush.** El filtro debe descartarlos. Se garantiza que los ejemplos que llegan después de la llamada a **EndFlush** son nuevos y se deben entregar.

Las secciones siguientes contienen ejemplos de código que muestran cómo implementar los métodos de filtro más importantes, como **Pausar,** Recibir, etc., de manera que se eviten interbloqueos y condiciones de carrera. Sin embargo, cada filtro tiene requisitos diferentes, por lo que deberá adaptar estos ejemplos a su filtro concreto.

> [!Note]  
> Las clases base [**CTransformFilter**](ctransformfilter.md) y [**CTransInPlaceFilter**](ctransinplacefilter.md) controlan muchos de los problemas descritos en este artículo. Si va a escribir un filtro de transformación y el filtro no espera eventos dentro de un método de streaming o mantiene muestras fuera de **Receive**, estas clases base deben ser suficientes.

 

 

 



