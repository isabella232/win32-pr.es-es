---
title: Procesos, subprocesos y apartamentos
description: Un proceso es una colección de espacio de memoria virtual, código, datos y recursos del sistema.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d598fc9d7dd39ab070b58aa7ba45a6e2fcae90db
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421447"
---
# <a name="processes-threads-and-apartments"></a>Procesos, subprocesos y apartamentos

Un *proceso* es una colección de espacio de memoria virtual, código, datos y recursos del sistema. Un *subproceso* es código que se ejecutará en serie dentro de un proceso. Un procesador ejecuta subprocesos, no procesos, por lo que cada aplicación tiene al menos un proceso y un proceso siempre tiene al menos un subproceso de ejecución, conocido como el subproceso principal. Un proceso puede tener varios subprocesos además del subproceso principal.

Los procesos se comunican entre sí a través de mensajes, mediante la tecnología de llamada a procedimiento remoto (RPC) de Microsoft para pasar información entre sí. No hay ninguna diferencia con el autor de la llamada entre una llamada procedente de un proceso en un equipo remoto y una llamada procedente de otro proceso en el mismo equipo.

Cuando un subproceso empieza a ejecutarse, continúa hasta que se elimina o hasta que lo interrumpe un subproceso con mayor prioridad (por una acción del usuario o el programador de subprocesos del kernel). Cada subproceso puede ejecutar secciones de código independientes, o varios subprocesos pueden ejecutar la misma sección de código. Los subprocesos que ejecutan el mismo bloque de código mantienen pilas independientes. Cada subproceso de un proceso comparte las variables y los recursos globales de ese proceso.

