---
description: Un grupo de subprocesos es una colección de subprocesos de trabajo que ejecutan de forma eficaz las devoluciones de llamada asincrónicas en nombre de la aplicación.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Grupos de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690aa3eb6fd3ce7a99d71e0f57118529ef79113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677987"
---
# <a name="thread-pools"></a>Grupos de subprocesos

Un *grupo de subprocesos* es una colección de subprocesos de trabajo que ejecutan de forma eficaz las devoluciones de llamada asincrónicas en nombre de la aplicación. El grupo de subprocesos se usa principalmente para reducir el número de subprocesos de aplicación y proporcionar administración de los subprocesos de trabajo. Las aplicaciones pueden poner en cola los elementos de trabajo, asociar el trabajo con los identificadores de espera, poner en cola automáticamente en función de un temporizador y enlazar con e/s.

## <a name="thread-pool-architecture"></a>Arquitectura de grupo de subprocesos

Las aplicaciones siguientes pueden beneficiarse del uso de un grupo de subprocesos:

-   Una aplicación muy paralela y puede distribuir un gran número de elementos de trabajo pequeños de forma asincrónica (por ejemplo, búsqueda de índice distribuida o e/s de red).
-   Aplicación que crea y destruye un gran número de subprocesos que se ejecutan durante un breve período de tiempo. El uso del grupo de subprocesos puede reducir la complejidad de la administración de subprocesos y la sobrecarga que implica la creación y destrucción de subprocesos.
-   Aplicación que procesa elementos de trabajo independientes en segundo plano y en paralelo (por ejemplo, la carga de varias pestañas).
-   Aplicación que debe realizar una espera exclusiva en los objetos de kernel o bloquear los eventos de entrada en un objeto. El uso del grupo de subprocesos puede reducir la complejidad de la administración de subprocesos y aumentar el rendimiento al reducir el número de cambios de contexto.
-   Aplicación que crea subprocesos de espera personalizados para esperar en los eventos.

El grupo de subprocesos original se ha rediseñado completamente en Windows Vista. El nuevo grupo de subprocesos mejora porque proporciona un único tipo de subproceso de trabajo (admite e/s y no e/s), no utiliza un subproceso de temporizador, proporciona una única cola de temporizador y proporciona un subproceso persistente dedicado. También proporciona grupos de limpieza, mayor rendimiento, varios grupos por proceso que se programan de forma independiente y una nueva API de grupo de subprocesos.

La arquitectura del grupo de subprocesos consta de lo siguiente:

-   Subprocesos de trabajo que ejecutan las funciones de devolución de llamada
-   Subprocesos en espera que esperan en varios identificadores de espera
-   Una cola de trabajo
-   Un grupo de subprocesos predeterminado para cada proceso
-   Un generador de trabajo que administra los subprocesos de trabajo

## <a name="best-practices"></a>Prácticas recomendadas

La nueva [API de grupo de subprocesos](thread-pool-api.md) proporciona más flexibilidad y control que la [API de grupo de subprocesos original](thread-pooling.md). Sin embargo, hay algunas diferencias sutiles pero importantes. En la API original, el restablecimiento de la espera era automático; en la nueva API, la espera debe restablecerse explícitamente cada vez. La API original controlaba la suplantación automáticamente, transfiriendo el contexto de seguridad del proceso de llamada al subproceso. Con la nueva API, la aplicación debe establecer explícitamente el contexto de seguridad.

A continuación se muestran los procedimientos recomendados para usar un grupo de subprocesos:

