---
description: La clase CSourceStream proporciona un pin de salida para la clase de filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: CSourceStream (clase, Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f7563cabff97626ac45a150e9a763033d9ce9261e5ae528e83d174e35d4f0d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428794"
---
# <a name="csourcestream-class"></a>CSourceStream (clase)

![Jerarquía de clases csourcestream](images/source02.png)

La **clase CSourceStream** proporciona un pin de salida para la [**clase de filtro CSource.**](csource.md)

Para obtener información sobre el uso de esta clase, vea [**CSource**](csource.md). Esta clase hereda la clase [**CAMThread,**](camthread.md) que proporciona un subproceso de trabajo para el streaming de datos del pin. La **clase CSourceStream** implementa los siguientes métodos auxiliares para enviar solicitudes al subproceso:

-   [**CSourceStream::Exit**](csourcestream-exit.md)
-   [**CSourceStream::Init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream::Run**](csourcestream-run.md)
-   [**CSourceStream::Stop**](csourcestream-stop.md)

La primera solicitud al subproceso debe ser [**Init**](csourcestream-init.md). La [**solicitud Exit**](csourcestream-exit.md) finaliza el subproceso. En la práctica, no es necesario llamar directamente a ninguno de estos métodos, ya que los métodos [**CSourceStream::Active**](csourcestream-active.md) y [**CSourceStream::Inactive**](csourcestream-inactive.md) del pin los llaman según sea necesario.

La clase también proporciona varios métodos de "controlador":

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

No hacen nada en la clase base, pero la clase derivada puede invalidarlos.



| Variables miembro protegidas                                             | Descripción                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Puntero al filtro que contiene este pin.                                                                                     |
| Métodos protegidos                                                      | Descripción                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Se llama cuando se inicializa el subproceso de streaming. Virtual.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Se llama cuando el subproceso de streaming está a punto de salir. Virtual.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Se llama al principio del [**método CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Virtual. |
| [**Activo**](csourcestream-active.md)                                 | Notifica al pin que el filtro ahora está activo.                                                                                   |
| [**Inactivo**](csourcestream-inactive.md)                             | Notifica al pin que el filtro ya no está activo.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Espera la siguiente solicitud de subproceso.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Comprueba si hay una solicitud de subproceso, sin bloquear.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Procedimiento de subproceso. Virtual.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Genera datos multimedia y los entrega al pin de entrada de bajada. Virtual.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Determina si el pin acepta un tipo de medio específico. Virtual.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Recupera un tipo de medio preferido. Virtual.                                                                                        |
| Métodos públicos                                                         | Descripción                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Método constructor.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Método destructor. Virtual.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Inicializa el subproceso de streaming.                                                                                                 |
| [**Salir**](csourcestream-exit.md)                                     | Indica al subproceso de streaming que se debe salir.                                                                                             |
| [**Ejecutar**](csourcestream-run.md)                                       | Indica el subproceso de streaming que se ejecutará.                                                                                              |
| [**Pausar**](csourcestream-pause.md)                                   | Indica al subproceso de streaming que se active.                                                                                    |
| [**Stop**](csourcestream-stop.md)                                     | Indica al subproceso de streaming que se detenga.                                                                                             |
| Métodos virtuales puros                                                   | Descripción                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Rellena un ejemplo multimedia con datos.                                                                                                   |
| Métodos de IPin                                                           | Descripción                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Recupera un identificador para el pin.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 




