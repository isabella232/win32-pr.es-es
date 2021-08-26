---
description: Un grupo de subprocesos es una colección de subprocesos de trabajo que ejecutan eficazmente devoluciones de llamada asincrónicas en nombre de la aplicación.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Grupos de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7918a0f6f0b881233ebea8e664d6e743a7bff105e265270063b08af313417e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081265"
---
# <a name="thread-pools"></a>Grupos de subprocesos

Un *grupo de subprocesos* es una colección de subprocesos de trabajo que ejecutan eficazmente devoluciones de llamada asincrónicas en nombre de la aplicación. El grupo de subprocesos se usa principalmente para reducir el número de subprocesos de aplicación y proporcionar administración de los subprocesos de trabajo. Las aplicaciones pueden poner en cola los elementos de trabajo, asociar el trabajo con identificadores que se pueden esperar, poner en cola automáticamente en función de un temporizador y enlazar con E/S.

## <a name="thread-pool-architecture"></a>Arquitectura del grupo de subprocesos

Las siguientes aplicaciones pueden beneficiarse del uso de un grupo de subprocesos:

-   Una aplicación que es muy paralela y puede enviar un gran número de elementos de trabajo pequeños de forma asincrónica (como la búsqueda de índices distribuidos o la E/S de red).
-   Una aplicación que crea y destruye un gran número de subprocesos que se ejecutan durante un breve período de tiempo. El uso del grupo de subprocesos puede reducir la complejidad de la administración de subprocesos y la sobrecarga implicada en la creación y destrucción de subprocesos.
-   Aplicación que procesa elementos de trabajo independientes en segundo plano y en paralelo (como cargar varias pestañas).
-   Una aplicación que debe realizar una espera exclusiva en objetos de kernel o bloquear los eventos entrantes en un objeto. El uso del grupo de subprocesos puede reducir la complejidad de la administración de subprocesos y aumentar el rendimiento al reducir el número de modificadores de contexto.
-   Aplicación que crea subprocesos de espera personalizados para esperar eventos.

El grupo de subprocesos original se ha reorganizado completamente en Windows Vista. El nuevo grupo de subprocesos se mejora porque proporciona un único tipo de subproceso de trabajo (admite E/S y no E/S), no usa un subproceso de temporizador, proporciona una cola de temporizador única y proporciona un subproceso persistente dedicado. También proporciona grupos de limpieza, un mayor rendimiento, varios grupos por proceso que se programan de forma independiente y una nueva API de grupo de subprocesos.

La arquitectura del grupo de subprocesos consta de lo siguiente:

-   Subprocesos de trabajo que ejecutan las funciones de devolución de llamada
-   Subprocesos de waiter que esperan en varios identificadores de espera
-   Una cola de trabajo
-   Un grupo de subprocesos predeterminado para cada proceso
-   Un generador de trabajo que administra los subprocesos de trabajo

## <a name="best-practices"></a>Prácticas recomendadas

La nueva [API del grupo de subprocesos](thread-pool-api.md) proporciona más flexibilidad y control que la API original del grupo de [subprocesos](thread-pooling.md). Sin embargo, hay algunas diferencias sutiles pero importantes. En la API original, el restablecimiento de espera era automático; en la nueva API, la espera se debe restablecer explícitamente cada vez. La API original controló la suplantación automáticamente, transfiriendo el contexto de seguridad del proceso de llamada al subproceso. Con la nueva API, la aplicación debe establecer explícitamente el contexto de seguridad.

Estos son los procedimientos recomendados al usar un grupo de subprocesos:

