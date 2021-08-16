---
description: La clase CAMSchedule implementa un programador para los relojes de referencia.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Clase CAMSchedule (Dsschedule.h)
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
ms.openlocfilehash: d2236eb66086bb590892401cab052f39d81a41941db38d2a73dedd5edb4c53ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955414"
---
# <a name="camschedule-class"></a>CLASE CAMSchedule

La `CAMSchedule` clase implementa un programador para los relojes de referencia.



| Métodos públicos                                             | Descripción                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Método constructor.                                                                  |
| [**~CAMSchedule**](camschedule--camschedule.md)           | Método destructor. Virtual.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Recupera el número de solicitudes de asesoramiento pendientes.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Recupera la hora de la siguiente solicitud de aviso.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Agrega una solicitud de asesoramiento a la lista de solicitudes pendientes.                              |
| [**Unadvise**](camschedule-unadvise.md)                   | Quita una solicitud de asesoramiento.                                                           |
| [**consejo**](camschedule-advise.md)                       | Envía todas las solicitudes programadas para una hora especificada o anterior.          |
| [**GetEvent**](camschedule-getevent.md)                   | Recupera un identificador de evento, que se usa para indicar un cambio en la próxima hora de aviso. |



 

## <a name="remarks"></a>Comentarios

Este objeto auxiliar mantiene una lista de solicitudes de aviso para un reloj de referencia. La [**clase CBaseReferenceClock**](cbasereferenceclock.md) la usa para ayudar a programar solicitudes de asesoramiento. Los relojes usan este objeto de la siguiente manera:

1.  El reloj crea un subproceso de trabajo para controlar la programación.
2.  El subproceso de trabajo llama [**al método CAMSchedule::GetEvent**](camschedule-getevent.md) para recuperar un identificador de evento del programador. Espera en este evento, inicialmente con un tiempo de espera infinito.
3.  Para programar una nueva solicitud de aviso, el reloj llama al [**método CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md) Una solicitud de asesoramiento puede ser de una sola toma o periódica. El programador mantiene la lista de solicitudes en orden de tiempo.
4.  Si se agrega una solicitud al frente de la lista, el programador señala el evento. (La lista está vacía al principio, por lo que se garantiza que la primera solicitud señale el evento).
5.  Cuando se señala el evento, el subproceso de trabajo llama al [**método CAMSchedule::Advise,**](camschedule-advise.md) especificando la hora de referencia actual. Si alguna solicitud pendiente ha expirado, el programador las envía.
6.  El método Advise devuelve la hora de la siguiente solicitud. El subproceso de trabajo usa este valor para calcular un nuevo valor de tiempo de espera.
7.  Los pasos 2 y 6 se repiten indefinidamente.
8.  Para finalizar el subproceso de trabajo, el reloj establece una marca interna y señala el evento.

En el paso 2, se señala el evento o se ha pasado el tiempo de espera. Si se señala el evento, significa que se agregó una nueva solicitud al frente de la lista. El subproceso de trabajo debe calcular un nuevo valor de tiempo de espera. Por otro lado, si se ha pasado el tiempo de espera, significa que ha llegado una solicitud de aviso y se debe enviar. La llamada a Advise en el paso 5 controla ambos casos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




