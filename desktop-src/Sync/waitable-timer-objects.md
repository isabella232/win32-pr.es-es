---
description: Un objeto de temporizador que se puede esperar es un objeto de sincronización cuyo estado se establece en señalado cuando llega el tiempo de vencimiento especificado.
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: Objetos de temporizador que se pueden esperar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160685"
---
# <a name="waitable-timer-objects"></a>Objetos de temporizador que se pueden esperar

Un *objeto de temporizador que se* puede esperar es un objeto de sincronización cuyo estado se establece en señalado cuando llega el tiempo de vencimiento especificado. Hay dos tipos de temporizadores que se pueden crear: restablecimiento manual y sincronización. Un temporizador de cualquier tipo también puede ser un temporizador periódico.



| Object                | Descripción                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| temporizador de restablecimiento manual    | Temporizador cuyo estado permanece señalado hasta que se llama a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para establecer un nuevo tiempo de vencimiento.                                                                          |
| temporizador de sincronización | Temporizador cuyo estado permanece señalado hasta que un subproceso completa una operación de espera en el objeto de temporizador.                                                                                                     |
| temporizador periódico        | Temporizador que se reactiva cada vez que expira el período especificado, hasta que se restablece o se cancela el temporizador. Un temporizador periódico es un temporizador de restablecimiento manual periódico o un temporizador de sincronización periódico. |



 

> [!Note]  
> Cuando se señala un temporizador, el procesador debe ejecutarse para procesar las instrucciones asociadas. Los temporizadores periódicos de alta frecuencia mantienen el procesador ocupado [](../power/system-power-states.md) continuamente, lo que impide que el sistema se mantenga en un estado de energía inferior durante cualquier cantidad significativa de tiempo. Esto puede tener un impacto negativo en la duración de la batería del equipo portátil y en escenarios que dependen de una administración eficaz de la energía, como centros de datos grandes. Para una mayor eficiencia energética, considere la posibilidad de usar notificaciones basadas en eventos en lugar de notificaciones basadas en tiempo en la aplicación. Si es necesario un temporizador, use un temporizador que se señale una vez en lugar de un temporizador periódico, o establezca el intervalo en un valor mayor que un segundo.

 

Un subproceso usa la [**función CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) [**o CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) para crear un objeto de temporizador. El subproceso de creación especifica si el temporizador es un temporizador de restablecimiento manual o un temporizador de sincronización. El subproceso de creación puede especificar un nombre para el objeto de temporizador. Los subprocesos de otros procesos pueden abrir un identificador para un temporizador existente especificando su nombre en una llamada a la [**función OpenWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) Cualquier subproceso con un identificador para un [](wait-functions.md) objeto de temporizador puede usar una de las funciones de espera para esperar a que el estado del temporizador se establezca en signaled.

-   El subproceso llama a [**la función SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para activar el temporizador. Tenga en cuenta el uso de los parámetros siguientes **para SetWaitableTimer**:
-   Use el *parámetro lpDueTime* para especificar la hora a la que se establecerá el temporizador en el estado señalado. Cuando un temporizador de restablecimiento manual se establece en el estado señalado, permanece en este estado hasta que [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) establece un nuevo tiempo de vencimiento. Cuando un temporizador de sincronización se establece en el estado señalado, permanece en este estado hasta que un subproceso completa una operación de espera en el objeto de temporizador.
-   Use el *parámetro lPeriod* de la [**función SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para especificar el período de temporizador. Si el período no es cero, el temporizador es un temporizador periódico; se vuelve a activar cada vez que expira el período, hasta que se restablece o se cancela el temporizador. Si el período es cero, el temporizador no es un temporizador periódico; se señala una vez y, a continuación, se desactiva.

Un subproceso puede usar la [**función CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) para establecer el temporizador en el estado inactivo. Para restablecer el temporizador, llame a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Cuando haya terminado con el objeto de temporizador, llame a [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) para cerrar el identificador del objeto de temporizador.

El comportamiento de un temporizador que se puede esperar se puede resumir de la siguiente manera:

-   Cuando se establece un temporizador, se cancela si ya estaba activo, el estado del temporizador no está establecido y el temporizador se coloca en la cola del temporizador del kernel.
-   Cuando expira un temporizador, el temporizador se establece en el estado señalado. Si el temporizador tiene una rutina de finalización, se pone en cola en el subproceso que establece el temporizador. La rutina de finalización permanece en la cola [de](asynchronous-procedure-calls.md) llamada a procedimiento asincrónico (APC) del subproceso hasta que el subproceso entra en un estado de espera que se puede alertar. En ese momento, se envía el APC y se llama a la rutina de finalización. Si el temporizador es periódico, se vuelve a colocar en la cola del temporizador del kernel.
-   Cuando se cancela un temporizador, se quita de la cola del temporizador del kernel si estaba pendiente. Si el temporizador ha expirado y todavía hay un APC en cola en el subproceso que establece el temporizador, el APC se quita de la cola de APC del subproceso. El estado señalado del temporizador no se ve afectado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamadas a procedimiento asincrónico](asynchronous-procedure-calls.md)
</dt> <dt>

[Usar objetos de temporizador que se pueden esperar](using-waitable-timer-objects.md)
</dt> </dl>

 

 