-   Los subprocesos de un proceso comparten el grupo de subprocesos. Un único subproceso de trabajo puede ejecutar varias funciones de devolución de llamada, de una en una. El grupo de subprocesos administra estos subprocesos de trabajo. Por lo tanto, no finalice un subproceso del grupo de subprocesos llamando a [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) en el subproceso o llamando a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) desde una función de devolución de llamada.
-   Una solicitud de E/S se puede ejecutar en cualquier subproceso del grupo de subprocesos. La cancelación de E/S en un subproceso del grupo de subprocesos requiere sincronización porque la función cancel podría ejecutarse en un subproceso diferente del que está controlando la solicitud de E/S, lo que puede dar lugar a la cancelación de una operación desconocida. Para evitar esto, proporcione siempre la estructura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) con la que se inició una solicitud de E/S al llamar a [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) para E/S asincrónica, o use su propia sincronización para asegurarse de que no se pueda iniciar ninguna otra E/S en el subproceso de destino antes de llamar a la función [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) o **CancelIoEx.**
-   Limpie todos los recursos creados en la función de devolución de llamada antes de volver de la función. Estos incluyen TLS, contextos de seguridad, prioridad de subproceso y registro COM. Las funciones de devolución de llamada también deben restaurar el estado del subproceso antes de volver.
-   Mantenga los identificadores de espera y sus objetos asociados activo hasta que el grupo de subprocesos haya señalado que ha finalizado con el identificador.
-   Marque todos los subprocesos que están esperando operaciones largas (como vaciados de E/S o limpieza de recursos) para que el grupo de subprocesos pueda asignar nuevos subprocesos en lugar de esperar a este.
-   Antes de descargar un archivo DLL que usa el grupo de subprocesos, cancele todos los elementos de trabajo, E/S, operaciones de espera y temporizadores, y espere a que se completen las devoluciones de llamada de ejecución.
-   Evite interbloqueos eliminando las dependencias entre los elementos de trabajo y entre las devoluciones de llamada, asegurándose de que una devolución de llamada no está esperando a que se complete y conservando la prioridad del subproceso.
-   No poner en cola demasiados elementos demasiado rápido en un proceso con otros componentes mediante el grupo de subprocesos predeterminado. Hay un grupo de subprocesos predeterminado por proceso, incluidos Svchost.exe. De forma predeterminada, cada grupo de subprocesos tiene un máximo de 500 subprocesos de trabajo. El grupo de subprocesos intenta crear más subprocesos de trabajo cuando el número de subprocesos de trabajo en estado listo o en ejecución debe ser menor que el número de procesadores.
-   Evite el modelo de apartamento de un solo subproceso COM, ya que no es compatible con el grupo de subprocesos. STA crea el estado del subproceso que puede afectar al siguiente elemento de trabajo para el subproceso. STA suele ser de larga duración y tiene afinidad de subproceso, lo que es lo contrario del grupo de subprocesos.
-   Cree un nuevo grupo de subprocesos para controlar la prioridad y el aislamiento de subprocesos, crear características personalizadas y posiblemente mejorar la capacidad de respuesta. Sin embargo, los grupos de subprocesos adicionales requieren más recursos del sistema (subprocesos, memoria de kernel). Demasiados grupos aumenta el potencial de contención de CPU.
-   Si es posible, use un objeto que se puede esperar en lugar de un mecanismo basado en APC para señalar un subproceso de grupo de subprocesos. Las API no funcionan tan bien con los subprocesos del grupo de subprocesos como otros mecanismos de señalización porque el sistema controla la duración de los subprocesos del grupo de subprocesos, por lo que es posible que un subproceso finalice antes de que se entregue la notificación.
-   Use la extensión del depurador del grupo de subprocesos, !tp. Este comando tiene el siguiente uso:

    -   marcas *de direcciones de* *grupo*
    -   Marcas de *dirección*  obj
    -   Marcas de dirección *de*  tqueue
    -   dirección del *waiter*
    -   dirección de *trabajo*

    Para pool, waiter y worker, si la dirección es cero, el comando vuelca todos los objetos. Para el waiter y el trabajo, la omisión de la dirección vuelca el subproceso actual. Se definen las marcas siguientes: 0x1 (salida de una sola línea), 0x2 (miembros de volcado) y 0x4 (cola de trabajo del grupo de volcado).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API del grupo de subprocesos](thread-pool-api.md)
</dt> <dt>

[Uso de las funciones del grupo de subprocesos](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