El programador de subprocesos determina cuándo y con qué frecuencia se ejecuta un subproceso, de acuerdo con una combinación del atributo de clase de prioridad del proceso y la prioridad base del subproceso. Establezca el atributo de clase de prioridad de un proceso llamando a la función [**SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) y establezca la prioridad base de un subproceso con una llamada a [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Las aplicaciones multiproceso deben evitar dos problemas de subprocesos: *interbloqueos* y *carreras*. Un interbloqueo se produce cuando cada subproceso está esperando a que el otro haga algo. El control de llamada COM ayuda a evitar los interbloqueos en las llamadas entre objetos. Una condición de carrera se produce cuando un subproceso finaliza antes que otro en el que depende, lo que hace que el primero use un valor no inicializado porque el último no ha proporcionado todavía uno válido. COM proporciona algunas funciones diseñadas específicamente para ayudar a evitar condiciones de carrera en servidores fuera de proceso. (Consulte [aplicaciones auxiliares de implementación de servidor fuera de proceso](out-of-process-server-implementation-helpers.md)).

## <a name="the-apartment-and-the-com-threading-architecture"></a>El apartamento y la arquitectura de subprocesos COM

Aunque COM admite el modelo de un solo subproceso por proceso antes de la introducción de varios subprocesos de ejecución, puede escribir código para aprovecharse de varios subprocesos, lo que da lugar a aplicaciones más eficaces, ya que permite que un subproceso se ejecute mientras otro subproceso espera a que se complete una operación que consume mucho tiempo.

> [!Note]  
> El uso de varios subprocesos no garantiza un mejor rendimiento. De hecho, dado que la factorización de subprocesos es un problema difícil, el uso de varios subprocesos suele causar problemas de rendimiento. La clave consiste en usar varios subprocesos solo si está seguro de lo que está haciendo.

 

En general, la manera más sencilla de ver la arquitectura de subprocesos COM es pensar en que todos los objetos COM del proceso se dividen en grupos denominados *apartamentos*. Un objeto COM reside exactamente en un apartamento, en el sentido de que solo un subproceso que pertenece a ese apartamento puede llamar legalmente a sus métodos. Cualquier otro subproceso que desee llamar al objeto debe pasar por un proxy.

Hay dos tipos de apartamentos: [apartamentos de un solo subproceso](single-threaded-apartments.md)y [apartamentos multiproceso](multithreaded-apartments.md).

-   Los apartamentos de un solo subproceso constan exactamente de un subproceso, por lo que todos los objetos COM que se encuentran en un apartamento de un solo subproceso pueden recibir llamadas a métodos solo desde el subproceso que pertenece a ese apartamento. Todas las llamadas a métodos a un objeto COM en un contenedor uniproceso se sincronizan con la cola de mensajes de Windows para el subproceso del contenedor uniproceso. Un proceso con un único subproceso de ejecución es simplemente un caso especial de este modelo.
-   Los apartamentos multiproceso se componen de uno o más subprocesos, por lo que todos los objetos COM que se encuentran en un apartamento multiproceso pueden recibir llamadas al método directamente desde cualquiera de los subprocesos que pertenecen al apartamento multiproceso. Los subprocesos de un apartamento multiproceso utilizan un modelo denominado *subprocesamiento libre*. Los propios objetos sincronizan las llamadas a objetos COM de un apartamento multiproceso.

> [!Note]  
> Para obtener una descripción de la comunicación entre apartamentos de un solo subproceso y apartamentos multiproceso en el mismo proceso, vea comunicación multiproceso [y](single-threaded-and-multithreaded-communication.md)multiproceso.

 

Un proceso puede tener cero o más apartamentos de un solo subproceso y cero o un apartamento multiproceso.

En un proceso, el apartamento principal es el primero que se va a inicializar. En un proceso de un solo subproceso, este es el único apartamento. Se calculan las referencias de los parámetros de llamada entre apartamentos y COM controla la sincronización a través de la mensajería. Si designa varios subprocesos en un proceso para que sean de subprocesamiento libre, todos los subprocesos libres residen en un único apartamento, los parámetros se pasan directamente a cualquier subproceso del apartamento y debe controlar toda la sincronización. En un proceso con subprocesamiento libre y subprocesamiento de apartamento, todos los subprocesos libres residen en un único apartamento y todos los demás apartamentos son apartamentos de un solo subproceso. Un proceso que realiza el trabajo COM es una colección de apartamentos con, como máximo, un apartamento multiproceso, pero cualquier número de apartamentos de un solo subproceso.

Los modelos de subprocesos de COM proporcionan el mecanismo para que los clientes y servidores que utilizan distintas arquitecturas de subprocesos funcionen juntos. Las llamadas entre objetos con diferentes modelos de subprocesos en distintos procesos se admiten de forma natural. Desde la perspectiva del objeto que realiza la llamada, todas las llamadas a objetos fuera de un proceso se comportan de manera idéntica, independientemente de cómo se procese el objeto que se está llamando. Del mismo modo, desde la perspectiva del objeto al que se llama, las llamadas de llegada se comportan de manera idéntica, independientemente del modelo de subprocesos del llamador.

La interacción entre un cliente y un objeto fuera de proceso es sencilla, incluso cuando utilizan diferentes modelos de subprocesos porque el cliente y el objeto se encuentran en procesos diferentes. COM, interposed entre el cliente y el servidor, puede proporcionar el código para que los modelos de subprocesos interoperen, mediante el cálculo de referencias estándar y RPC. Por ejemplo, si varios clientes de subprocesamiento libre llaman simultáneamente a un objeto de un solo subproceso, las llamadas se sincronizarán mediante COM colocando los mensajes de ventana correspondientes en la cola de mensajes del servidor. El apartamento del objeto recibirá una llamada cada vez que recupere y envíe mensajes. Sin embargo, se debe tener cuidado para asegurarse de que los servidores en proceso interactúen correctamente con sus clientes. (Vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)).

El problema más importante en la programación con un modelo multiproceso es hacer que el código sea seguro para subprocesos, de modo que los mensajes destinados a un subproceso determinado vayan solo a ese subproceso y se proteja el acceso a los subprocesos.

Para obtener más información, vea los temas siguientes:

-   [Elegir el modelo de subprocesos](choosing-the-threading-model.md)
-   [Apartamentos de un solo subproceso](single-threaded-apartments.md)
-   [Apartamentos multiproceso](multithreaded-apartments.md)
-   [Comunicación multiproceso y de un solo subproceso](single-threaded-and-multithreaded-communication.md)
-   [Problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)
-   [Acceso a interfaces entre apartamentos](accessing-interfaces-across-apartments.md)

 

 