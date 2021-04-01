---
description: Hay muchas aplicaciones que crean subprocesos que invierten mucho tiempo en el estado de inactividad en espera de que se produzca un evento.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Agrupación de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf3565401dc57b077e333043861d42b683e810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909666"
---
# <a name="thread-pooling"></a>Agrupación de subprocesos

Hay muchas aplicaciones que crean subprocesos que invierten mucho tiempo en el estado de inactividad en espera de que se produzca un evento. Otros subprocesos pueden entrar en un estado de inactividad que solo se activa periódicamente para sondear un cambio o actualizar la información de estado. La *agrupación de subprocesos* permite usar subprocesos de forma más eficaz al proporcionar a la aplicación un grupo de subprocesos de trabajo administrados por el sistema. Al menos un subproceso supervisa el estado de todas las operaciones de espera en cola en el grupo de subprocesos. Cuando se ha completado una operación de espera, un subproceso de trabajo del grupo de subprocesos ejecuta la función de devolución de llamada correspondiente.

En este tema se describe la API de grupo de subprocesos original. La API de grupo de subprocesos introducida en Windows Vista es más sencilla, más confiable, tiene un mejor rendimiento y proporciona más flexibilidad a los desarrolladores. Para obtener información sobre la API de grupo de subprocesos actual, consulte [grupos de subprocesos](thread-pools.md).

También puede poner en cola los elementos de trabajo que no están relacionados con una operación de espera en el grupo de subprocesos. Para solicitar que un subproceso del grupo de subprocesos controle un elemento de trabajo, llame a la función [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) . Esta función toma un parámetro de la función a la que llamará el subproceso seleccionado en el grupo de subprocesos. No hay ninguna manera de cancelar un elemento de trabajo una vez que se ha puesto en la cola.

[Temporizador:](../sync/timer-queues.md) los temporizadores de cola y [las operaciones de espera registradas](../sync/wait-functions.md) también usan el grupo de subprocesos. Sus funciones de devolución de llamada se ponen en cola en el grupo de subprocesos. También puede usar la función [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) para publicar operaciones de e/s asincrónicas. Al completarse la e/s, un subproceso del grupo de subprocesos ejecuta la devolución de llamada.

El grupo de subprocesos se crea la primera vez que se llama a [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) o [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback), o cuando un temporizador de cola de temporizador o una operación de espera registrada pone en cola una función de devolución de llamada. De forma predeterminada, el número de subprocesos que se pueden crear en el grupo de subprocesos es aproximadamente 500. Cada subproceso utiliza el tamaño de pila predeterminado y se ejecuta con la prioridad predeterminada.

Hay dos tipos de subprocesos de trabajo en el grupo de subprocesos: e/s y no e/s. Un *subproceso de trabajo de e/s* es un subproceso que espera en un estado de espera de alerta. Los elementos de trabajo se ponen en cola para los subprocesos de trabajo de e/s como llamadas a procedimiento asincrónico (APC). Debe poner en cola un elemento de trabajo en un subproceso de trabajo de e/s si debe ejecutarse en un subproceso que espera en un estado de alerta.

Un *subproceso de trabajo que no es de e/s* espera en los puertos de finalización de e/s. El uso de subprocesos de trabajo que no son de e/s es más eficaz que el uso de subprocesos de trabajo de e/s. Por lo tanto, debe usar subprocesos de trabajo que no sean de e/s siempre que sea posible. Tanto las operaciones de e/s como los subprocesos de trabajo que no son de e/s no salen si hay solicitudes de e/s asincrónicas pendientes. Los elementos de trabajo que inician solicitudes de finalización de e/s asincrónicas pueden usar ambos tipos de subprocesos. Sin embargo, evite publicar solicitudes de finalización de e/s asincrónicas en subprocesos de trabajo que no son de e/s si pueden tardar mucho tiempo en completarse.

Para usar la agrupación de subprocesos, los elementos de trabajo y todas las funciones a las que llaman deben ser seguros para el grupo de subprocesos. Una función segura no supone que el subproceso que ejecuta es un subproceso dedicado o persistente. En general, debe evitar el uso de [almacenamiento local de subprocesos](thread-local-storage.md) o hacer una llamada asincrónica que requiera un subproceso persistente, como la función [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) . Sin embargo, se puede llamar a estas funciones en un subproceso dedicado (creado por la aplicación) o poner en cola en un subproceso de trabajo persistente (mediante [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) con la \_ opción WT EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[E/s de alertas](../fileio/alertable-i-o.md)
</dt> <dt>

[Llamadas a procedimientos asincrónicos](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Puertos de finalización de e/s](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Grupos de subprocesos](thread-pools.md)
</dt> </dl>

 

 
