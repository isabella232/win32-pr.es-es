---
title: Procesos, subprocesos y departamentos
description: Un proceso es una colección de espacio de memoria virtual, código, datos y recursos del sistema.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d598fc9d7dd39ab070b58aa7ba45a6e2fcae90db
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369451"
---
# <a name="processes-threads-and-apartments"></a>Procesos, subprocesos y departamentos

Un *proceso* es una colección de espacio de memoria virtual, código, datos y recursos del sistema. Un *subproceso* es código que se va a ejecutar en serie dentro de un proceso. Un procesador ejecuta subprocesos, no procesos, por lo que cada aplicación tiene al menos un proceso y un proceso siempre tiene al menos un subproceso de ejecución, conocido como subproceso principal. Un proceso puede tener varios subprocesos además del subproceso principal.

Los procesos se comunican entre sí a través de mensajes, mediante la tecnología de llamada a procedimiento remoto (RPC) de Microsoft para pasar información entre sí. No hay ninguna diferencia para el autor de la llamada entre una llamada procedente de un proceso en un equipo remoto y una llamada procedente de otro proceso en la misma máquina.

Cuando un subproceso comienza a ejecutarse, continúa hasta que se ha interrumpido o hasta que lo interrumpe un subproceso con mayor prioridad (por una acción del usuario o el programador de subprocesos del kernel). Cada subproceso puede ejecutar secciones de código independientes o varios subprocesos pueden ejecutar la misma sección de código. Los subprocesos que ejecutan el mismo bloque de código mantienen pilas independientes. Cada subproceso de un proceso comparte las variables globales y los recursos de ese proceso.

