---
description: La clase CCmdQueue es una clase base que proporciona una cola de objetos CDeferredCommand y funciones miembro para agregar, quitar, comprobar el estado e invocar los comandos en cola.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: CCmdQueue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue
api_type:
- COM
api_location: ''
ms.openlocfilehash: 78af7a975d54ba832bbdf1fb7f8027f87b747660
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072288"
---
# <a name="ccmdqueue-class"></a>CCmdQueue (clase)

La clase es una clase base que proporciona una cola de objetos CDeferredCommand y funciones miembro para agregar, quitar, comprobar el estado e invocar los comandos `CCmdQueue` en cola. [](cdeferredcommand.md) Un `CCmdQueue` objeto forma parte de un objeto que implementa métodos [**IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand) El administrador de gráficos de filtros implementa métodos **IQueueCommand** para que las aplicaciones puedan poner en cola comandos en el gráfico de filtros. Los filtros que implementan **la interfaz IQueueCommand** usan directamente esta clase. Si desea usar objetos **CDeferredCommand,** la cola debe derivarse de esta clase.

Hay dos modos de sincronización: general y preciso. En modo general, la aplicación espera hasta que llega una hora especificada y, a continuación, ejecuta el comando. En modo preciso, la aplicación espera hasta que comienza el procesamiento en el ejemplo que aparece en el momento y, a continuación, ejecuta el comando . El filtro determina cuál implementará. El administrador de gráficos de filtro siempre implementa el modo general para los comandos que se ponen en cola en el administrador de gráficos de filtro.

Si desea una sincronización general, es probable que quiera esperar hasta que haya un comando debido y, a continuación, ejecutarlo. Para ello, llame a [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md). Si tiene varias cosas que esperar, obtenga el identificador de evento de [**CCmdQueue::GetDueHandle**](ccmdqueue-getduehandle.md) y, a continuación, llame a **CCmdQueue::GetDueCommand** cuando se señale esto. [**El tiempo de**](stream-time.md) secuencia solo avanzará entre las llamadas a las funciones miembro [**CCmdQueue::Run**](ccmdqueue-run.md) y [**CCmdQueue::EndRun.**](ccmdqueue-endrun.md) No hay ninguna garantía de que si se establece el identificador, habrá un comando listo. Cada vez que se señale el evento, llame a la función miembro **GetDueCommand** (probablemente con un tiempo de espera de cero); esto puede devolver E \_ ABORT si no hay ningún comando listo.

Si desea una sincronización precisa, llame a la función miembro [**CCmdQueue::GetCommandDueFor**](ccmdqueue-getcommandduefor.md) y pase los ejemplos que va a procesar como parámetro. Esto devuelve lo siguiente:

-   Un comando en tiempo de secuencia que debe en o antes de esa hora de secuencia.
-   Un comando de tiempo de presentación debido a o antes de la presentación del tiempo de secuencia. Haga esto solo entre las funciones miembro [**CCmdQueue::Run**](ccmdqueue-run.md) y [**CCmdQueue::EndRun,**](ccmdqueue-endrun.md) ya que fuera de esto, no se conoce la asignación del tiempo de transmisión a la hora de presentación.
-   Cualquier comando en tiempo de presentación que se deba ahora.

Si desea una sincronización precisa de los ejemplos que se pueden procesar durante el modo en pausa, debe usar comandos en tiempo de transmisión.

En todos los casos, los comandos permanecen en cola hasta que se llama o se cancela. La configuración y el restablecimiento del identificador de eventos se administran completamente mediante este objeto de cola.



| Miembros de datos protegidos                                 | Descripción                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bRunning                                            | Marca para el estado de ejecución; establezca **TRUE cuando** se ejecute.                                                     |
| m \_ dwAdvise                                            | Aconsejar el identificador del reloj de referencia (cero si no hay ningún aviso pendiente).                            |
| m \_ evDue                                               | Establece la hora a la que deben pagarse los comandos.                                                               |
| m \_ listPresentation                                    | Almacena los comandos en cola en tiempo de presentación.                                                           |
| m \_ listStream                                          | Almacena los comandos en cola en tiempo de transmisión.                                                                 |
| m \_ Lock                                                | Protege el acceso a las listas.                                                                              |
| m \_ pClock                                              | Reloj de referencia actual.                                                                               |
| m \_ StreamTimeOffset                                    | Contiene el desplazamiento de tiempo de secuencia **cuando m \_ bRunning** es **TRUE.**                                      |
| m \_ StreamTimeOffset                                    | Contiene el desplazamiento de tiempo de secuencia **cuando m \_ bRunning** es **TRUE.**                                      |
| Funciones de miembro                                       | Descripción                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Construye un **objeto CCmdQueue.**                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Determina si se debe un tiempo determinado.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Recupera el identificador de evento que se señalizará.                                                      |
| Funciones miembro reemplazables                           | Descripción                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Cambia al modo detenido o en pausa.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Recupera un comando aplazado que se programa a la hora especificada.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Recupera un puntero al comando siguiente que está a la orden de vencimiento.                                                   |
| [**Insertar**](ccmdqueue-insert.md)                     | Agrega el [**objeto CDeferredCommand**](cdeferredcommand.md) a la cola.                             |
| [**Nuevo**](ccmdqueue-new.md)                           | Inicializa un comando que se va a ejecutar y devuelve un nuevo [**objeto CDeferredCommand.**](cdeferredcommand.md) |
| [**Remove**](ccmdqueue-remove.md)                     | Quita el objeto [**CDeferredCommand**](cdeferredcommand.md) de la cola.                        |
| [**Ejecutar**](ccmdqueue-run.md)                           | Cambia al modo en ejecución.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Establece el reloj utilizado para el control de tiempo.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Configura un evento de temporizador con el reloj de referencia.                                                        |



 

 

 



