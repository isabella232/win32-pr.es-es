---
description: Los subprocesos se programan para ejecutarse en función de su prioridad de programación.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Prioridades de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062803"
---
# <a name="scheduling-priorities"></a>Prioridades de programación

Los subprocesos se programan para ejecutarse en función de *su prioridad de programación.* A cada subproceso se le asigna una prioridad de programación. Los niveles de prioridad van de cero (prioridad más baja) a 31 (prioridad más alta). Solo el subproceso de página cero puede tener una prioridad de cero. (El subproceso de página cero es un subproceso del sistema responsable de la puesta a cero de las páginas libres cuando no hay ningún otro subproceso que tenga que ejecutarse).

El sistema trata todos los subprocesos con la misma prioridad que igual. El sistema asigna segmentos de tiempo de forma round robin a todos los subprocesos con la prioridad más alta. Si ninguno de estos subprocesos está listo para ejecutarse, el sistema asigna segmentos de tiempo de forma round robin a todos los subprocesos con la prioridad más alta siguiente. Si un subproceso de mayor prioridad está disponible para ejecutarse, el sistema deja de ejecutar el subproceso de prioridad inferior (sin permitir que termine de usar su segmento de tiempo) y asigna un segmento de tiempo completo al subproceso de prioridad más alta. Para obtener más información, vea [Modificadores de contexto.](context-switches.md)

La prioridad de cada subproceso viene determinada por los criterios siguientes:

-   Clase de prioridad de su proceso
-   Nivel de prioridad del subproceso dentro de la clase de prioridad de su proceso

La clase de prioridad y el nivel de prioridad se combinan para formar la *prioridad base* de un subproceso. Para obtener información sobre la prioridad dinámica de un subproceso, vea [Aumentos de prioridad.](priority-boosts.md)

## <a name="priority-class"></a>Priority (clase)

Cada proceso pertenece a una de las siguientes clases de prioridad:<dl> IDLE \_ PRIORITY \_ (CLASE)  
CLASE POR \_ \_ DEBAJO DE LA PRIORIDAD \_ NORMAL  
NORMAL \_ PRIORITY \_ (CLASE)  
ABOVE \_ NORMAL \_ PRIORITY \_ CLASS  
HIGH \_ PRIORITY \_ (CLASE)  
CLASE \_ PRIORITY EN \_ TIEMPO REAL  
</dl>

