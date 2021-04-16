---
title: Apartamentos multiproceso
description: Apartamentos multiproceso
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2594f9341fc662b068fb7e007e538282a31273
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105685798"
---
# <a name="multithreaded-apartments"></a>Apartamentos multiproceso

En un modelo de Apartamento multiproceso, todos los subprocesos del proceso que se han inicializado como subproceso libre se encuentran en un único apartamento. Por lo tanto, no hay necesidad de calcular las referencias entre subprocesos. Los subprocesos no necesitan recuperar y enviar mensajes porque COM no utiliza los mensajes de ventana de este modelo.

Las llamadas a métodos de objetos en el contenedor multiproceso se pueden ejecutar en cualquier subproceso del apartamento. No hay ninguna serialización de llamadas; pueden producirse muchas llamadas al mismo método o al mismo objeto simultáneamente. Los objetos creados en el contenedor multiproceso deben ser capaces de controlar llamadas en sus métodos desde otros subprocesos en cualquier momento.

Dado que las llamadas a objetos no se serializan de ninguna manera, la simultaneidad de objetos multiproceso ofrece el mayor rendimiento y toma la mejor ventaja del hardware multiprocesador para la llamada entre subprocesos, entre procesos y entre equipos. Sin embargo, esto significa que el código de los objetos debe proporcionar sincronización en sus implementaciones de interfaz, normalmente mediante el uso de primitivas de sincronización, como objetos de evento, secciones críticas, exclusiones mutuas o semáforos, que se describen más adelante en esta sección. Además, dado que el objeto no controla la duración de los subprocesos que acceden a él, no se puede almacenar ningún estado específico del subproceso en el objeto (en almacenamiento local para el subproceso).

A continuación se presentan algunas consideraciones importantes con respecto a la sincronización de apartamentos multiproceso:

-   COM permite la sincronización de llamadas para apartamentos de un solo subproceso.
-   Los apartamentos multiproceso no reciben llamadas mientras realizan llamadas (en el mismo subproceso).
-   Los apartamentos multiproceso no pueden realizar llamadas sincronizadas por entrada.
-   Las llamadas asincrónicas se convierten en llamadas sincrónicas en apartamentos multiproceso.
-   No se llama al filtro de mensajes para ningún subproceso de un apartamento multiproceso.

Para inicializar un subproceso como de subproceso libre, llame a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)y especifique el multiproceso de coinit \_ . Para obtener información sobre los subprocesos de servidor en proceso, vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md).

Varios clientes pueden llamar simultáneamente a, desde distintos subprocesos, un objeto que admite el subprocesamiento libre. En los servidores fuera de proceso de subprocesos libres, COM, a través del subsistema RPC, crea un grupo de subprocesos en el proceso de servidor y una llamada de cliente (o varias llamadas de cliente) se puede entregar por cualquiera de estos subprocesos en cualquier momento. Un servidor fuera de proceso también debe implementar la sincronización en su generador de clases. Los objetos en proceso de subprocesamiento libre pueden recibir llamadas directas desde varios subprocesos del cliente.

El cliente puede realizar trabajos COM en varios subprocesos. Todos los subprocesos pertenecen al mismo apartamento multiproceso. Los punteros de interfaz se pasan directamente desde el subproceso al subproceso en un apartamento multiproceso, por lo que no se calculan las referencias de los punteros de interfaz entre sus subprocesos. Los filtros de mensajes (implementaciones de [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)) no se usan en apartamentos multiproceso. El subproceso de cliente se suspenderá cuando realice una llamada COM a objetos fuera de apartamento y se reanudará cuando se devuelva la llamada. Las llamadas entre procesos todavía se controlan mediante RPC.

Los subprocesos inicializados con el modelo de subprocesamiento libre deben implementar su propia sincronización. Como se mencionó anteriormente en esta sección, Windows habilita esta implementación a través de los primitivos de sincronización siguientes:

-   Los objetos de evento proporcionan una manera de señalizar uno o más subprocesos que se ha producido un evento. Cualquier subproceso de un proceso puede crear un objeto de evento. La función de creación de eventos, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), devuelve un identificador para el evento. Una vez creado un objeto de evento, los subprocesos con un identificador al objeto pueden esperar en él antes de continuar con la ejecución.
-   Las secciones críticas se usan para una sección de código que requiere acceso exclusivo a algún conjunto de datos compartidos antes de que se pueda ejecutar y que solo los subprocesos de un único proceso usan. Una sección crítica es como un paso a través del cual se puede pasar un solo subproceso a la vez, lo que funciona de la siguiente manera:
    -   Para asegurarse de que no hay más de un subproceso a la vez que tiene acceso a los datos compartidos, el subproceso principal de un proceso asigna una estructura de datos de sección crítica global \_ e inicializa sus miembros. Un subproceso que entra en una sección crítica llama a la función [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) y modifica los miembros de la estructura de datos.
    -   Un subproceso que intenta entrar en una sección crítica llama a [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) , que comprueba si se ha modificado la estructura de datos de la \_ sección crítica. Si es así, hay otro subproceso en la sección crítica y el subproceso subsiguiente se pone en suspensión. Un subproceso que sale de una sección crítica llama a [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection), que restablece la estructura de datos. Cuando un subproceso deja una sección crítica, el sistema reactiva uno de los subprocesos inactivos, que luego entra en la sección crítica.
-   Las exclusiones mutuas realizan la misma función que una sección crítica, salvo que la exclusión mutua es accesible para los subprocesos que se ejecutan en procesos diferentes. La propiedad de un objeto mutex es como tener el piso en un debate. Un proceso crea un objeto de exclusión mutua mediante una llamada a la función [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) , que devuelve un identificador. El primer subproceso que solicita un objeto mutex obtiene su propiedad. Cuando el subproceso ha terminado con la exclusión mutua, la propiedad pasa a otros subprocesos en función de la primera vez que se atiende.
-   Los semáforos se utilizan para mantener un recuento de referencias en algún recurso disponible. Un subproceso crea un semáforo para un recurso mediante una llamada a la función [**createsemaphore (**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) y pasando un puntero al recurso, un recuento inicial de recursos y el recuento máximo de recursos. Esta función devuelve un identificador. Un subproceso que solicita un recurso pasa su identificador de semáforo en una llamada a la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) . El objeto Semaphore sondea el recurso para determinar si está disponible. Si es así, el semáforo disminuye el recuento de recursos y reactiva el subproceso en espera. Si el recuento es cero, el subproceso permanece suspendido hasta que otro subproceso libera un recurso, lo que hace que el semáforo aumente el número a uno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre apartamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elegir el modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de un solo subproceso](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 