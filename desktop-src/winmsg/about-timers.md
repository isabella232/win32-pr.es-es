---
description: En este tema se describe cómo crear, identificar, establecer y eliminar temporizadores.
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: Acerca de los temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3163dbfd5357de516e0202665cd76d017335593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003065"
---
# <a name="about-timers"></a>Acerca de los temporizadores

En este tema se describe cómo crear, identificar, establecer y eliminar temporizadores. Una aplicación utiliza un temporizador para programar un evento para una ventana después de que haya transcurrido un tiempo especificado. Cada vez que transcurre el intervalo especificado (o el valor de tiempo de espera) para un temporizador, el sistema notifica a la ventana asociada con el temporizador. Dado que la precisión de un temporizador depende de la tasa de reloj del sistema y de la frecuencia con la que la aplicación recupera mensajes de la cola de mensajes, el valor de tiempo de espera solo es aproximado.

En este tema se incluyen las secciones siguientes.

-   [Operaciones de temporizador](#timer-operations)
-   [Temporizador de alta resolución](#high-resolution-timer)
-   [Objetos de temporizador de espera](#waitable-timer-objects)
-   [Temas relacionados](#related-topics)

## <a name="timer-operations"></a>Operaciones de temporizador

Las aplicaciones crean temporizadores mediante la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Un nuevo temporizador inicia el tiempo del intervalo en cuanto se crea. Una aplicación puede cambiar el valor de tiempo de espera de un temporizador mediante **SetTimer** y puede destruir un temporizador mediante la función [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) . Para usar los recursos del sistema de forma eficaz, las aplicaciones deben destruir temporizadores que ya no sean necesarios.

Cada temporizador tiene un identificador único. Al crear un temporizador, una aplicación puede especificar un identificador o hacer que el sistema cree un valor único. El primer parámetro de un mensaje del [**\_ temporizador de WM**](wm-timer.md) contiene el identificador del temporizador que envió el mensaje.

Si especifica un identificador de ventana en la llamada a [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer), la aplicación asocia el temporizador a esa ventana. Cada vez que transcurre el valor de tiempo de espera del temporizador, el sistema envía un mensaje del [**\_ temporizador de WM**](wm-timer.md) a la ventana asociada con el temporizador. Si no se especifica ningún identificador de ventana en la llamada a **SetTimer**, la aplicación que creó el temporizador debe supervisar su cola de mensajes para los mensajes de **\_ temporizador de WM** y enviarlos a la ventana correspondiente. Si se especifica una función de devolución de llamada [**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc) , el procedimiento de ventana predeterminado llama a la función de devolución de llamada cuando procesa el **\_ temporizador de WM**. Por lo tanto, debe enviar mensajes en el subproceso de llamada, incluso si usa **TimerProc** en lugar de procesar el **\_ temporizador de WM**.

Si necesita recibir una notificación cuando transcurra un temporizador, use un temporizador que espere. Para obtener más información, vea [objetos de temporizador](/windows/desktop/Sync/waitable-timer-objects)que se van a esperar.

## <a name="high-resolution-timer"></a>Temporizador de High-Resolution

Un contador es un término general que se usa en la programación para hacer referencia a una variable de incremento. Algunos sistemas incluyen un contador de rendimiento de alta resolución que proporciona tiempos transcurridos de alta resolución.

Si existe un contador de rendimiento de alta resolución en el sistema, puede usar la función [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) para expresar la frecuencia, en recuentos por segundo. El valor del recuento depende del procesador. En algunos procesadores, por ejemplo, el recuento puede ser la velocidad del ciclo del reloj del procesador.

La función [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) recupera el valor actual del contador de rendimiento de alta resolución. Al llamar a esta función al principio y al final de una sección de código, una aplicación utiliza esencialmente el contador como un temporizador de alta resolución. Por ejemplo, supongamos que [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) indica que la frecuencia del contador de rendimiento de alta resolución es 50.000 recuentos por segundo. Si la aplicación llama a **QueryPerformanceCounter** inmediatamente antes y inmediatamente después de la sección de código a la que se va a establecer el tiempo, los valores del contador podrían ser 1500 y 3500, respectivamente. Estos valores indicarían que transcurrió .04 segundos (recuentos de 2000) mientras se ejecutaba el código.

## <a name="waitable-timer-objects"></a>Objetos de temporizador de espera

Un objeto de temporizador que se pueda esperar es un objeto de sincronización cuyo estado está establecido en señalado cuando llega el momento de vencimiento especificado. Hay dos tipos de temporizadores de espera que se pueden crear: restablecimiento manual y sincronización. Un temporizador de cualquier tipo también puede ser un temporizador periódico.

Un subproceso utiliza la función [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) o [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) para crear un objeto de temporizador. El subproceso de creación especifica si el temporizador es un temporizador de restablecimiento manual o un temporizador de sincronización. El subproceso de creación puede especificar un nombre para el objeto de temporizador. Los subprocesos de otros procesos pueden abrir un identificador de un temporizador existente especificando su nombre en una llamada a la función [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Cualquier subproceso con un identificador a un objeto de temporizador puede utilizar una de las funciones de espera para esperar a que el estado del temporizador se establezca en señalado.

Para obtener más información sobre el uso de objetos de temporizador que se esperan para la sincronización de subprocesos, vea [objetos de temporizador](/windows/desktop/Sync/waitable-timer-objects)que se esperan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar temporizadores](using-timers.md)
</dt> </dl>

 

 
