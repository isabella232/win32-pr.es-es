---
description: Los subprocesos están programados para ejecutarse en función de su prioridad de programación.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Prioridades de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677837"
---
# <a name="scheduling-priorities"></a>Prioridades de programación

Los subprocesos están programados para ejecutarse en función de su *prioridad de programación*. A cada subproceso se le asigna una prioridad de programación. Los niveles de prioridad van desde cero (prioridad más baja) hasta 31 (prioridad más alta). Solo el subproceso de página cero puede tener una prioridad de cero. (El subproceso de página cero es un subproceso del sistema responsable de cero páginas libres cuando no hay otros subprocesos que deban ejecutarse).

El sistema trata todos los subprocesos con la misma prioridad que iguales. El sistema asigna los intervalos de tiempo en un modo Round-Robin a todos los subprocesos con la prioridad más alta. Si ninguno de estos subprocesos está listo para ejecutarse, el sistema asigna los intervalos de tiempo en un modo Round-Robin a todos los subprocesos con la siguiente prioridad más alta. Si un subproceso de mayor prioridad está disponible para ejecutarse, el sistema deja de ejecutar el subproceso de prioridad más baja (sin permitir que termine de usar su intervalo de tiempo) y asigna un intervalo de tiempo completo al subproceso de prioridad superior. Para obtener más información, vea [cambios de contexto](context-switches.md).

La prioridad de cada subproceso viene determinada por los siguientes criterios:

-   La clase de prioridad de su proceso
-   Nivel de prioridad del subproceso dentro de la clase de prioridad de su proceso.

La clase de prioridad y el nivel de prioridad se combinan para formar la *prioridad base* de un subproceso. Para obtener información sobre la prioridad dinámica de un subproceso, consulte [aumentos de prioridad](priority-boosts.md).

## <a name="priority-class"></a>Priority (clase)

Cada proceso pertenece a una de las siguientes clases de prioridad:<dl> \_clase de prioridad INactiva \_  
POR debajo de la \_ \_ clase de prioridad normal \_  
\_clase de prioridad normal \_  
POR encima de la \_ \_ clase de prioridad normal \_  
\_clase de prioridad alta \_  
\_clase de prioridad en tiempo real \_  
</dl>

De forma predeterminada, la clase de prioridad de un proceso es la \_ clase de prioridad normal \_ . Utilice la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) para especificar la clase de prioridad de un proceso secundario cuando lo cree. Si el proceso que realiza la llamada es una clase de prioridad inactiva \_ o una \_ clase de \_ \_ prioridad normal \_ , el nuevo proceso heredará esta clase. Utilice la función [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) para determinar la clase de prioridad actual de un proceso y la función [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para cambiar la clase de prioridad de un proceso.

Los procesos que supervisan el sistema, como los protectores de pantalla o las aplicaciones que actualizan periódicamente una pantalla, deben usar la clase de prioridad inactiva \_ \_ . Esto evita que los subprocesos de este proceso, que no tienen una prioridad alta, interfieran con subprocesos de mayor prioridad.

Use la \_ \_ clase de prioridad alta con cuidado. Si un subproceso se ejecuta en el nivel de prioridad más alto durante períodos prolongados, otros subprocesos del sistema no obtendrán el tiempo de procesador. Si varios subprocesos se establecen en alta prioridad al mismo tiempo, los subprocesos pierden su eficacia. La clase de prioridad alta se debe reservar para los subprocesos que deben responder a eventos críticos en el tiempo. Si la aplicación realiza una tarea que requiere la clase de prioridad alta, mientras que el resto de sus tareas es una prioridad normal, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para aumentar temporalmente la clase de prioridad de la aplicación. a continuación, reduzca el tiempo después de que se haya completado la tarea crítica temporal. Otra estrategia consiste en crear un proceso de alta prioridad que tenga todos los subprocesos bloqueados la mayor parte del tiempo, activando los subprocesos solo cuando se necesitan tareas críticas. Lo importante es que un subproceso de prioridad alta debe ejecutarse durante un breve período de tiempo y solo cuando tenga trabajo crítico en el tiempo.

Casi nunca se debe usar \_ \_ la clase de prioridad en tiempo real, porque interrumpe los subprocesos del sistema que administran la entrada del mouse, la entrada del teclado y el vaciado del disco en segundo plano. Esta clase puede ser adecuada para las aplicaciones que "hablan" directamente en el hardware o que realizan tareas breves que deben tener interrupciones limitadas.

## <a name="priority-level"></a>Nivel de prioridad

A continuación se muestran los niveles de prioridad dentro de cada clase de prioridad:<dl> prioridad de subproceso \_ \_ inactiva  
prioridad de subproceso \_ \_ más baja  
prioridad de subproceso \_ \_ por debajo de lo \_ normal  
prioridad de subproceso \_ \_ normal  
prioridad de subproceso \_ \_ por encima de lo \_ normal  
prioridad de subproceso \_ \_ más alta  
tiempo de prioridad de subproceso \_ \_ \_ crítico  
</dl>

Todos los subprocesos se crean mediante la prioridad de subproceso \_ \_ normal. Esto significa que la prioridad del subproceso es la misma que la clase de prioridad del proceso. Después de crear un subproceso, utilice la función [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) para ajustar su prioridad en relación con otros subprocesos del proceso.

Una estrategia típica es usar la prioridad de subprocesos por \_ \_ encima \_ \_ de la normal o la prioridad de subproceso \_ más alta para el subproceso de entrada del proceso, para asegurarse de que la aplicación responde al usuario. Los subprocesos en segundo plano, especialmente aquellos que usan un uso intensivo del procesador, se pueden establecer en prioridad de subproceso \_ \_ por debajo de la \_ prioridad normal o de subproceso \_ \_ más baja, para asegurarse de que se pueden cambiar cuando sea necesario. Sin embargo, si tiene un subproceso que está esperando a otro subproceso con una prioridad más baja para completar alguna tarea, asegúrese de bloquear la ejecución del subproceso de alta prioridad en espera. Para ello, use una [función wait](../sync/wait-functions.md), una [sección Critical](../sync/critical-section-objects.md)o la función [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) . Es preferible que el subproceso ejecute un bucle. De lo contrario, el proceso puede quedar interbloqueado, ya que el subproceso con prioridad inferior nunca está programado.

Para determinar el nivel de prioridad actual de un subproceso, utilice la función [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .

## <a name="base-priority"></a>Prioridad base

La clase de prioridad del proceso y el nivel de prioridad del subproceso se combinan para formar la prioridad base de cada subproceso.

En la tabla siguiente se muestra la prioridad base de las combinaciones de clase de prioridad de proceso y valor de prioridad de subproceso.


<table>
<tr>
<th colspan="2">Clase de prioridad del proceso</th>
<th>Nivel de prioridad de subproceso</th>
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

 

 

 
