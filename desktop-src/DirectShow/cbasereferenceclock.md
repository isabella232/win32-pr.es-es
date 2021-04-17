---
description: La clase CBaseReferenceClock implementa un reloj de referencia.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Clase CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671085"
---
# <a name="cbasereferenceclock-class"></a>Clase CBaseReferenceClock

![jerarquía de clases cbasereferenceclock](images/rclock01.png)

La `CBaseReferenceClock` clase implementa un reloj de referencia.



| Variables de miembro protegidas                                                         | Descripción                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pSchedule**](cbasereferenceclock-m-pschedule.md)                            | Objeto [**CAMSchedule**](camschedule.md) que controla las tareas de programación del reloj. |
| Métodos protegidos                                                                  | Descripción                                                                            |
| [**~ CBaseReferenceClock**](cbasereferenceclock--cbasereferenceclock.md)           | Método de destructor.                                                                     |
| Métodos públicos                                                                     | Descripción                                                                            |
| [**CBaseReferenceClock**](cbasereferenceclock-cbasereferenceclock.md)             | Método de constructor.                                                                    |
| [**GetPrivateTime**](cbasereferenceclock-getprivatetime.md)                       | Recupera la hora real del reloj.                                                |
| [**SetTimeDelta**](cbasereferenceclock-settimedelta.md)                           | Ajusta la hora interna del reloj.                                                       |
| [**GetSchedule**](cbasereferenceclock-getschedule.md)                             | Recupera un puntero al objeto de programación del reloj.                                  |
| [**TriggerThread**](cbasereferenceclock-triggerthread.md)                         | Reactiva el subproceso de trabajo que controla la programación.                                    |
| Métodos IReferenceClock                                                            | Descripción                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | Recupera el tiempo de referencia actual.                                                  |
| [**AdviseTime**](cbasereferenceclock-advisetime.md)                               | Crea una solicitud de notificación de una captura.                                                     |
| [**AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)                       | Crea una solicitud de notificación periódica.                                                     |
| [**No notificar**](cbasereferenceclock-unadvise.md)                                   | Quita una solicitud de notificación pendiente.                                                      |
| Métodos IReferenceClockTimerControl                                                | Descripción                                                                            |
| [**GetDefaultTimerResolution**](cbasereferenceclock-getdefaulttimerresolution.md) | Devuelve la resolución actual del temporizador del reloj de referencia.                         |
| [**SetDefaultTimerResolution**](cbasereferenceclock-setdefaulttimerresolution.md) | Establece la resolución del temporizador del reloj de referencia.                                    |
| Funciones del asistente                                                                   | Descripción                                                                            |
| [**ConvertToMilliseconds**](converttomilliseconds.md)                             | Convierte una hora de referencia en milisegundos.                                             |



 

## <a name="remarks"></a>Observaciones

Esta clase implementa un reloj de referencia que admite las interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) y [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) . Si un filtro puede proporcionar un reloj de referencia para el gráfico de filtros, por ejemplo, mediante el acceso a un dispositivo de hardware, puede usar esta clase para implementar el reloj.

El `CBaseReferenceClock` objeto mantiene dos valores de hora distintos:

-   Internamente, el método [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) devuelve la hora real que mantiene el reloj.
-   Externamente, el método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) devuelve el tiempo de referencia para el gráfico de filtro.

Es válido para que el reloj interno se ejecute hacia atrás en breves períodos. Por ejemplo, si el reloj se desplaza hacia delante, el filtro puede ajustarlo hacia atrás. (Vea [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md)). El método **getTime** usa los valores de hora que se indican en **GetPrivateTime**. Sin embargo, el tiempo de referencia aumenta de forma monotónica; en otras palabras, nunca se ejecuta hacia atrás. Por lo tanto, si el reloj interno se ejecuta hacia atrás, **getTime** continúa notificando el tiempo anterior hasta que el reloj interno se pone al día.

Por ejemplo, los dos métodos podrían devolver las secuencias siguientes:

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

En el tercer paso del reloj, el reloj interno salta hacia atrás hasta 103. El método **getTime** continúa notificando 106 hasta que el reloj interno se pone al día.

De forma predeterminada, **GetPrivateTime** devuelve la hora del sistema, a través de una llamada a la función **timeGetTime** . Un filtro que proporciona un reloj de referencia desde un dispositivo externo puede realizar una de las siguientes acciones:

-   Invalide **GetPrivateTime** para devolver la hora del dispositivo.
-   Supervise la discrepancia entre la hora del dispositivo y la hora del sistema, y llame a **SetTimeDelta** para hacer correcciones.

Esta clase utiliza un objeto [**CAMSchedule**](camschedule.md) para controlar la programación de solicitudes de notificaciones. Para obtener más información, consulte la documentación de la clase **CAMSchedule** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




