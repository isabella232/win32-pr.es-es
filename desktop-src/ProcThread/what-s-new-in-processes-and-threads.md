---
description: Windows 7 y Windows Server 2008 R2 incluyen los siguientes elementos de programación nuevos para procesos y subprocesos.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Novedades de procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909662"
---
# <a name="whats-new-in-processes-and-threads"></a>Novedades de procesos y subprocesos

Windows 7 y Windows Server 2008 R2 incluyen los siguientes elementos de programación nuevos para procesos y subprocesos.

## <a name="new-capabilities"></a>Nuevas funcionalidades

Las versiones de 64 bits de Windows 7 y Windows Server 2008 R2 admiten más de 64 procesadores lógicos en un único equipo. Para obtener más información, consulte [grupos de procesadores](processor-groups.md).

La programación de modo de usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Para obtener más información, consulte [programación en modo usuario](user-mode-scheduling.md).

## <a name="new-functions"></a>Funciones nuevas

Las siguientes funciones nuevas se utilizan con procesadores y grupos de procesadores.



| Función                                                                                | Descripción                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Crea un subproceso que se ejecuta en el espacio de direcciones virtuales de otro proceso y, opcionalmente, especifica atributos extendidos, como la afinidad del grupo de procesadores.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Devuelve el número de procesadores activos en un grupo de procesadores o en el sistema.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Devuelve el número de grupos de procesadores activos en el sistema.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Recupera el grupo de procesadores y el número del procesador lógico en el que se está ejecutando el subproceso que realiza la llamada.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Recupera información acerca de las relaciones de los procesadores lógicos y el hardware relacionado.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Devuelve el número máximo de procesadores lógicos que puede tener un grupo de procesadores o el sistema.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Devuelve el número máximo de grupos de procesadores que el sistema puede tener. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Recupera la cantidad de memoria que está disponible en el nodo especificado como un valor USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Recupera el nodo NUMA asociado al dispositivo subyacente para un identificador de archivo.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Recupera la máscara del procesador para el nodo NUMA especificado como un valor USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Recupera el número de nodo del procesador lógico especificado como un valor USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Recupera el número de nodo como un valor USHORT para el identificador de proximidad especificado.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Recupera la afinidad del grupo de procesadores del proceso especificado.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Recupera el tiempo de ciclo en que cada procesador del grupo especificado dedicó a ejecutar llamadas a procedimiento diferidas (DPC) y rutinas de servicio de interrupción (ISR).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Recupera la afinidad del grupo de procesadores del subproceso especificado.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Recupera el número de procesador del procesador ideal para el subproceso especificado.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Recupera el tiempo de ciclo acumulado para el subproceso inactivo en cada procesador lógico del grupo de procesadores especificado. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Establece la afinidad del grupo de procesadores para el subproceso especificado.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Establece el procesador ideal para el subproceso especificado y, opcionalmente, recupera el procesador ideal anterior.<br/>                                                  |



 

Las siguientes funciones nuevas se utilizan con grupos de subprocesos.



| Función                                                                              | Descripción                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Recupera los tamaños de reserva de la pila y de confirmación para los subprocesos del grupo de subprocesos especificado.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Especifica que la devolución de llamada se debe ejecutar en un subproceso persistente.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Especifica la prioridad de una función de devolución de llamada relativa a otros elementos de trabajo en el mismo grupo de subprocesos.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Establece los tamaños de reserva de la pila y de confirmación para los nuevos subprocesos en el grupo de subprocesos especificado. <br/>              |



 

Las siguientes funciones nuevas se utilizan con UMS.



| Función                                                                          | Descripción                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Crea una lista de finalización de UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Crea un contexto de subproceso UMS para representar un subproceso de trabajo UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Elimina la lista de finalización de UMS especificada. La lista debe estar vacía.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Elimina el contexto del subproceso UMS especificado. El subproceso debe terminar.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Recupera los subprocesos de trabajo UMS de la lista de finalización de UMS especificada.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Convierte el subproceso que realiza la llamada en un subproceso del programador UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Ejecuta el subproceso de trabajo UMS especificado.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Devuelve el contexto del subproceso UMS del subproceso UMS que realiza la llamada.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Devuelve el siguiente contexto del subproceso UMS en una lista de contextos de subproceso UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Recupera un identificador para el evento asociado a la lista de finalización de UMS especificada.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Recupera información sobre el subproceso de trabajo UMS especificado.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Establece la información de contexto específica de la aplicación para el subproceso de trabajo UMS especificado.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Función de punto de entrada del programador UMS definida por la aplicación asociada a una lista de finalización de UMS. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Proporciona el control al subproceso del programador UMS en el que se está ejecutando el subproceso de trabajo UMS que realiza la llamada.<br/>      |



 

## <a name="new-structures"></a>Nuevas estructuras



| Estructura                                                                                                 | Descripción                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**relación de caché \_**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Describe los atributos de caché. <br/>                                                             |
| [**afinidad de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contiene una afinidad específica del grupo de procesadores, como la afinidad de un subproceso.<br/>          |
| [**relación de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contiene información acerca de los grupos de procesadores. <br/>                                            |
| [**\_relación de nodo Numa \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contiene información sobre un nodo NUMA de un grupo de procesadores. <br/>                            |
| [**\_información del grupo de procesadores \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contiene el número y la afinidad de procesadores en un grupo de procesadores.<br/>                     |
| [**número de procesador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Representa un procesador lógico de un grupo de procesadores.<br/>                                     |
| [**relación de procesador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contiene información sobre la afinidad dentro de un grupo de procesadores.<br/>                            |
| [**\_información del procesador lógico del sistema \_ \_ \_ ex**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contiene información acerca de las relaciones de los procesadores lógicos y el hardware relacionado.<br/> |
| [**\_atributos de creación de \_ SUBproceso UMS \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Especifica los atributos de un subproceso de trabajo UMS. <br/>                                           |
| [**\_información de \_ Inicio del programador UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Especifica los atributos de un subproceso del programador UMS<br/>                                          |



 

 

 
