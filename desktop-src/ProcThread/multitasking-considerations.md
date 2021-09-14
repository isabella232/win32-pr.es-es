---
description: La guía recomendada es usar el menor número posible de subprocesos, lo que minimiza el uso de recursos del sistema.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Consideraciones sobre multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375031"
---
# <a name="multitasking-considerations"></a>Consideraciones sobre multitarea

La guía recomendada es usar el menor número posible de subprocesos, lo que minimiza el uso de recursos del sistema. De este modo se aumenta el rendimiento. Multitasking tiene requisitos de recursos y posibles conflictos que se deben tener en cuenta al diseñar la aplicación. Los requisitos de recursos son los siguientes:

-   El sistema consume memoria para la información de contexto requerida por los procesos y subprocesos. Por lo tanto, el número de procesos y subprocesos que se pueden crear está limitado por la memoria disponible.
-   Realizar un seguimiento de un número elevado de subprocesos consume un tiempo de procesador significativo. Si hay demasiados subprocesos, la mayoría de ellos no podrán realizar progresos significativos. Si la mayoría de los subprocesos actuales se encuentran en un proceso, los subprocesos de otros procesos se programan con menos frecuencia.

Proporcionar acceso compartido a los recursos puede generar conflictos. Para evitarlos, debe sincronizar el acceso a los recursos compartidos. Esto es así para los recursos del sistema (como los puertos de comunicaciones), los recursos compartidos por varios procesos (como identificadores de archivo) o los recursos de un único proceso (como las variables globales) a los que acceden varios subprocesos. Si no se sincroniza correctamente el acceso (en el mismo proceso o en procesos diferentes), se pueden producir problemas como condiciones de interbloqueo y carrera. Los objetos de sincronización y las funciones que puede usar para coordinar el uso compartido de recursos entre varios subprocesos. Para obtener más información sobre la sincronización, vea Sincronizar la ejecución [de varios subprocesos.](synchronizing-execution-of-multiple-threads.md) Reducir el número de subprocesos facilita y hace más eficaz sincronizar los recursos.

Un buen diseño para una aplicación multiproceso es el servidor de canalización. En este diseño, se crea un subproceso por procesador y se crean colas de solicitudes para las que la aplicación mantiene la información de contexto. Un subproceso procesaría todas las solicitudes de una cola antes de procesar las solicitudes en la cola siguiente.

 

 



