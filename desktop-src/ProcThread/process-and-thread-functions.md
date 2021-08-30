---
description: En este tema se describen las funciones de proceso y subproceso.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Funciones de proceso y subproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f187244e65008e3b4e082578af56a734d7e7571747fa7e3a565b0aa99904de66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081405"
---
# <a name="process-and-thread-functions"></a>Funciones de proceso y subproceso

En este tema se describen las funciones de proceso y subproceso.

-   [Dispatch Queue (Función)](#dispatch-queue-function)
-   [Funciones de proceso](#process-functions)
-   [Funciones de enumeración de procesos](#process-enumeration-functions)
-   [Funciones de directiva](#policy-functions)
-   [Funciones de subproceso](#thread-functions)
-   [Funciones de atributos extendidos de proceso y subproceso](#process-and-thread-extended-attribute-functions)
-   [Funciones WOW64](#wow64-functions)
-   [Funciones de objeto de trabajo](#job-object-functions)
-   [Funciones del grupo de subprocesos](#thread-pool-functions)
-   [Funciones del servicio de ordenación de subprocesos](#thread-ordering-service-functions)
-   [Funciones del servicio Programador de clases multimedia](#multimedia-class-scheduler-service-functions)
-   [Funciones de fibra](#fiber-functions)
-   [Funciones de compatibilidad de NUMA](#numa-support-functions)
-   [Funciones de procesador](#processor-functions)
-   [Funciones de programación en modo de usuario](#user-mode-scheduling-functions)
-   [Funciones obsoletas](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Dispatch Queue (Función)

La función siguiente crea un [dispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).



| Función                                                                   | Descripción                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDispatcherQueueController**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Crea un [DispatcherQueueController que](/uwp/api/windows.system.dispatcherqueuecontroller) administra la duración de [un dispatcherQueue](/uwp/api/windows.system.dispatcherqueue) que ejecuta tareas en cola en orden de prioridad en otro subproceso. |



 

## <a name="process-functions"></a>Funciones de proceso

Las funciones siguientes se usan con [procesos](child-processes.md).



| Función                                                                 | Descripción                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Crea un nuevo proceso y su subproceso principal.                                                                                                                                                 |
| [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Crea un nuevo proceso y su subproceso principal. El nuevo proceso se ejecuta en el contexto de seguridad del usuario representado por el token especificado.                                                    |
| [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Crea un nuevo proceso y su subproceso principal. A continuación, el nuevo proceso ejecuta el archivo ejecutable especificado en el contexto de seguridad de las credenciales especificadas (usuario, dominio y contraseña).      |
| [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Crea un nuevo proceso y su subproceso principal. El nuevo proceso se ejecuta en el contexto de seguridad del token especificado.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Finaliza el proceso de llamada y todos sus subprocesos.                                                                                                                                                 |
| [**FlushProcessWriteBuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Vacía la cola de escritura de cada procesador que ejecuta un subproceso del proceso actual.                                                                                                    |
| [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Libera un bloque de cadenas de entorno.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Recupera la cadena de la línea de comandos para el proceso actual.                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Recupera un pseudo identificador para el proceso actual.                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Recupera el identificador de proceso del proceso que realiza la llamada.                                                                                                                                      |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.                                                                                     |
| [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Recupera el bloque de entorno para el proceso actual.                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Recupera el valor de la variable especificada del bloque de entorno del proceso de llamada.                                                                                              |
| [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Recupera el estado de finalización del proceso especificado.                                                                                                                                    |
| [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Recupera el recuento de identificadores de los objetos de interfaz gráfica de usuario (GUI) en uso por el proceso especificado.                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Recupera información sobre procesadores lógicos y hardware relacionado.                                                                                                                          |
| [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Recupera la clase de prioridad para el proceso especificado.                                                                                                                                       |
| [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Recupera una máscara de afinidad de proceso para el proceso especificado y la máscara de afinidad del sistema para el sistema.                                                                                      |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Recupera la afinidad del grupo de procesadores del proceso especificado.                                                                                                                              |
| [**GetProcessHandleCount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Recupera el número de identificadores abiertos que pertenecen al proceso especificado.                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Recupera el identificador de proceso del proceso especificado.                                                                                                                                    |
| [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Recupera el identificador de proceso del proceso asociado al subproceso especificado.                                                                                                         |
| [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Recupera información de contabilidad de todas las operaciones de E/S realizadas por el proceso especificado.                                                                                                   |
| [**GetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Recupera la configuración de la directiva de mitigación para el proceso de llamada.                                                                                                                                 |
| [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Recupera el estado de control de aumento de prioridad del proceso especificado.                                                                                                                          |
| [**GetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Recupera los parámetros de apagado para el proceso que realiza la llamada actualmente.                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Recupera información de tiempo sobre para el proceso especificado.                                                                                                                                 |
| [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Recupera los números de versión principal y secundaria del sistema en el que el proceso especificado espera ejecutarse.                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)             | Recupera los tamaños mínimo y máximo del espacio de trabajo del proceso especificado.                                                                                                                 |
| [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Recupera los tamaños mínimo y máximo del espacio de trabajo del proceso especificado.                                                                                                                 |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Recupera el tiempo de ciclo que cada procesador del grupo especificado dedica a ejecutar llamadas a procedimientos diferidos (DPC) e interrumpir rutinas de servicio (ISR).                                         |
| [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Recupera el contenido de la estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que se especificó cuando se creó el proceso de llamada.                                                       |
| [**IsImmersiveProcess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Determina si el proceso pertenece a una aplicación Windows Store.                                                                                                                                |
| [**NeedCurrentDirectoryForExePath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Determina si el directorio actual debe incluirse en la ruta de acceso de búsqueda del ejecutable especificado.                                                                                  |
| [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Abre un objeto de proceso local existente.                                                                                                                                                       |
| [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Recupera el nombre completo de la imagen ejecutable para el proceso especificado.                                                                                                                    |
| [**QueryProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Recupera el modo de actualización de afinidad del proceso especificado.                                                                                                                                  |
| [**QueryProcessCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Recupera la suma del tiempo de ciclo de todos los subprocesos del proceso especificado.                                                                                                                  |
| [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Establece el valor de una variable de entorno para el proceso actual.                                                                                                                            |
| [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Establece la clase de prioridad para el proceso especificado.                                                                                                                                            |
| [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Establece una máscara de afinidad de procesador para los subprocesos de un proceso especificado.                                                                                                                        |
| [**SetProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Establece el modo de actualización de afinidad del proceso especificado.                                                                                                                                       |
| [**SetProcessInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Establece información para el proceso especificado.                                                                                                                                                   |
| [**SetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Establece la directiva de mitigación para el proceso de llamada.                                                                                                                                           |
| [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Deshabilita la capacidad del sistema de aumentar temporalmente la prioridad de los subprocesos del proceso especificado.                                                                                 |
| [**SetProcessRestrictionExemption**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Excluye el proceso de llamada de restricciones que impiden que los procesos de escritorio interactúen con el entorno de Windows store. Esta función la usan las herramientas de desarrollo y depuración. |
| [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Establece los parámetros de apagado para el proceso que realiza la llamada actualmente.                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)             | Establece los tamaños mínimo y máximo del espacio de trabajo para el proceso especificado.                                                                                                                     |
| [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Establece los tamaños mínimo y máximo del espacio de trabajo para el proceso especificado.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Finaliza el proceso especificado y todos sus subprocesos.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Funciones de enumeración de procesos

Las funciones siguientes se usan para enumerar los procesos.



| Función                                                    | Descripción                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera el identificador de proceso para cada objeto de proceso del sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera información sobre el primer proceso encontrado en una instantánea del sistema.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera información sobre el siguiente proceso registrado en una instantánea del sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera información sobre los procesos activos en el servidor de terminal especificado. |



 

## <a name="policy-functions"></a>Funciones de directiva

Las siguientes funciones se usan con la directiva de todo el proceso.



|  Función                                                    |  Descripción                                                     |
|------------------------------------------------------|-------------------------------------------------------|
| [**QueryProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Consulta el valor asociado a una directiva protegida. |
| [**SetProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Establece una directiva protegida.                              |



 

## <a name="thread-functions"></a>Funciones de subproceso

Las funciones siguientes se usan con [subprocesos](multiple-threads.md).



| Función                                                           | Descripción                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Asocia el mecanismo de procesamiento de entrada de un subproceso al de otro subproceso.                                                                          |
| [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Crea un subproceso que se ejecuta en el espacio de direcciones virtuales de otro proceso.                                                                               |
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Crea un subproceso que se ejecuta en el espacio de direcciones virtuales de otro proceso y, opcionalmente, especifica atributos extendidos, como la afinidad de grupo de procesadores. |
| [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Crea un subproceso que se ejecutará dentro del espacio de direcciones virtuales del proceso de llamada.                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Finaliza el subproceso que realiza la llamada.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Recupera un pseudo identificador para el subproceso actual.                                                                                                         |
| [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Recupera el identificador de subproceso del subproceso que realiza la llamada.                                                                                                    |
| [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Recupera el estado de finalización del subproceso especificado.                                                                                                 |
| [**GetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Recupera la descripción que se asignó a un subproceso mediante una llamada a [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription).                                  |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Recupera la afinidad de grupo de procesadores del subproceso especificado.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Recupera el identificador de subproceso del subproceso especificado.                                                                                                  |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Recupera el número de procesador del procesador ideal para el subproceso especificado.                                                                           |
| [**GetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Recupera información sobre el subproceso especificado.                                                                                                         |
| [**GetThreadIOPendingFlag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Determina si un subproceso especificado tiene solicitudes de E/S pendientes.                                                                                       |
| [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Recupera el valor de prioridad para el subproceso especificado.                                                                                                    |
| [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Recupera el estado de control de aumento de prioridad del subproceso especificado.                                                                                       |
| [**GetThreadTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Recupera información de tiempo para el subproceso especificado.                                                                                                    |
| [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Abre un objeto de subproceso existente.                                                                                                                          |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Recupera el tiempo de ciclo para el subproceso inactivo de cada procesador del sistema.                                                                             |
| [**QueryThreadCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Recupera el tiempo de ciclo para el subproceso especificado.                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Disminuye el recuento de suspensión de un subproceso.                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Establece una máscara de afinidad de procesador para el subproceso especificado.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Asigna una descripción a un subproceso.                                                                                                                        |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Establece la afinidad del grupo de procesadores para el subproceso especificado.                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Especifica un procesador preferido para un subproceso.                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Establece el procesador ideal para el subproceso especificado y, opcionalmente, recupera el procesador ideal anterior.                                                  |
| [**SetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Establece información para el subproceso especificado.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Establece el valor de prioridad para el subproceso especificado.                                                                                                         |
| [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Deshabilita la capacidad del sistema de aumentar temporalmente la prioridad de un subproceso.                                                                         |
| [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Establece la garantía de pila para el subproceso que realiza la llamada.                                                                                                          |
| [**Dormir**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Suspende la ejecución del subproceso actual durante un intervalo especificado.                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Suspende el subproceso actual hasta que se cumple la condición especificada.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Suspende el subproceso especificado.                                                                                                                            |
| [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Hace que el subproceso que realiza la llamada ceda la ejecución a otro subproceso que está listo para ejecutarse en el procesador actual.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Finaliza un subproceso.                                                                                                                                      |
| [**ThreadProc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Función definida por la aplicación que actúa como dirección inicial de un subproceso.                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Asigna un índice de almacenamiento local de subprocesos (TLS).                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Libera un índice TLS.                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Recupera el valor de la ranura TLS del subproceso que realiza la llamada para un índice TLS especificado.                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Almacena un valor en la ranura TLS del subproceso que realiza la llamada para un índice TLS especificado.                                                                                |
| [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Espera hasta que el proceso especificado está esperando la entrada del usuario sin ninguna entrada pendiente o hasta que haya transcurrido el intervalo de tiempo de espera.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Funciones de atributos extendidos de proceso y subproceso

Las siguientes funciones se usan para establecer atributos extendidos para la creación de procesos y subprocesos.



| Función                                                                       | Descripción                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DeleteProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Elimina la lista de atributos especificada para la creación de procesos y subprocesos.                            |
| [**InitializeProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Inicializa la lista especificada de atributos para la creación de procesos y subprocesos.                        |
| [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Actualiza el atributo especificado en la lista especificada de atributos para la creación de procesos y subprocesos. |



 

## <a name="wow64-functions"></a>Funciones WOW64

Las funciones siguientes se usan con [WOW64](../winprog64/running-32-bit-applications.md).



| Función                                         | Descripción                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Determina si el último mensaje leído de la cola del subproceso actual se originó en un proceso WOW64.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Determina si el proceso especificado se está ejecutando en WOW64.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Determina si el proceso especificado se está ejecutando en WOW64; también devuelve información adicional sobre el proceso de la máquina y la arquitectura. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Suspende el subproceso WOW64 especificado.                                                                                                   |



 

## <a name="job-object-functions"></a>Funciones de objeto de trabajo

Las funciones siguientes se usan con objetos [de trabajo](job-objects.md).



| Función                                                       | Descripción                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Asocia un proceso a un objeto de trabajo existente.                                                    |
| [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Crea o abre un objeto de trabajo.                                                                       |
| [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Determina si el proceso se está ejecutando en el trabajo especificado.                                      |
| [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Abre un objeto de trabajo existente.                                                                        |
| [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Recupera información sobre el límite y el estado del trabajo del objeto de trabajo.                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Establecer límites para un objeto de trabajo.                                                                         |
| [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Finaliza todos los procesos asociados actualmente al trabajo.                                          |
| [**UserHandleGrantAccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Concede o deniega el acceso a un identificador a un objeto User a un trabajo que tiene una restricción de interfaz de usuario. |



 

## <a name="thread-pool-functions"></a>Funciones del grupo de subprocesos

Las siguientes funciones se usan con grupos [de subprocesos](thread-pools.md).



| Función                                                                                   | Descripción                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Indica que es posible que la devolución de llamada no se devuelva rápidamente.                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Cancela la notificación de la [**función StartThreadpoolIo.**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                                                                                                                                          |
| [**CloseThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Cierra el grupo de subprocesos especificado.                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Cierra el grupo de limpieza especificado.                                                                                                                                                                                                                 |
| [**CloseThreadpoolCleanupGroupMembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Libera los miembros del grupo de limpieza especificado, espera a que se completen todas las funciones de devolución de llamada y, opcionalmente, cancela las funciones de devolución de llamada pendientes.                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Libera el objeto de finalización de E/S especificado.                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Libera el objeto de temporizador especificado.                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Libera el objeto de espera especificado.                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Libera el objeto de trabajo especificado.                                                                                                                                                                                                                 |
| [**CreateThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Asigna un nuevo grupo de subprocesos para ejecutar devoluciones de llamada.                                                                                                                                                                                               |
| [**CreateThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Crea un grupo de limpieza que las aplicaciones pueden usar para realizar un seguimiento de una o varias devoluciones de llamada del grupo de subprocesos.                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Crea un nuevo objeto de finalización de E/S.                                                                                                                                                                                                                |
| [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Crea un nuevo objeto de temporizador.                                                                                                                                                                                                                         |
| [**CreateThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Crea un nuevo objeto wait.                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Crea un nuevo objeto de trabajo.                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Elimina el entorno de devolución de llamada especificado. Llame a esta función cuando el entorno de devolución de llamada ya no sea necesario para crear nuevos objetos de grupo de subprocesos.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Quita la asociación entre la función de devolución de llamada que se está ejecutando actualmente y el objeto que inició la devolución de llamada. El subproceso actual ya no cuenta como ejecución de una devolución de llamada en nombre del objeto .                                      |
| [**FreeLibraryWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Especifica el archivo DLL que el grupo de subprocesos descargará cuando se complete la devolución de llamada actual.                                                                                                                                                             |
| [**InitializeThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Inicializa un entorno de devolución de llamada.                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Determina si el objeto de temporizador especificado está establecido actualmente.                                                                                                                                                                                     |
| [**LeaveCriticalSectionWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Especifica la sección crítica que el grupo de subprocesos liberará cuando se complete la devolución de llamada actual.                                                                                                                                               |
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Recupera los tamaños de reserva y confirmación de pila para los subprocesos del grupo de subprocesos especificado.                                                                                                                                                              |
| [**ReleaseMutexWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Especifica la exclusión mutua que liberará el grupo de subprocesos cuando se complete la devolución de llamada actual.                                                                                                                                                          |
| [**ReleaseSemaphoreWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Especifica el semáforo que el grupo de subprocesos liberará cuando se complete la devolución de llamada actual.                                                                                                                                                      |
| [**SetEventWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Especifica el evento que establecerá el grupo de subprocesos cuando se complete la devolución de llamada actual.                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Asocia el grupo de limpieza especificado al entorno de devolución de llamada especificado.                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Garantiza que el archivo DLL especificado permanece cargado siempre y cuando haya devoluciones de llamada pendientes.                                                                                                                                                           |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Especifica que la devolución de llamada se debe ejecutar en un subproceso persistente.                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Establece el grupo de subprocesos que se va a usar al generar devoluciones de llamada.                                                                                                                                                                                          |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Especifica la prioridad de una función de devolución de llamada con respecto a otros elementos de trabajo del mismo grupo de subprocesos.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Indica que es posible que las devoluciones de llamada asociadas a este entorno de devolución de llamada no se devuelvan rápidamente.                                                                                                                                                          |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Establece los tamaños de reserva y confirmación de pila para los nuevos subprocesos del grupo de subprocesos especificado.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Establece el número máximo de subprocesos que el grupo de subprocesos especificado puede asignar a las devoluciones de llamada de proceso.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Establece el número mínimo de subprocesos que el grupo de subprocesos especificado debe hacer que estén disponibles para procesar las devoluciones de llamada.                                                                                                                                         |
| [**SetThreadpoolTimerEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Establece el objeto de temporizador. Un subproceso de trabajo llama a la devolución de llamada del objeto de temporizador después de que expire el tiempo de espera especificado.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Establece el objeto de temporizador. Un subproceso de trabajo llama a la devolución de llamada del objeto de temporizador después de que expire el tiempo de espera especificado.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Establece el objeto wait. Un subproceso de trabajo llama a la función de devolución de llamada del objeto wait después de que el identificador se señale o después de que expire el tiempo de espera especificado.                                                                                           |
| [**SetThreadpoolWaitEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Establece el objeto wait. Un subproceso de trabajo llama a la función de devolución de llamada del objeto wait después de que el identificador se señale o después de que expire el tiempo de espera especificado.                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Notifica al grupo de subprocesos que es posible que las operaciones de E/S puedan comenzar para el objeto de finalización de E/S especificado. Un subproceso de trabajo llama a la función de devolución de llamada del objeto de finalización de E/S una vez completada la operación en el identificador de archivo enlazado a este objeto. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Envía un objeto de trabajo al grupo de subprocesos. Un subproceso de trabajo llama a la función de devolución de llamada del objeto de trabajo.                                                                                                                                                  |
| [**TpInitializeCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Inicializa un entorno de devolución de llamada para el grupo de subprocesos.                                                                                                                                                                                             |
| [**TpDestroyCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Elimina el entorno de devolución de llamada especificado. Llame a esta función cuando el entorno de devolución de llamada ya no sea necesario para crear nuevos objetos de grupo de subprocesos.                                                                                              |
| [**TpSetCallbackActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Asigna un contexto de activación al entorno de devolución de llamada.                                                                                                                                                                                          |
| [**TpSetCallbackCleanupGroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Asocia el grupo de limpieza especificado al entorno de devolución de llamada especificado.                                                                                                                                                                     |
| [**TpSetCallbackFinalizationCallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Indica una función a la que se va a llamar cuando se haya finalizado el entorno de devolución de llamada.                                                                                                                                                                            |
| [**TpSetCallbackLongFunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Indica que es posible que las devoluciones de llamada asociadas a este entorno de devolución de llamada no se devuelvan rápidamente.                                                                                                                                                          |
| [**TpSetCallbackNoActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Indica que el entorno de devolución de llamada no tiene ningún contexto de activación.                                                                                                                                                                                  |
| [**TpSetCallbackPersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Especifica que la devolución de llamada se debe ejecutar en un subproceso persistente.                                                                                                                                                                                      |
| [**TpSetCallbackPriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Especifica la prioridad de una función de devolución de llamada con respecto a otros elementos de trabajo del mismo grupo de subprocesos.                                                                                                                                                 |
| [**TpSetCallbackRaceWithDll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Garantiza que el archivo DLL especificado permanece cargado siempre y cuando haya devoluciones de llamada pendientes.                                                                                                                                                           |
| [**TpSetCallbackThreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Asigna un grupo de subprocesos a un entorno de devolución de llamada.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Solicita que un subproceso de trabajo del grupo de subprocesos llame a la función de devolución de llamada especificada.                                                                                                                                                                     |
| [**WaitForThreadpoolIoCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Espera a que se completen las devoluciones de llamada de finalización de E/S pendientes y, opcionalmente, cancela las devoluciones de llamada pendientes que aún no se han iniciado para ejecutarse.                                                                                                           |
| [**WaitForThreadpoolTimerCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Espera a que se completen las devoluciones de llamada de temporizador pendientes y, opcionalmente, cancela las devoluciones de llamada pendientes que aún no se han iniciado para ejecutarse.                                                                                                                    |
| [**WaitForThreadpoolWaitCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Espera a que se completen las devoluciones de llamada de espera pendientes y, opcionalmente, cancela las devoluciones de llamada pendientes que aún no se han iniciado para ejecutarse.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Espera a que se completen las devoluciones de llamada de trabajo pendientes y, opcionalmente, cancela las devoluciones de llamada pendientes que aún no se han iniciado para ejecutarse.                                                                                                                     |



 

Las siguientes funciones forman parte de la API de [agrupación de subprocesos](thread-pooling.md) original.



| Función                                                            | Descripción                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Asocia el puerto de finalización de E/S propiedad del grupo de subprocesos con el identificador de archivo especificado. Al finalizar una solicitud de E/S que implica este archivo, un subproceso de trabajo que no es de E/S ejecutará la función de devolución de llamada especificada. |
| [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Pone en cola un elemento de trabajo en un subproceso de trabajo del grupo de subprocesos.                                                                                                                                                              |
| [**RegisterWaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Dirige a un subproceso de espera del grupo de subprocesos para que espere en el objeto .                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Espera hasta que uno o todos los objetos especificados estén en el estado señalado o hasta que transcurra el intervalo de tiempo de espera.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Funciones del servicio de ordenación de subprocesos

Las funciones siguientes se usan con el servicio [de ordenación de subprocesos](thread-ordering-service.md).



| Función                                                                   | Descripción                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**AvQuerySystemResponsiveness**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Recupera la configuración de capacidad de respuesta del sistema utilizada por el servicio programador de clases multimedia. |
| [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Crea un grupo de ordenación de subprocesos.                                                            |
| [**AvRtCreateThreadOrderingGroupEx**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Crea un grupo de ordenación de subprocesos y asocia el subproceso de servidor a una tarea.               |
| [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Elimina el grupo de ordenación de subprocesos especificado creado por el autor de la llamada.                          |
| [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Une subprocesos de cliente a un grupo de ordenación de subprocesos.                                            |
| [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Permite que los subprocesos de cliente dejen un grupo de ordenación de subprocesos.                                    |
| [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Permite que los subprocesos de cliente de un grupo de ordenación de subprocesos esperen hasta que se ejecuten.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Funciones del servicio Programador de clases multimedia

Las siguientes funciones se usan con el servicio [programador de clases multimedia](multimedia-class-scheduler-service.md).



| Función                                                                   | Descripción                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**AvRevertMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Indica que un subproceso ya no realiza el trabajo asociado a la tarea especificada.              |
| [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Asocia el subproceso que realiza la llamada a las tareas especificadas.                                               |
| [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Asocia el subproceso que realiza la llamada a la tarea especificada.                                                |
| [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Ajusta la prioridad de subproceso del subproceso que realiza la llamada en relación con otros subprocesos que realizan la misma tarea. |



 

## <a name="fiber-functions"></a>Funciones de fibra

Las funciones siguientes se usan con [fibras](fibers.md).



| Función                                                 | Descripción                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ConvertFiberToThread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Convierte la fibra actual en un subproceso.                                                                    |
| [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Convierte el subproceso actual en una fibra.                                                                    |
| [**ConvertThreadToFiberEx**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Convierte el subproceso actual en una fibra.                                                                    |
| [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Asigna un objeto de fibra, le asigna una pila y configura la ejecución para comenzar en la dirección de inicio especificada. |
| [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Asigna un objeto de fibra, le asigna una pila y configura la ejecución para comenzar en la dirección de inicio especificada. |
| [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Elimina una fibra existente.                                                                                   |
| [**FiberProc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Función definida por la aplicación que se usa con [**la función CreateFiber.**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                   |
| [**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Asigna un índice de almacenamiento local de fibra (FLS).                                                                 |
| [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Libera un índice fls.                                                                                       |
| [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Recupera el valor de la ranura FLS de la fibra de llamada para un índice FLS especificado.                               |
| [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Almacena un valor en la ranura FLS de la fibra que realiza la llamada para un índice FLS especificado.                                    |
| [**IsThreadAFiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Determina si el subproceso actual es una fibra.                                                            |
| [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Programa una fibra.                                                                                           |



 

## <a name="numa-support-functions"></a>Funciones de compatibilidad de NUMA

Las funciones siguientes proporcionan compatibilidad [con NUMA.](numa-support.md)



| Función                                                                 | Descripción                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Reserva o confirma una región de memoria dentro del espacio de direcciones virtuales del proceso especificado y especifica el nodo NUMA para la memoria física. |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Recupera información sobre procesadores lógicos y hardware relacionado.                                                                                   |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Recupera la cantidad de memoria disponible en el nodo especificado.                                                                                        |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Recupera la cantidad de memoria disponible en el nodo especificado como un valor USHORT.                                                              |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Recupera el nodo que tiene actualmente el número más alto.                                                                                              |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Recupera el nodo NUMA asociado al dispositivo subyacente para un identificador de archivo.                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Recupera la máscara del procesador para el nodo especificado.                                                                                                   |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Recupera la máscara del procesador para el nodo NUMA especificado como un valor USHORT.                                                                            |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Recupera el número de nodo para el procesador especificado.                                                                                                 |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Recupera el número de nodo del procesador lógico especificado como un valor USHORT.                                                                        |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Recupera el número de nodo para el identificador de proximidad especificado.                                                                                      |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Recupera el número de nodo como un valor USHORT para el identificador de proximidad especificado.                                                                    |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Reserva o confirma una región de memoria dentro del espacio de direcciones virtuales del proceso especificado y especifica el nodo NUMA para la memoria física. |



 

## <a name="processor-functions"></a>Funciones de procesador

Las siguientes funciones se usan con procesadores lógicos y [grupos de procesadores](processor-groups.md).



| Función                                                                     | Descripción                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Devuelve el número de procesadores activos en un grupo de procesadores o en el sistema.                                       |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Devuelve el número de grupos de procesadores activos del sistema.                                                         |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.            |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Recupera el grupo de procesadores y el número del procesador lógico en el que se ejecuta el subproceso que realiza la llamada.            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Recupera información sobre procesadores lógicos y hardware relacionado.                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Recupera información sobre las relaciones de los procesadores lógicos y el hardware relacionado.                            |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Devuelve el número máximo de procesadores lógicos que puede tener un grupo de procesadores o el sistema.                      |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Devuelve el número máximo de grupos de procesadores que puede tener el sistema.                                             |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Recupera el tiempo de ciclo para el subproceso inactivo de cada procesador del sistema.                                        |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Recupera el tiempo de ciclo acumulado para el subproceso inactivo en cada procesador lógico del grupo de procesadores especificado. |



 

## <a name="user-mode-scheduling-functions"></a>User-Mode funciones de programación

Las siguientes funciones se usan con la programación en modo de usuario (UMS).



| Función                                                               | Descripción                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Crea una lista de finalización de UMS.                                                                            |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Crea un contexto de subproceso UMS para representar un subproceso de trabajo UMS.                                            |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Elimina la lista de finalización de UMS especificada. La lista debe estar vacía.                                        |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Elimina el contexto de subproceso UMS especificado. El subproceso debe terminarse.                                  |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Recupera subprocesos de trabajo UMS de la lista de finalización de UMS especificada.                                      |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Convierte el subproceso que realiza la llamada en un subproceso del programador UMS.                                                  |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Ejecuta el subproceso de trabajo UMS especificado.                                                                     |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Devuelve el contexto del subproceso UMS del subproceso UMS que realiza la llamada.                                                 |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Devuelve el siguiente contexto de subproceso UMS en una lista de contextos de subproceso UMS.                                     |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Recupera un identificador para el evento asociado a la lista de finalización ums especificada.                        |
| [**GetUmsSystemThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Consulta si el subproceso especificado es un subproceso de programador UMS, un subproceso de trabajo UMS o un subproceso que no es UMS. |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Recupera información sobre el subproceso de trabajo UMS especificado.                                              |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Establece la información de contexto específica de la aplicación para el subproceso de trabajo UMS especificado.                        |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | La función de punto de entrada del programador UMS definida por la aplicación asociada a una lista de finalización ums.         |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Produce el control al subproceso del programador ums en el que se ejecuta el subproceso de trabajo ums que realiza la llamada.             |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

-   [**NtGetCurrentProcessorNumber**](ntgetcurrentprocessornumber.md)
-   [**NtQueryInformationProcess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**NtQueryInformationThread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**WinExec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**ZwQueryInformationProcess**](zwqueryinformationprocess.md)

 

 
