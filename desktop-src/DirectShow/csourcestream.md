---
description: La clase CSourceStream proporciona un PIN de salida para la clase de filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Clase CSourceStream (Source. h)
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
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680598"
---
# <a name="csourcestream-class"></a>Clase CSourceStream

![jerarquía de clases csourcestream](images/source02.png)

La clase **CSourceStream** proporciona un PIN de salida para la clase de filtro [**CSource**](csource.md) .

Para obtener información sobre el uso de esta clase, vea [**CSource**](csource.md). Esta clase hereda la clase [**CAMThread**](camthread.md) , que proporciona un subproceso de trabajo para el streaming de datos del PIN. La clase **CSourceStream** implementa los siguientes métodos auxiliares para enviar solicitudes al subproceso:

-   [**CSourceStream:: Exit**](csourcestream-exit.md)
-   [**CSourceStream:: init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream:: Run**](csourcestream-run.md)
-   [**CSourceStream:: Stop**](csourcestream-stop.md)

La primera solicitud al subproceso debe ser [**init**](csourcestream-init.md). La solicitud de [**salida**](csourcestream-exit.md) finaliza el subproceso. En la práctica, no es necesario llamar a cualquiera de estos métodos directamente, ya que los métodos [**CSourceStream:: Active**](csourcestream-active.md) y [**CSourceStream:: Inactive**](csourcestream-inactive.md) del PIN los llaman según sea necesario.

La clase también proporciona varios métodos de "controlador":

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

No hacen nada en la clase base, pero la clase derivada puede invalidarlos.



| Variables de miembro protegidas                                             | Descripción                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Puntero al filtro que contiene este pin.                                                                                     |
| Métodos protegidos                                                      | Descripción                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Se llama cuando se inicializa el subproceso de streaming. Virtualiza.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Se llama cuando el subproceso de streaming está a punto de salir. Virtualiza.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Se llama al principio del método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Virtualiza. |
| [**Active**](csourcestream-active.md)                                 | Notifica al pin que el filtro está activo ahora.                                                                                   |
| [**Inactivo**](csourcestream-inactive.md)                             | Notifica al pin que el filtro ya no está activo.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Espera a la siguiente solicitud de subproceso.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Comprueba si hay una solicitud de subproceso, sin bloqueos.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Procedimiento de subproceso. Virtualiza.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Genera datos multimedia y los entrega al pin de entrada de nivel inferior. Virtualiza.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Determina si el PIN acepta un tipo de medio específico. Virtualiza.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Recupera un tipo de medio preferido. Virtualiza.                                                                                        |
| Métodos públicos                                                         | Descripción                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Método de constructor.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Método de destructor. Virtualiza.                                                                                                       |
| [**Smss**](csourcestream-init.md)                                     | Inicializa el subproceso de streaming.                                                                                                 |
| [**Salir**](csourcestream-exit.md)                                     | Indica al subproceso de streaming que salga.                                                                                             |
| [**Ejecutar**](csourcestream-run.md)                                       | Indica al subproceso de streaming que se ejecute.                                                                                              |
| [**Pausar**](csourcestream-pause.md)                                   | Indica al subproceso de streaming que se active.                                                                                    |
| [**Stop**](csourcestream-stop.md)                                     | Indica al subproceso de streaming que se detenga.                                                                                             |
| Métodos virtuales puros                                                   | Descripción                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Rellena un ejemplo multimedia con datos.                                                                                                   |
| Métodos IPin                                                           | Descripción                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Recupera un identificador para el código PIN.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 




