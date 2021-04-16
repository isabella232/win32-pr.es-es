---
description: La clase CAMSchedule implementa un programador para los relojes de referencia.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Clase CAMSchedule (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671292"
---
# <a name="camschedule-class"></a>Clase CAMSchedule

La `CAMSchedule` clase implementa un programador para los relojes de referencia.



| Métodos públicos                                             | Descripción                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Método de constructor.                                                                  |
| [**~ CAMSchedule**](camschedule--camschedule.md)           | Método de destructor. Virtualiza.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Recupera el número de solicitudes de notificación pendientes.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Recupera la hora de la solicitud de notificación siguiente.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Agrega una solicitud de notificación a la lista de solicitudes pendientes.                              |
| [**No notificar**](camschedule-unadvise.md)                   | Quita una solicitud de notificación.                                                           |
| [**Informar**](camschedule-advise.md)                       | Envía todas las solicitudes programadas durante un tiempo especificado o anterior.          |
| [**GetEvent**](camschedule-getevent.md)                   | Recupera un identificador de evento, que se usa para indicar un cambio en la hora de notificación siguiente. |



 

## <a name="remarks"></a>Observaciones

Este objeto auxiliar mantiene una lista de solicitudes de notificación para un reloj de referencia. La clase [**CBaseReferenceClock**](cbasereferenceclock.md) la usa para ayudar a programar solicitudes de notificación. Los relojes usan este objeto de la siguiente manera:

1.  El reloj crea un subproceso de trabajo para controlar la programación.
2.  El subproceso de trabajo llama al método [**CAMSchedule:: GetEvent**](camschedule-getevent.md) para recuperar un identificador de evento del programador. Espera en este evento, inicialmente con un tiempo de espera infinito.
3.  Para programar una nueva solicitud de notificación, el reloj llama al método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) . Una solicitud de notificación puede ser de una sola captura o periódica. Scheduler mantiene la lista de solicitudes en el orden en el tiempo.
4.  Si se agrega una solicitud al principio de la lista, el programador indica el evento. (La lista está vacía al principio, por lo que se garantiza que la primera solicitud señale el evento).
5.  Cuando se señala el evento, el subproceso de trabajo llama al método [**CAMSchedule:: Advise**](camschedule-advise.md) , especificando el tiempo de referencia actual. Si alguna solicitud pendiente ha expirado, el programador las envía.
6.  El método Advise devuelve la hora de la siguiente solicitud. El subproceso de trabajo usa este valor para calcular un nuevo valor de tiempo de espera.
7.  Los pasos 2 6 se repiten indefinidamente.
8.  Para terminar el subproceso de trabajo, el reloj establece una marca interna y señala el evento.

En el paso 2, se señala el evento o se agota el tiempo de espera. Si el evento se señala, significa que se ha agregado una nueva solicitud al principio de la lista. El subproceso de trabajo debe calcular un nuevo valor de tiempo de espera. Por otro lado, si se agota el tiempo de espera, significa que una solicitud de notificación ha vencido y se debe enviar. La llamada a Advise en el paso 5 controla ambos casos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule. h (incluir streams. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