-   Los subprocesos de un proceso comparten el grupo de subprocesos. Un único subproceso de trabajo puede ejecutar varias funciones de devolución de llamada, de una en una. Estos subprocesos de trabajo se administran mediante el grupo de subprocesos. Por consiguiente, no termine un subproceso del grupo de subprocesos llamando a [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) en el subproceso o llamando a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) desde una función de devolución de llamada.
-   Una solicitud de e/s se puede ejecutar en cualquier subproceso del grupo de subprocesos. La cancelación de e/s en un subproceso del grupo de subprocesos requiere sincronización porque la función de cancelación puede ejecutarse en un subproceso diferente al que controla la solicitud de e/s, lo que puede dar lugar a la cancelación de una operación desconocida. Para evitar esto, proporcione siempre la estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) con la que se inició una solicitud de e/s al llamar a [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) para la e/s asincrónica, o use su propia sincronización para asegurarse de que no se pueda iniciar ninguna otra e/s en el subproceso de destino antes de llamar a la función [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) o **CancelIoEx** .
-   Limpie todos los recursos creados en la función de devolución de llamada antes de volver de la función. Entre ellas se incluyen TLS, contextos de seguridad, prioridad de subprocesos y registro COM. Las funciones de devolución de llamada también deben restaurar el estado del subproceso antes de devolver.
-   Mantenga los controladores de espera y sus objetos asociados activos hasta que el grupo de subprocesos haya señalado que ha finalizado con el identificador.
-   Marque todos los subprocesos que están a la espera de operaciones largas (como vaciados de e/s o limpieza de recursos) para que el grupo de subprocesos pueda asignar nuevos subprocesos en lugar de esperar a este.
-   Antes de descargar un archivo DLL que usa el grupo de subprocesos, cancele todos los elementos de trabajo, e/s, operaciones de espera y temporizadores, y espere a que se complete la ejecución de las devoluciones de llamada.
-   Evite los interbloqueos eliminando las dependencias entre los elementos de trabajo y entre las devoluciones de llamada, asegurándose de que una devolución de llamada no está esperando a que se complete y conservando la prioridad del subproceso.
-   No ponga en cola demasiados elementos demasiado rápido en un proceso con otros componentes que usen el grupo de subprocesos predeterminado. Hay un grupo de subprocesos predeterminado por proceso, incluido Svchost.exe. De forma predeterminada, cada grupo de subprocesos tiene un máximo de 500 subprocesos de trabajo. El grupo de subprocesos intenta crear más subprocesos de trabajo cuando el número de subprocesos de trabajo en el estado listo/en ejecución debe ser menor que el número de procesadores.
-   Evite el modelo de apartamento de un solo subproceso COM, ya que no es compatible con el grupo de subprocesos. STA crea un estado de subproceso que puede afectar al siguiente elemento de trabajo para el subproceso. STA suele ser de larga duración y tiene afinidad de subprocesos, que es lo contrario que el grupo de subprocesos.
-   Cree un nuevo grupo de subprocesos para controlar la prioridad y el aislamiento de subprocesos, cree características personalizadas y, posiblemente, mejore la capacidad de respuesta. Sin embargo, los grupos de subprocesos adicionales requieren más recursos del sistema (subprocesos, memoria de kernel). Un número excesivo de grupos aumenta la posibilidad de contención de la CPU.
-   Si es posible, utilice un objeto que se puede esperar en lugar de un mecanismo basado en APC para indicar un subproceso del grupo de subprocesos. APC no funcionan también con subprocesos de grupo de subprocesos como otros mecanismos de señalización porque el sistema controla la duración de los subprocesos del grupo de subprocesos, por lo que es posible que un subproceso finalice antes de que se entregue la notificación.
-   Use la extensión del depurador del grupo de subprocesos,! TP. Este comando tiene el siguiente uso:

    -   *marcas* de *Dirección* de grupo
    -   *marcas* de *Dirección* de obj
    -   *marcas* de *Dirección* TNO
    -   *Dirección* de espera
    -   *Dirección* de trabajo

    En el caso de los grupos, waitr y Worker, si la dirección es cero, el comando vuelca todos los objetos. En wait y Worker, si se omite la dirección, se vuelca el subproceso actual. Se definen las marcas siguientes: 0x1 (salida de una sola línea), 0X2 (miembros de volcado de memoria) y 0x4 (cola de trabajo del grupo de volcado).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de grupo de subprocesos](thread-pool-api.md)
</dt> <dt>

[Usar las funciones de grupo de subprocesos](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
