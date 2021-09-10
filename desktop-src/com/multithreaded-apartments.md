---
title: Departamentos multiproceso
description: Departamentos multiproceso
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2594f9341fc662b068fb7e007e538282a31273
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369483"
---
# <a name="multithreaded-apartments"></a>Departamentos multiproceso

En un modelo de apartamento multiproceso, todos los subprocesos del proceso que se han inicializado como subproceso libre residen en un único apartamento. Por lo tanto, no es necesario serializar entre subprocesos. Los subprocesos no necesitan recuperar y enviar mensajes porque COM no usa mensajes de ventana en este modelo.

Las llamadas a métodos de objetos del apartamento multiproceso se pueden ejecutar en cualquier subproceso del apartamento. No hay ninguna serialización de llamadas; muchas llamadas pueden producirse al mismo método o al mismo objeto simultáneamente. Los objetos creados en el apartamento multiproceso deben ser capaces de controlar las llamadas en sus métodos desde otros subprocesos en cualquier momento.

Dado que las llamadas a objetos no se serializan de ninguna manera, la simultaneidad de objetos multiproceso ofrece el máximo rendimiento y aprovecha mejor el hardware de varios procesadores para llamadas entre subprocesos, entre procesos y entre equipos. Sin embargo, esto significa que el código de los objetos debe proporcionar sincronización en sus implementaciones de interfaz, normalmente mediante el uso de primitivas de sincronización como objetos de evento, secciones críticas, exclusiones mutuas o semáforos, que se describen más adelante en esta sección. Además, como el objeto no controla la duración de los subprocesos que acceden a él, no se puede almacenar ningún estado específico del subproceso en el objeto (en el almacenamiento local del subproceso).

A continuación se incluyen algunas consideraciones importantes relacionadas con la sincronización de los hoteles multiproceso:

-   COM proporciona sincronización de llamadas solo para los departamentos de un solo subproceso.
-   Los departamentos multiproceso no reciben llamadas al realizar llamadas (en el mismo subproceso).
-   Los departamentos multiproceso no pueden realizar llamadas sincronizadas con entrada.
-   Las llamadas asincrónicas se convierten en llamadas sincrónicas en los departamentos multiproceso.
-   No se llama al filtro de mensajes para ningún subproceso de un apartamento multiproceso.

Para inicializar un subproceso como subproceso libre, llame a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)y especifique COINIT \_ MULTITHREADED. Para obtener información sobre los subprocesos del servidor en proceso, vea [In-Process Server Threading Issues](in-process-server-threading-issues.md).

Varios clientes pueden llamar simultáneamente, desde subprocesos diferentes, a un objeto que admite el subprocesamiento libre. En servidores fuera de proceso sin subprocesos, COM, a través del subsistema RPC, crea un grupo de subprocesos en el proceso del servidor y cualquiera de estos subprocesos puede entregar una llamada de cliente (o varias llamadas de cliente) en cualquier momento. Un servidor fuera de proceso también debe implementar la sincronización en su generador de clases. Los objetos en proceso de subproceso libre pueden recibir llamadas directas desde varios subprocesos del cliente.

El cliente puede realizar el trabajo COM en varios subprocesos. Todos los subprocesos pertenecen al mismo apartamento multiproceso. Los punteros de interfaz se pasan directamente de subproceso a subproceso dentro de un apartamento multiproceso, por lo que los punteros de interfaz no se serializan entre sus subprocesos. Los filtros de mensajes (implementaciones [**de IMessageFilter)**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)no se usan en los departamentos multiproceso. El subproceso de cliente se suspenderá cuando realiza una llamada COM a objetos fuera de apartamento y se reanudará cuando se devuelva la llamada. Rpc sigue administrando las llamadas entre procesos.

Los subprocesos inicializados con el modelo de subproceso libre deben implementar su propia sincronización. Como se mencionó anteriormente en esta sección, Windows esta implementación a través de las primitivas de sincronización siguientes:

-   Los objetos de evento proporcionan una manera de señalar uno o varios subprocesos de que se ha producido un evento. Cualquier subproceso dentro de un proceso puede crear un objeto de evento. La función de creación de eventos [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)devuelve un identificador para el evento . Una vez creado un objeto de evento, los subprocesos con un identificador para el objeto pueden esperar en él antes de continuar con la ejecución.
-   Las secciones críticas se usan para una sección de código que requiere acceso exclusivo a algún conjunto de datos compartidos antes de que se puedan ejecutar y que solo los subprocesos usan dentro de un único proceso. Una sección crítica es como un giro a través del cual solo puede pasar un subproceso a la vez, funcionando de la siguiente manera:
    -   Para asegurarse de que no más de un subproceso a la vez accede a los datos compartidos, el subproceso principal de un proceso asigna una estructura de datos CRITICAL SECTION global e inicializa \_ sus miembros. Un subproceso que entra en una sección crítica llama a [**la función EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) y modifica los miembros de la estructura de datos.
    -   Un subproceso que intenta entrar en una sección crítica llama a [**EnterCriticalSection,**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) que comprueba si se ha modificado la estructura de datos \_ CRITICAL SECTION. Si es así, otro subproceso se encuentra actualmente en la sección crítica y el subproceso posterior se pone en suspensión. Un subproceso que sale de una sección crítica llama [**a LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection), que restablece la estructura de datos. Cuando un subproceso sale de una sección crítica, el sistema reactiva uno de los subprocesos en modo de espera, que luego entra en la sección crítica.
-   Las exclusiones mutuas realizan la misma función que una sección crítica, salvo que la exclusión mutua es accesible para los subprocesos que se ejecutan en procesos diferentes. Poseer un objeto de exclusión mutua es como tener la palabra en un debate. Un proceso crea un objeto mutex llamando a la [**función CreateMutex,**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) que devuelve un identificador. El primer subproceso que solicita un objeto de exclusión mutua obtiene su propiedad. Cuando el subproceso ha terminado con la exclusión mutua, la propiedad pasa a otros subprocesos por primera vez y por primera vez.
-   Los semáforos se usan para mantener un recuento de referencias en algún recurso disponible. Un subproceso crea un semáforo para un recurso llamando a la función [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) y pasando un puntero al recurso, un recuento inicial de recursos y el número máximo de recursos. Esta función devuelve un identificador. Un subproceso que solicita un recurso pasa su identificador de semáforo en una llamada a la [**función WaitForSingleObject.**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) El objeto semáforo sondea el recurso para determinar si está disponible. Si es así, el semáforo disminuye el número de recursos y reactiva el subproceso en espera. Si el recuento es cero, el subproceso permanece en estado de desuso hasta que otro subproceso libera un recurso, lo que hace que el semáforo incremente el recuento a uno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre departamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elección del modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Problemas de subprocesos del servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de subproceso único](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Departamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 