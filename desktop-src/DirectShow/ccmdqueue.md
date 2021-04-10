---
description: La clase CCmdQueue es una clase base que proporciona una cola de objetos CDeferredCommand y funciones miembro para agregar, quitar, comprobar el estado e invocar los comandos en cola.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: Clase CCmdQueue
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
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152084"
---
# <a name="ccmdqueue-class"></a>Clase CCmdQueue

La `CCmdQueue` clase es una clase base que proporciona una cola de objetos [**CDeferredCommand**](cdeferredcommand.md) y funciones miembro para agregar, quitar, comprobar el estado e invocar los comandos en cola. Un `CCmdQueue` objeto es una parte de un objeto que implementa los métodos [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . El administrador de gráficos de filtro implementa los métodos de **IQueueCommand** para que las aplicaciones puedan poner en cola los comandos en el gráfico de filtro. Los filtros que implementan la interfaz **IQueueCommand** usan directamente esta clase. Si desea usar objetos **CDeferredCommand** , la cola se debe derivar de esta clase.

Hay dos modos de sincronización: grueso y preciso. En el modo grueso, la aplicación espera hasta que llega una hora especificada y, a continuación, ejecuta el comando. En el modo preciso, la aplicación espera hasta que el procesamiento comienza en el ejemplo que aparece en el momento y, a continuación, ejecuta el comando. El filtro determina cuál de ellos implementará. El administrador de gráficos de filtros siempre implementa el modo grueso para los comandos que se ponen en cola en el administrador de gráficos de filtro.

Si desea realizar una sincronización aproximada, es probable que desee esperar hasta que haya un comando pendiente y, a continuación, ejecutarlo. Para ello, puede llamar a [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md). Si tiene varias cosas que esperar, obtenga el identificador de evento de [**CCmdQueue:: GetDueHandle**](ccmdqueue-getduehandle.md) y, a continuación, llame a **CCmdQueue:: GetDueCommand** cuando se señale. el [**tiempo de flujo**](stream-time.md) solo realizará el avance entre las llamadas a las funciones miembro [**CCmdQueue:: Run**](ccmdqueue-run.md) y [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) . No hay ninguna garantía de que, si se establece el identificador, habrá un comando listo. Cada vez que se señala el evento, llame a la función miembro **GetDueCommand** (probablemente con un tiempo de espera de cero); Esto puede devolver E \_ Abort si no hay ningún comando listo.

Si desea una sincronización precisa, llame a la función miembro [**CCmdQueue:: GetCommandDueFor**](ccmdqueue-getcommandduefor.md) y pase los ejemplos que va a procesar como parámetro. Esto devuelve lo siguiente:

-   Un comando de tiempo de secuencia debido a o antes de esa hora de flujo.
-   Un comando de tiempo de presentación debido a o antes de la presentación de la hora de la secuencia. Haga esto solo entre las funciones miembro [**CCmdQueue:: Run**](ccmdqueue-run.md) y [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) , porque fuera de esto, no se conoce la asignación del tiempo de transmisión al tiempo de presentación.
-   Cualquier comando de tiempo de presentación debido ahora.

Si desea realizar una sincronización precisa de los ejemplos que se pueden procesar durante el modo de pausa, debe usar comandos de tiempo de secuencia.

En todos los casos, los comandos permanecen en la cola hasta que se llama o se cancela. Este objeto de cola administra completamente la configuración y el restablecimiento del identificador de evento.



| Miembros de datos protegidos                                 | Descripción                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bRunning                                            | Marca de estado de ejecución; establezca **true** cuando se ejecute.                                                     |
| m \_ dwAdvise                                            | Identificador de notificación del reloj de referencia (cero si no hay ninguna notificación pendiente).                            |
| m \_ evDue                                               | Establece la hora a la que se deben tener los comandos.                                                               |
| m \_ listPresentation                                    | Almacena comandos en cola en el momento de la presentación.                                                           |
| m \_ listStream                                          | Almacena comandos en cola en tiempo de secuencia.                                                                 |
| \_bloqueo m                                                | Protege el acceso a las listas.                                                                              |
| m \_ pClock                                              | Reloj de referencia actual.                                                                               |
| m \_ StreamTimeOffset                                    | Contiene el desplazamiento de tiempo de transmisión cuando **m \_ BRunning** es **true**.                                      |
| m \_ StreamTimeOffset                                    | Contiene el desplazamiento de tiempo de transmisión cuando **m \_ BRunning** es **true**.                                      |
| Funciones de miembro                                       | Descripción                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Construye un objeto **CCmdQueue** .                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Determina si se debe a una hora determinada.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Recupera el identificador de evento que se señalará.                                                      |
| Funciones miembro reemplazables                           | Descripción                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Cambia a modo detenido o en pausa.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Recupera un comando aplazado que se programa en un momento especificado.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Recupera un puntero al siguiente comando que se debe a.                                                   |
| [**Introducir**](ccmdqueue-insert.md)                     | Agrega el objeto [**CDeferredCommand**](cdeferredcommand.md) a la cola.                             |
| [**Nuevo**](ccmdqueue-new.md)                           | Inicializa un comando que se va a ejecutar y devuelve un nuevo objeto [**CDeferredCommand**](cdeferredcommand.md) . |
| [**Retirar**](ccmdqueue-remove.md)                     | Quita el objeto [**CDeferredCommand**](cdeferredcommand.md) de la cola.                        |
| [**Ejecutar**](ccmdqueue-run.md)                           | Cambia al modo de ejecución.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Establece el reloj usado para el control de tiempo.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Configura un evento de temporizador con el reloj de referencia.                                                        |



 

 

 



