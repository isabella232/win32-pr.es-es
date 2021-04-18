---
description: Un objeto de temporizador que se pueda esperar es un objeto de sincronización cuyo estado está establecido en señalado cuando llega el momento de vencimiento especificado.
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: Objetos de temporizador de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668157"
---
# <a name="waitable-timer-objects"></a>Objetos de temporizador de espera

Un *objeto de temporizador* que se pueda esperar es un objeto de sincronización cuyo estado está establecido en señalado cuando llega el momento de vencimiento especificado. Hay dos tipos de temporizadores de espera que se pueden crear: restablecimiento manual y sincronización. Un temporizador de cualquier tipo también puede ser un temporizador periódico.



| Object                | Descripción                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| temporizador de restablecimiento manual    | Un temporizador cuyo estado permanece señalado hasta que se llama a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para establecer un nuevo tiempo de espera.                                                                          |
| temporizador de sincronización | Un temporizador cuyo estado permanece señalado hasta que un subproceso completa una operación de espera en el objeto de temporizador.                                                                                                     |
| temporizador periódico        | Un temporizador que se reactiva cada vez que expira el período especificado hasta que el temporizador se restablece o se cancela. Un temporizador periódico es un temporizador periódico de restablecimiento manual o un temporizador de sincronización periódico. |



 

> [!Note]  
> Cuando se señala un temporizador, el procesador debe ejecutar para procesar las instrucciones asociadas. Los temporizadores periódicos de alta frecuencia mantienen el procesador continuamente ocupado, lo que impide que el sistema permanezca en un [Estado de energía](../power/system-power-states.md) inferior durante un período de tiempo significativo. Esto puede tener un impacto negativo en la duración de la batería del equipo portátil y en escenarios que dependen de la administración eficaz de la energía, como centros de recursos de gran tamaño. Para lograr una mayor eficacia energética, considere la posibilidad de usar notificaciones basadas en eventos en lugar de notificaciones basadas en el tiempo en la aplicación. Si es necesario un temporizador, use un temporizador que se señale una vez en lugar de un temporizador periódico, o establezca el intervalo en un valor superior a un segundo.

 

Un subproceso utiliza la función [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) o [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) para crear un objeto de temporizador. El subproceso de creación especifica si el temporizador es un temporizador de restablecimiento manual o un temporizador de sincronización. El subproceso de creación puede especificar un nombre para el objeto de temporizador. Los subprocesos de otros procesos pueden abrir un identificador de un temporizador existente especificando su nombre en una llamada a la función [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Cualquier subproceso con un identificador a un objeto de temporizador puede utilizar una de las [funciones de espera](wait-functions.md) para esperar a que el estado del temporizador se establezca en señalado.

-   El subproceso llama a la función [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para activar el temporizador. Tenga en cuenta el uso de los siguientes parámetros para **SetWaitableTimer**:
-   Use el parámetro *lpDueTime* para especificar la hora a la que se establecerá el temporizador en el estado señalado. Cuando se establece un temporizador de restablecimiento manual en el estado señalado, permanece en este estado hasta que [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) establece una nueva hora de vencimiento. Cuando un temporizador de sincronización se establece en el estado señalado, permanece en este estado hasta que un subproceso completa una operación de espera en el objeto de temporizador.
-   Use el parámetro *lPeriod* de la función [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para especificar el período del temporizador. Si el período no es cero, el temporizador es un temporizador periódico; se reactiva cada vez que el período expira, hasta que el temporizador se restablece o se cancela. Si el punto es cero, el temporizador no es un temporizador periódico; se señaliza una vez y luego se desactiva.

Un subproceso puede usar la función [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) para establecer el temporizador en el estado inactivo. Para restablecer el temporizador, llame a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Cuando haya terminado con el objeto de temporizador, llame a [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) para cerrar el identificador del objeto de temporizador.

El comportamiento de un temporizador de espera se puede resumir de la manera siguiente:

-   Cuando se establece un temporizador, se cancela si ya estaba activo, el estado del temporizador no es señalado y el temporizador se coloca en la cola del temporizador del kernel.
-   Cuando un temporizador expira, el temporizador se establece en el estado señalado. Si el temporizador tiene una rutina de finalización, se pone en la cola del subproceso que establece el temporizador. La rutina de finalización permanece en la cola de [llamadas a procedimiento asincrónico](asynchronous-procedure-calls.md) (APC) del subproceso hasta que el subproceso entra en un estado de espera de alerta. En ese momento, se envía la APC y se llama a la rutina de finalización. Si el temporizador es periódico, se vuelve a colocar en la cola del temporizador del kernel.
-   Cuando se cancela un temporizador, se quita de la cola del temporizador del kernel si estaba pendiente. Si el temporizador expiró y todavía hay un APC en cola para el subproceso que estableció el temporizador, el APC se quita de la cola APC del subproceso. El estado señalado del temporizador no se ve afectado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamadas a procedimientos asincrónicos](asynchronous-procedure-calls.md)
</dt> <dt>

[Usar objetos de temporizador de espera](using-waitable-timer-objects.md)
</dt> </dl>

 

 