El programador de subprocesos determina cuándo y con qué frecuencia ejecutar un subproceso, según una combinación del atributo de clase de prioridad del proceso y la prioridad base del subproceso. Para establecer el atributo de clase de prioridad de un proceso, llame a la función [**SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) y establezca la prioridad base de un subproceso con una llamada a [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Las aplicaciones multiproceso deben evitar dos problemas de subprocesamiento: *interbloqueos* y *carreras.* Se produce un interbloqueo cuando cada subproceso está esperando a que el otro haga algo. El control de llamada COM ayuda a evitar interbloqueos en las llamadas entre objetos . Una condición de carrera se produce cuando un subproceso finaliza antes que otro del que depende, lo que hace que el primero use un valor no inicializado porque el segundo aún no ha proporcionado uno válido. COM proporciona algunas funciones diseñadas específicamente para ayudar a evitar condiciones de carrera en servidores fuera de proceso. (Vea [Asistentes de implementación de servidor fuera](out-of-process-server-implementation-helpers.md)de proceso).

## <a name="the-apartment-and-the-com-threading-architecture"></a>El apartamento y la arquitectura de subprocesos COM

Aunque COM admite el modelo de subproceso único por proceso frecuente antes de la introducción de varios subprocesos de ejecución, puede escribir código para aprovechar las ventajas de varios subprocesos, lo que da lugar a aplicaciones más eficaces, permitiendo que un subproceso se ejecute mientras otro subproceso espera a que se complete alguna operación que lleva mucho tiempo.

> [!Note]  
> El uso de varios subprocesos no es una garantía de un mejor rendimiento. De hecho, dado que la factoría de subprocesos es un problema difícil, el uso de varios subprocesos suele provocar problemas de rendimiento. La clave es usar varios subprocesos solo si está muy seguro de lo que está haciendo.

 

En general, la manera más sencilla de ver la arquitectura de subprocesos COM es pensar en todos los objetos COM del proceso como divididos en grupos *denominados departamentos*. Un objeto COM reside exactamente en un apartamento, en el sentido de que sus métodos solo pueden llamarse directamente legalmente por un subproceso que pertenezca a ese apartamento. Cualquier otro subproceso que quiera llamar al objeto debe pasar por un proxy.

Hay dos tipos de departamentos: [los de](single-threaded-apartments.md)un solo subproceso y los de [varios subprocesos.](multithreaded-apartments.md)

-   Los departamentos de un solo subproceso constan de exactamente un subproceso, por lo que todos los objetos COM que se encuentra en un apartamento de un solo subproceso pueden recibir llamadas de método solo desde el subproceso que pertenece a ese apartamento. Todas las llamadas de método a un objeto COM en un apartamento de un solo subproceso se sincronizan con la cola de mensajes de Windows para el subproceso del apartamento de un solo subproceso. Un proceso con un único subproceso de ejecución es simplemente un caso especial de este modelo.
-   Los departamentos multiproceso constan de uno o varios subprocesos, por lo que todos los objetos COM que se encuentra en un apartamento multiproceso pueden recibir llamadas de método directamente desde cualquiera de los subprocesos que pertenecen al apartamento multiproceso. Los subprocesos de un apartamento multiproceso usan un modelo denominado *free-threading*. Las llamadas a objetos COM en un apartamento multiproceso se sincronizan mediante los propios objetos.

> [!Note]  
> Para obtener una descripción de la comunicación entre los departamentos de un solo subproceso y los departamentos multiproceso dentro del mismo proceso, vea [Single-Threaded and Multithreaded Communication](single-threaded-and-multithreaded-communication.md).

 

Un proceso puede tener cero o más departamentos de un solo subproceso y cero o un apartamento multiproceso.

En un proceso, el apartamento principal es el primero que se inicializa. En un proceso de un solo subproceso, este es el único apartamento. Los parámetros de llamada se serializan entre los departamentos y COM controla la sincronización a través de la mensajería. Si designa varios subprocesos de un proceso para que sean de subproceso libre, todos los subprocesos libres residen en un único apartamento, los parámetros se pasan directamente a cualquier subproceso del apartamento y debe controlar toda la sincronización. En un proceso con subprocesamiento libre y subprocesamiento de apartamento, todos los subprocesos libres residen en un solo apartamento y todos los demás departamentos son departamentos de un solo subproceso. Un proceso que realiza el trabajo COM es una colección de departamentos con, como máximo, un apartamento multiproceso, pero cualquier número de departamentos de un solo subproceso.

Los modelos de subprocesos de COM proporcionan el mecanismo para que los clientes y servidores que usan diferentes arquitecturas de subprocesos funcionen juntos. Las llamadas entre objetos con diferentes modelos de subprocesamiento en procesos diferentes se admiten de forma natural. Desde la perspectiva del objeto que realiza la llamada, todas las llamadas a objetos fuera de un proceso se comportan de forma idéntica, independientemente de cómo se procese el objeto al que se llama. Del mismo modo, desde la perspectiva del objeto al que se llama, las llamadas entrantes se comportan de forma idéntica, independientemente del modelo de subprocesos del autor de la llamada.

La interacción entre un cliente y un objeto fuera de proceso es sencilla, incluso cuando usan modelos de subprocesos diferentes porque el cliente y el objeto están en procesos diferentes. COM, entre el cliente y el servidor, puede proporcionar el código para que los modelos de subprocesamiento interoperan, mediante la serialización estándar y RPC. Por ejemplo, si varios clientes de subproceso libre llaman simultáneamente a un objeto de un solo subproceso, COM sincronizará las llamadas colocando los mensajes de ventana correspondientes en la cola de mensajes del servidor. El apartamento del objeto recibirá una llamada cada vez que recupere y envíe mensajes. Sin embargo, se debe tener cierto cuidado para asegurarse de que los servidores en proceso interactúan correctamente con sus clientes. (Vea [In-Process Server Threading Issues](in-process-server-threading-issues.md)[Problemas de subprocesos del servidor en proceso]).

El problema más importante en la programación con un modelo multiproceso es hacer que el código sea seguro para subprocesos para que los mensajes destinados a un subproceso determinado vayan solo a ese subproceso y el acceso a los subprocesos esté protegido.

Para obtener más información, vea los temas siguientes:

-   [Elección del modelo de subprocesos](choosing-the-threading-model.md)
-   [Departamentos de un solo subproceso](single-threaded-apartments.md)
-   [Departamentos multiproceso](multithreaded-apartments.md)
-   [Comunicación multiproceso y de subproceso único](single-threaded-and-multithreaded-communication.md)
-   [Problemas de subprocesos del servidor en proceso](in-process-server-threading-issues.md)
-   [Acceso a interfaces entre departamentos](accessing-interfaces-across-apartments.md)

 

 