---
description: Hay muchas aplicaciones que crean subprocesos que pasan una gran cantidad de tiempo en estado de espera a que se produzca un evento.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Agrupación de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf3565401dc57b077e333043861d42b683e810c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062783"
---
# <a name="thread-pooling"></a>Agrupación de subprocesos

Hay muchas aplicaciones que crean subprocesos que pasan una gran cantidad de tiempo en estado de espera a que se produzca un evento. Otros subprocesos pueden entrar en un estado de espera solo para que se reande periódicamente para sondear en busca de un cambio o actualizar la información de estado. *La agrupación de* subprocesos permite usar subprocesos de forma más eficaz proporcionando a la aplicación un grupo de subprocesos de trabajo administrados por el sistema. Al menos un subproceso supervisa el estado de todas las operaciones de espera en cola en el grupo de subprocesos. Cuando se ha completado una operación de espera, un subproceso de trabajo del grupo de subprocesos ejecuta la función de devolución de llamada correspondiente.

En este tema se describe la API del grupo de subprocesos original. La API del grupo de subprocesos introducida en Windows Vista es más sencilla, más confiable, tiene un mejor rendimiento y proporciona más flexibilidad a los desarrolladores. Para obtener información sobre la API del grupo de subprocesos actual, vea [Grupos de subprocesos.](thread-pools.md)

También puede poner en cola elementos de trabajo que no están relacionados con una operación de espera en el grupo de subprocesos. Para solicitar que un subproceso del grupo de subprocesos controle un elemento de trabajo, llame a la [**función QueueUserWorkItem.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) Esta función toma un parámetro para la función a la que llamará el subproceso seleccionado del grupo de subprocesos. No hay ninguna manera de cancelar un elemento de trabajo después de que se haya puesto en cola.

[Los temporizadores de la cola de temporizadores](../sync/timer-queues.md) [y las operaciones de espera registradas](../sync/wait-functions.md) también usan el grupo de subprocesos. Sus funciones de devolución de llamada se ponen en cola en el grupo de subprocesos. También puede usar la función [**BindIoCompletionCallback para**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) publicar operaciones de E/S asincrónicas. Al finalizar la E/S , un subproceso del grupo de subprocesos ejecuta la devolución de llamada.

El grupo de subprocesos se crea la primera vez que se llama a [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) o [**BindIoCompletionCallback,**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)o cuando un temporizador de cola de temporizador o una operación de espera registrada pone en cola una función de devolución de llamada. De forma predeterminada, el número de subprocesos que se pueden crear en el grupo de subprocesos es de aproximadamente 500. Cada subproceso usa el tamaño de pila predeterminado y se ejecuta con la prioridad predeterminada.

Hay dos tipos de subprocesos de trabajo en el grupo de subprocesos: E/S y no E/S. Un *subproceso de trabajo de E/S* es un subproceso que espera en un estado de espera que se puede alertar. Los elementos de trabajo se ponen en cola en subprocesos de trabajo de E/S como llamadas a procedimiento asincrónico (APC). Debe poner en cola un elemento de trabajo en un subproceso de trabajo de E/S si se debe ejecutar en un subproceso que espera en estado de alerta.

Un subproceso de trabajo que no es *de E/S* espera en los puertos de finalización de E/S. El uso de subprocesos de trabajo que no son de E/S es más eficaz que usar subprocesos de trabajo de E/S. Por lo tanto, debe usar subprocesos de trabajo que no son de E/S siempre que sea posible. Tanto los subprocesos de trabajo de E/S como los subprocesos de trabajo que no son de E/S no se cierran si hay solicitudes de E/S asincrónicas pendientes. Los elementos de trabajo que inician solicitudes asincrónicas de finalización de E/S pueden usar ambos tipos de subprocesos. Sin embargo, evite publicar solicitudes asincrónicas de finalización de E/S en subprocesos de trabajo que no son de E/S si podrían tardar mucho tiempo en completarse.

Para usar la agrupación de subprocesos, los elementos de trabajo y todas las funciones a las que llaman deben ser seguros para el grupo de subprocesos. Una función segura no supone que el subproceso que la ejecuta es un subproceso dedicado o persistente. En general, debe evitar el uso del almacenamiento [local](thread-local-storage.md) de subprocesos o realizar una llamada asincrónica que requiera un subproceso persistente, como la [**función RegNotifyChangeKeyValue.**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) Sin embargo, estas funciones se pueden llamar en un subproceso dedicado (creado por la aplicación) o poner en cola en un subproceso de trabajo persistente (mediante [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) con la opción \_ WT EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[E/S que se puede alertar](../fileio/alertable-i-o.md)
</dt> <dt>

[Llamadas a procedimiento asincrónico](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Puertos de finalización de E/S](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Grupos de subprocesos](thread-pools.md)
</dt> </dl>

 

 
