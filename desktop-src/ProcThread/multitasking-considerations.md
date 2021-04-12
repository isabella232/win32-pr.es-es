---
description: La directriz recomendada es usar el menor número posible de subprocesos, lo que minimiza el uso de los recursos del sistema.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Consideraciones sobre la multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156516"
---
# <a name="multitasking-considerations"></a>Consideraciones sobre la multitarea

La directriz recomendada es usar el menor número posible de subprocesos, lo que minimiza el uso de los recursos del sistema. De este modo se aumenta el rendimiento. La multitarea tiene requisitos de recursos y posibles conflictos que se deben tener en cuenta al diseñar la aplicación. Los requisitos de recursos son los siguientes:

-   El sistema consume memoria para la información de contexto requerida por los procesos y los subprocesos. Por lo tanto, el número de procesos y subprocesos que se pueden crear está limitado por la memoria disponible.
-   Realizar un seguimiento de un número elevado de subprocesos consume un tiempo de procesador significativo. Si hay demasiados subprocesos, la mayoría de ellos no podrán realizar un progreso significativo. Si la mayoría de los subprocesos actuales se encuentran en un proceso, los subprocesos de otros procesos se programan con menos frecuencia.

Proporcionar acceso compartido a los recursos puede generar conflictos. Para evitarlos, debe sincronizar el acceso a los recursos compartidos. Esto se cumple para los recursos del sistema (como los puertos de comunicaciones), los recursos compartidos por varios procesos (como los identificadores de archivo) o los recursos de un único proceso (como las variables globales) a los que tienen acceso varios subprocesos. Si no se sincroniza el acceso correctamente (en el mismo proceso o en procesos diferentes), pueden producirse problemas como el interbloqueo y las condiciones de carrera. Los objetos de sincronización y las funciones que puede usar para coordinar el uso compartido de recursos entre varios subprocesos. Para obtener más información acerca de la sincronización, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md). Reducir el número de subprocesos hace que sea más fácil y eficaz sincronizar los recursos.

Un buen diseño para una aplicación multiproceso es el servidor de canalización. En este diseño, se crea un subproceso por procesador y se crean colas de solicitudes para las que la aplicación mantiene la información de contexto. Un subproceso procesaría todas las solicitudes de una cola antes de procesar las solicitudes en la siguiente cola.

 

 



