---
description: En este tema se enumeran las estructuras que se usan con procesos, subprocesos, procesadores, objetos de trabajo y programación en modo de usuario (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Estructuras de procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5893340c72ee46eff43b16db936025fbb5463fbe0cc10e2eba1829962269d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081385"
---
# <a name="process-and-thread-structures"></a>Estructuras de procesos y subprocesos

En este tema se enumeran las estructuras que se usan con procesos, subprocesos, procesadores, objetos de trabajo y programación en modo de usuario (UMS).

## <a name="process-and-thread-structures"></a>Estructuras de procesos y subprocesos

Las estructuras siguientes se usan con procesos y subprocesos:

-   [**INFORMACIÓN DE \_ MEMORIA DE \_ LA APLICACIÓN**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**AR \_ STATE**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**DESCRIPTOR DE \_ CACHÉ**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**CONTADORES \_ DE E/S**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**PREFERENCIA DE \_ ORIENTACIÓN**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**Peb**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**PEB \_ LDR \_ DATA**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**INFORMACIÓN \_ DEL PROCESO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**INFORMACIÓN DE \_ AGOTAMIENTO DE LA MEMORIA DE \_ \_ PROCESO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**DIRECTIVA \_ \_ ASLR DE MITIGACIÓN \_ DE PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**DIRECTIVA DE \_ FIRMA \_ BINARIA DE \_ MITIGACIÓN DE \_ PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**DIRECTIVA DE \_ PROTECCIÓN DE FLUJO DE CONTROL DE \_ \_ \_ \_ MITIGACIÓN DE PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**DIRECTIVA \_ \_ DEP DE MITIGACIÓN DE \_ PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**DIRECTIVA DE \_ CÓDIGO \_ DINÁMICO DE \_ MITIGACIÓN DE \_ PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**DIRECTIVA DE \_ \_ DESHABILITACIÓN DE \_ PUNTO DE EXTENSIÓN \_ DE \_ MITIGACIÓN DE PROCESOS**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**DIRECTIVA DE \_ \_ DESHABILITACIÓN DE FUENTE \_ DE \_ MITIGACIÓN DE PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**DIRECTIVA DE \_ CARGA DE IMÁGENES DE \_ \_ MITIGACIÓN DE \_ PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**DIRECTIVA DE \_ COMPROBACIÓN DE IDENTIFICADOR ESTRICTA DE \_ \_ \_ \_ MITIGACIÓN DE PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**DIRECTIVA DE \_ \_ DESHABILITACIÓN \_ DE LLAMADA DEL SISTEMA \_ DE \_ MITIGACIÓN DE PROCESOS**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**PARÁMETROS DE PROCESO \_ DE \_ USUARIO RTL \_**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Estructuras de procesador

Las estructuras siguientes se usan con procesadores y grupos de procesadores:

-   [**RELACIÓN DE \_ CACHÉ**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**AFINIDAD DE \_ GRUPO**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**RELACIÓN \_ DE GRUPO**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**RELACIÓN DE \_ NODO \_ NUMA**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**INFORMACIÓN DEL \_ GRUPO DE \_ PROCESADORES**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**NÚMERO DE \_ PROCESADOR**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**RELACIÓN DEL \_ PROCESADOR**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**INFORMACIÓN DEL \_ CONJUNTO DE CPU DEL \_ \_ SISTEMA**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**INFORMACIÓN DEL \_ PROCESADOR \_ LÓGICO DEL \_ SISTEMA**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**INFORMACIÓN \_ DEL PROCESADOR LÓGICO DEL \_ \_ \_ SISTEMA, POR EJEMPLO,**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Estructura de cola del distribuidor

La siguiente estructura se usa para crear [un dispatcherQueueController.](/uwp/api/windows.system.dispatcherqueuecontroller)

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Estructuras de objetos de trabajo

Las estructuras siguientes se usan con objetos de trabajo:

-   [**PUERTO DE FINALIZACIÓN ASOCIADO DE JOBOBJECT \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**INFORMACIÓN DE CONTABILIDAD BÁSICA DE JOBOBJECT \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**INFORMACIÓN BÁSICA DE JOBOBJECT \_ \_ Y CONTABILIDAD DE \_ \_ \_ E/S**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**INFORMACIÓN DE LÍMITE BÁSICO DE JOBOBJECT \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**JOBOBJECT \_ BASIC \_ PROCESS \_ ID \_ LIST**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**RESTRICCIONES DE LA \_ INTERFAZ DE USUARIO BÁSICA \_ \_ DE JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**INFORMACIÓN SOBRE EL \_ FIN DEL TRABAJO DE \_ \_ \_ \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**INFORMACIÓN DE LÍMITE EXTENDIDO DE JOBOBJECT \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**INFORMACIÓN DEL \_ LÍMITE DE SEGURIDAD DE \_ \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>User-Mode de programación

Las estructuras siguientes se usan con UMS:

-   [**ATRIBUTOS DE \_ SUBPROCESO DE UMS \_ CREATE \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**INFORMACIÓN DE INICIO \_ DE UMS SCHEDULER \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**INFORMACIÓN DE \_ SUBPROCESOS \_ DEL SISTEMA \_ UMS**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