De forma predeterminada, la clase de prioridad de un proceso es NORMAL \_ PRIORITY \_ CLASS. Use la [**función CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) para especificar la clase de prioridad de un proceso secundario al crearlo. Si el proceso de llamada es IDLE \_ PRIORITY CLASS o BELOW NORMAL PRIORITY \_ \_ \_ \_ CLASS, el nuevo proceso heredará esta clase. Use la [**función GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) para determinar la clase de prioridad actual de un proceso y la [**función SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para cambiar la clase priority de un proceso.

Los procesos que supervisan el sistema, como protectores de pantalla o aplicaciones que actualizan periódicamente una pantalla, deben usar IDLE \_ PRIORITY \_ CLASS. Esto evita que los subprocesos de este proceso, que no tienen prioridad alta, interfieran con subprocesos de mayor prioridad.

Use HIGH \_ PRIORITY \_ CLASS con cuidado. Si un subproceso se ejecuta en el nivel de prioridad más alto durante períodos extendidos, otros subprocesos del sistema no tendrán tiempo de procesador. Si se establecen varios subprocesos con prioridad alta al mismo tiempo, los subprocesos pierden su eficacia. La clase de prioridad alta debe reservarse para los subprocesos que deben responder a eventos críticos para el tiempo. Si la aplicación realiza una tarea que requiere la clase de prioridad alta mientras que el resto de sus tareas tienen prioridad normal, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para generar temporalmente la clase de prioridad de la aplicación; después, rebajála una vez completada la tarea de tiempo crítico. Otra estrategia es crear un proceso de alta prioridad que tenga todos sus subprocesos bloqueados la mayor parte del tiempo, resalte los subprocesos solo cuando se necesiten tareas críticas. Lo importante es que un subproceso de prioridad alta se ejecute durante un breve período de tiempo y solo cuando tenga que realizar un trabajo crítico para el tiempo.

Casi nunca debe usar REALTIME PRIORITY CLASS, ya que esto interrumpe los subprocesos del sistema que administran la entrada del mouse, la entrada del teclado y el vaciado \_ del disco en segundo \_ plano. Esta clase puede ser adecuada para las aplicaciones que "se hablan" directamente con el hardware o que realizan tareas breves que deben tener interrupciones limitadas.

## <a name="priority-level"></a>Nivel de prioridad

Los siguientes son los niveles de prioridad dentro de cada clase de prioridad:<dl> PRIORIDAD \_ DE SUBPROCESO \_ INACTIVA  
PRIORIDAD \_ MÁS BAJA DEL \_ SUBPROCESO  
PRIORIDAD \_ DEL SUBPROCESO POR \_ DEBAJO DE LO \_ NORMAL  
PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO  
PRIORIDAD \_ DEL SUBPROCESO POR ENCIMA DE LO \_ \_ NORMAL  
PRIORIDAD \_ MÁS ALTA DEL \_ SUBPROCESO  
TIEMPO CRÍTICO \_ DE \_ PRIORIDAD DEL \_ SUBPROCESO  
</dl>

Todos los subprocesos se crean mediante THREAD \_ PRIORITY \_ NORMAL. Esto significa que la prioridad del subproceso es la misma que la clase de prioridad de proceso. Después de crear un subproceso, use la [**función SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) para ajustar su prioridad con respecto a otros subprocesos del proceso.

Una estrategia típica es usar THREAD PRIORITY ABOVE NORMAL o THREAD PRIORITY HIGHEST para el subproceso de entrada del proceso, para asegurarse de que la aplicación responde \_ \_ al \_ \_ \_ usuario. Los subprocesos en segundo plano, especialmente los que consumen muchos procesadores, se pueden establecer en THREAD PRIORITY BELOW NORMAL o THREAD PRIORITY LOWEST, para asegurarse de que se pueden adelantar cuando \_ \_ sea \_ \_ \_ necesario. Sin embargo, si tiene un subproceso esperando a que otro subproceso con una prioridad inferior complete alguna tarea, asegúrese de bloquear la ejecución del subproceso de alta prioridad en espera. Para ello, use una función [wait](../sync/wait-functions.md), [una sección](../sync/critical-section-objects.md)crítica o la función [**Sleep,**](/windows/win32/api/synchapi/nf-synchapi-sleep) [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)o [**SwitchToThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) Esto es preferible a hacer que el subproceso ejecute un bucle. De lo contrario, el proceso puede quedar interbloqueado, porque el subproceso con prioridad inferior nunca está programado.

Para determinar el nivel de prioridad actual de un subproceso, use la [**función GetThreadPriority.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)

## <a name="base-priority"></a>Prioridad base

La clase de prioridad de proceso y el nivel de prioridad del subproceso se combinan para formar la prioridad base de cada subproceso.

En la tabla siguiente se muestra la prioridad base para las combinaciones de clase de prioridad de proceso y valor de prioridad de subproceso.


<table>
<tr>
<th colspan="2">Clase de prioridad de proceso</th>
<th>Nivel de prioridad del subproceso</th>
<th>Prioridad base</th>
</tr>
<tr>
<td rowspan="7" colspan="2">IDLE_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>2</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>3</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">BELOW_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">ABOVE_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">HIGH_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>13</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>14</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>15</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">REALTIME_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>16</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>22</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>23</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>24</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>25</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>26</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>31</td>
</tr>
</table>

 

 

 
