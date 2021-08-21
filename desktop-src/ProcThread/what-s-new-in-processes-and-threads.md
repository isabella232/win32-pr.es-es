---
description: Windows 7 y Windows Server 2008 R2 incluyen los siguientes nuevos elementos de programación para procesos y subprocesos.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Novedades de procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe8b53349f5c6f19dd9beda1ffe6b933fbff63533988a40937453194df57295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792963"
---
# <a name="whats-new-in-processes-and-threads"></a>Novedades de procesos y subprocesos

Windows 7 y Windows Server 2008 R2 incluyen los siguientes nuevos elementos de programación para procesos y subprocesos.

## <a name="new-capabilities"></a>Nuevas funcionalidades

Las versiones de 64 bits de Windows 7 y Windows Server 2008 R2 admiten más de 64 procesadores lógicos en un solo equipo. Para obtener más información, vea [Grupos de procesadores](processor-groups.md).

La programación en modo de usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Para obtener más información, vea [Programación en modo de usuario.](user-mode-scheduling.md)

## <a name="new-functions"></a>Funciones nuevas

Las siguientes funciones nuevas se usan con procesadores y grupos de procesadores.



| Función                                                                                | Descripción                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Crea un subproceso que se ejecuta en el espacio de direcciones virtuales de otro proceso y, opcionalmente, especifica atributos extendidos, como la afinidad de grupo de procesadores.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Devuelve el número de procesadores activos en un grupo de procesadores o en el sistema.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Devuelve el número de grupos de procesadores activos del sistema.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Recupera el grupo de procesadores y el número del procesador lógico en el que se ejecuta el subproceso que realiza la llamada.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Recupera información sobre las relaciones de los procesadores lógicos y el hardware relacionado.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Devuelve el número máximo de procesadores lógicos que puede tener un grupo de procesadores o el sistema.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Devuelve el número máximo de grupos de procesadores que puede tener el sistema. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Recupera la cantidad de memoria disponible en el nodo especificado como un valor USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Recupera el nodo NUMA asociado al dispositivo subyacente para un identificador de archivo.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Recupera la máscara del procesador para el nodo NUMA especificado como un valor USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Recupera el número de nodo del procesador lógico especificado como un valor USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Recupera el número de nodo como un valor USHORT para el identificador de proximidad especificado.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Recupera la afinidad del grupo de procesadores del proceso especificado.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Recupera el tiempo de ciclo que cada procesador del grupo especificado dedica a ejecutar llamadas a procedimientos diferidos (DPC) e interrumpir rutinas de servicio (ISR).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Recupera la afinidad de grupo de procesadores del subproceso especificado.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Recupera el número de procesador del procesador ideal para el subproceso especificado.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Recupera el tiempo de ciclo acumulado para el subproceso inactivo en cada procesador lógico del grupo de procesadores especificado. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Establece la afinidad de grupo de procesadores para el subproceso especificado.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Establece el procesador ideal para el subproceso especificado y, opcionalmente, recupera el procesador ideal anterior.<br/>                                                  |



 

Las siguientes funciones nuevas se usan con grupos de subprocesos.



| Función                                                                              | Descripción                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Recupera los tamaños de reserva y confirmación de pila para los subprocesos del grupo de subprocesos especificado.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Especifica que la devolución de llamada se debe ejecutar en un subproceso persistente.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Especifica la prioridad de una función de devolución de llamada relativa a otros elementos de trabajo del mismo grupo de subprocesos.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Establece los tamaños de reserva y confirmación de pila para los nuevos subprocesos del grupo de subprocesos especificado. <br/>              |



 

Las siguientes funciones nuevas se usan con UMS.



| Función                                                                          | Descripción                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Crea una lista de finalización de UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Crea un contexto de subproceso UMS para representar un subproceso de trabajo UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Elimina la lista de finalización de UMS especificada. La lista debe estar vacía.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Elimina el contexto de subproceso UMS especificado. El subproceso debe terminarse.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Recupera subprocesos de trabajo UMS de la lista de finalización de UMS especificada.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Convierte el subproceso que realiza la llamada en un subproceso del programador UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Ejecuta el subproceso de trabajo UMS especificado.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Devuelve el contexto del subproceso UMS del subproceso UMS que realiza la llamada.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Devuelve el siguiente contexto de subproceso UMS en una lista de contextos de subproceso UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Recupera un identificador para el evento asociado a la lista de finalización ums especificada.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Recupera información sobre el subproceso de trabajo UMS especificado.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Establece la información de contexto específica de la aplicación para el subproceso de trabajo UMS especificado.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | La función de punto de entrada del programador UMS definida por la aplicación asociada a una lista de finalización ums. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Produce el control al subproceso del programador ums en el que se ejecuta el subproceso de trabajo ums que realiza la llamada.<br/>      |



 

## <a name="new-structures"></a>Nuevas estructuras



| Estructura                                                                                                 | Descripción                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**RELACIÓN DE \_ CACHÉ**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Describe los atributos de caché. <br/>                                                             |
| [**AFINIDAD DE \_ GRUPO**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contiene una afinidad específica del grupo de procesadores, como la afinidad de un subproceso.<br/>          |
| [**RELACIÓN \_ DE GRUPO**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contiene información sobre los grupos de procesadores. <br/>                                            |
| [**RELACIÓN DE \_ NODO \_ NUMA**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contiene información sobre un nodo NUMA en un grupo de procesadores. <br/>                            |
| [**INFORMACIÓN DEL \_ GRUPO DE \_ PROCESADORES**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contiene el número y la afinidad de los procesadores de un grupo de procesadores.<br/>                     |
| [**NÚMERO DE \_ PROCESADOR**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Representa un procesador lógico en un grupo de procesadores.<br/>                                     |
| [**RELACIÓN DEL \_ PROCESADOR**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contiene información sobre la afinidad dentro de un grupo de procesadores.<br/>                            |
| [**INFORMACIÓN \_ DEL PROCESADOR LÓGICO DEL \_ \_ \_ SISTEMA, POR EJEMPLO,**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contiene información sobre las relaciones de los procesadores lógicos y el hardware relacionado.<br/> |
| [**ATRIBUTOS DE SUBPROCESO \_ DE UMS \_ CREATE \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Especifica atributos para un subproceso de trabajo UMS. <br/>                                           |
| [**INFORMACIÓN DE INICIO \_ DEL PROGRAMADOR \_ DE UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Especifica atributos para un subproceso de programador ums<br/>                                          |



 

 

 
