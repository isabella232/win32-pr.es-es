---
description: La clase CBaseReferenceClock implementa un reloj de referencia.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: CBaseReferenceClock (clase, Refclock.h)
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
ms.openlocfilehash: ab737bb74b687854d0d45469a9e2784389c9e5a09dafedaab91c739415d448b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044115"
---
# <a name="cbasereferenceclock-class"></a>CBaseReferenceClock (clase)

![Jerarquía de clases cbasereferenceclock](images/rclock01.png)

La `CBaseReferenceClock` clase implementa un reloj de referencia.



| Variables miembro protegidas                                                         | Descripción                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pSchedule**](cbasereferenceclock-m-pschedule.md)                            | [**Objeto CAMSchedule**](camschedule.md) que controla las tareas de programación para el reloj. |
| Métodos protegidos                                                                  | Descripción                                                                            |
| [**~CBaseReferenceClock**](cbasereferenceclock--cbasereferenceclock.md)           | Método destructor.                                                                     |
| Métodos públicos                                                                     | Descripción                                                                            |
| [**CBaseReferenceClock**](cbasereferenceclock-cbasereferenceclock.md)             | Método constructor.                                                                    |
| [**GetPrivateTime**](cbasereferenceclock-getprivatetime.md)                       | Recupera la hora real del reloj.                                                |
| [**SetTimeDelta**](cbasereferenceclock-settimedelta.md)                           | Ajusta la hora del reloj interno.                                                       |
| [**GetSchedule**](cbasereferenceclock-getschedule.md)                             | Recupera un puntero al objeto de programación del reloj.                                  |
| [**TriggerThread**](cbasereferenceclock-triggerthread.md)                         | Reactiva el subproceso de trabajo que controla la programación.                                    |
| Métodos IReferenceClock                                                            | Descripción                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | Recupera la hora de referencia actual.                                                  |
| [**AdviseTime**](cbasereferenceclock-advisetime.md)                               | Crea una solicitud de asesoramiento de una sola toma.                                                     |
| [**AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)                       | Crea una solicitud de aviso periódica.                                                     |
| [**Unadvise**](cbasereferenceclock-unadvise.md)                                   | Quita una solicitud de aviso pendiente.                                                      |
| Métodos IReferenceClockTimerControl                                                | Descripción                                                                            |
| [**GetDefaultTimerResolution**](cbasereferenceclock-getdefaulttimerresolution.md) | Devuelve la resolución actual del temporizador del reloj de referencia.                         |
| [**SetDefaultTimerResolution**](cbasereferenceclock-setdefaulttimerresolution.md) | Establece la resolución del temporizador del reloj de referencia.                                    |
| Funciones del asistente                                                                   | Descripción                                                                            |
| [**ConvertToMilliseconds**](converttomilliseconds.md)                             | Convierte un tiempo de referencia en milisegundos.                                             |



 

## <a name="remarks"></a>Comentarios

Esta clase implementa un reloj de referencia que admite las interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) e [**IReferenceClockTimerControl.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) Si un filtro puede proporcionar un reloj de referencia para el gráfico de filtros, por ejemplo, al acceder a un dispositivo de hardware, puede usar esta clase para implementar el reloj.

El `CBaseReferenceClock` objeto mantiene dos valores de tiempo distintos:

-   Internamente, [**el método CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) devuelve la hora real que conserva el reloj.
-   Externamente, el [**método CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) devuelve la hora de referencia para el gráfico de filtros.

Es válido que el reloj interno se ejecute hacia atrás durante breves períodos. Por ejemplo, si el reloj se desvía hacia delante, el filtro puede ajustarlo hacia atrás. (Vea [**CBaseReferenceClock::SetTimeDelta).**](cbasereferenceclock-settimedelta.md) El **método GetTime** usa los valores de hora notificados **por GetPrivateTime.** Sin embargo, el tiempo de referencia aumenta de forma monónica. en otras palabras, nunca se ejecuta hacia atrás. Por lo tanto, si el reloj interno se ejecuta hacia atrás, **GetTime** continúa informando de la hora anterior hasta que el reloj interno se activa.

Por ejemplo, los dos métodos pueden devolver las secuencias siguientes:

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

En el tercer paso del reloj, el reloj interno salta hacia atrás hasta 103. El **método GetTime** continúa informando de 106 hasta que el reloj interno se alcanza.

De forma predeterminada, **GetPrivateTime devuelve** la hora del sistema, a través de una llamada a la **función timeGetTime.** Un filtro que proporciona un reloj de referencia desde un dispositivo externo puede realizar una de las siguientes acciones:

-   Invalide **GetPrivateTime** para devolver la hora del dispositivo.
-   Supervise la discrepancia entre la hora del dispositivo y la hora del sistema y llame a **SetTimeDelta** para realizar correcciones.

Esta clase usa un [**objeto CAMSchedule**](camschedule.md) para controlar la programación de solicitudes de asesoramiento. Para más información, consulte la documentación de la **clase CAMSchedule.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




