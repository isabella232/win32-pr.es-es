---
description: En este tema se describe cómo crear, identificar, establecer y eliminar temporizadores.
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: Acerca de los temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fdcaa8c7e4a46f6d64aea17c84f9b137879a915489527e1b53cb391c1817560
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028513"
---
# <a name="about-timers"></a>Acerca de los temporizadores

En este tema se describe cómo crear, identificar, establecer y eliminar temporizadores. Una aplicación usa un temporizador para programar un evento para una ventana después de que haya transcurrido un tiempo especificado. Cada vez que transcurre el intervalo especificado (o el valor de tiempo de espera) para un temporizador, el sistema notifica a la ventana asociada al temporizador. Dado que la precisión de un temporizador depende de la velocidad del reloj del sistema y de la frecuencia con la que la aplicación recupera mensajes de la cola de mensajes, el valor de tiempo de espera solo es aproximado.

En este tema se incluyen las secciones siguientes.

-   [Operaciones de temporizador](#timer-operations)
-   [Temporizador de alta resolución](#high-resolution-timer)
-   [Objetos de temporizador que se pueden esperar](#waitable-timer-objects)
-   [Temas relacionados](#related-topics)

## <a name="timer-operations"></a>Operaciones de temporizador

Las aplicaciones crean temporizadores mediante la [**función SetTimer.**](/windows/win32/api/winuser/nf-winuser-settimer) Un nuevo temporizador comienza a cronometr el intervalo en cuanto se crea. Una aplicación puede cambiar el valor de tiempo de espera de un temporizador mediante **SetTimer** y puede destruir un temporizador mediante la [**función KillTimer.**](/windows/win32/api/winuser/nf-winuser-killtimer) Para usar los recursos del sistema de forma eficaz, las aplicaciones deben destruir los temporizadores que ya no son necesarios.

Cada temporizador tiene un identificador único. Al crear un temporizador, una aplicación puede especificar un identificador o hacer que el sistema cree un valor único. El primer parámetro de un [**mensaje WM \_ TIMER**](wm-timer.md) contiene el identificador del temporizador que publicó el mensaje.

Si especifica un identificador de ventana en la llamada a [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer), la aplicación asocia el temporizador a esa ventana. Cada vez que transcurre el valor de tiempo de espera del temporizador, el sistema envía un mensaje [**DE \_ TEMPORIZADOR WM**](wm-timer.md) a la ventana asociada al temporizador. Si no se especifica ningún identificador de ventana en la llamada a **SetTimer**, la aplicación que creó el temporizador debe supervisar su cola de mensajes para mensajes **WM \_ TIMER** y enviarlos a la ventana adecuada. Si especifica una función de devolución de llamada [**TimerProc,**](/windows/win32/api/winuser/nc-winuser-timerproc) el procedimiento de ventana predeterminado llama a la función de devolución de llamada cuando procesa **WM \_ TIMER**. Por lo tanto, debe enviar mensajes en el subproceso que realiza la llamada, incluso cuando se usa **TimerProc** en lugar de procesar **WM \_ TIMER**.

Si necesita recibir una notificación cuando transcurra un temporizador, use un temporizador que se pueda esperar. Para obtener más información, vea [Waitable Timer Objects](/windows/desktop/Sync/waitable-timer-objects).

## <a name="high-resolution-timer"></a>High-Resolution temporizador

Un contador es un término general que se usa en la programación para hacer referencia a una variable de incremento. Algunos sistemas incluyen un contador de rendimiento de alta resolución que proporciona tiempos transcurridos de alta resolución.

Si existe un contador de rendimiento de alta resolución en el sistema, puede usar la función [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) para expresar la frecuencia, en recuentos por segundo. El valor del recuento depende del procesador. En algunos procesadores, por ejemplo, el recuento podría ser la velocidad de ciclo del reloj del procesador.

La [**función QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) recupera el valor actual del contador de rendimiento de alta resolución. Al llamar a esta función al principio y al final de una sección de código, una aplicación usa básicamente el contador como temporizador de alta resolución. Por ejemplo, suponga que [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) indica que la frecuencia del contador de rendimiento de alta resolución es de 50 000 recuentos por segundo. Si la aplicación llama a **QueryPerformanceCounter** inmediatamente antes e inmediatamente después de la sección de código a la que se va a realizar el tiempo, los valores de contador podrían ser 1500 recuentos y 3500 recuentos, respectivamente. Estos valores indican que han transcurrido 04 segundos (2000 recuentos) mientras se ejecutaba el código.

## <a name="waitable-timer-objects"></a>Objetos de temporizador que se pueden esperar

Un objeto de temporizador que se puede esperar es un objeto de sincronización cuyo estado se establece en señalado cuando llega el tiempo de vencimiento especificado. Hay dos tipos de temporizadores que se pueden crear: restablecimiento manual y sincronización. Un temporizador de cualquier tipo también puede ser un temporizador periódico.

Un subproceso usa la [**función CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) [**o CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) para crear un objeto de temporizador. El subproceso de creación especifica si el temporizador es un temporizador de restablecimiento manual o un temporizador de sincronización. El subproceso de creación puede especificar un nombre para el objeto de temporizador. Los subprocesos de otros procesos pueden abrir un identificador para un temporizador existente especificando su nombre en una llamada a la [**función OpenWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) Cualquier subproceso con un identificador para un objeto de temporizador puede usar una de las funciones de espera para esperar a que el estado del temporizador se establezca en signaled.

Para obtener más información sobre el uso de objetos de temporizador que se pueden esperar para la sincronización de subprocesos, vea [Waitable Timer Objects](/windows/desktop/Sync/waitable-timer-objects).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de temporizadores](using-timers.md)
</dt> </dl>

 

 
