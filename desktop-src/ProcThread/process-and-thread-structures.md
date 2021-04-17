---
description: En este tema se enumeran las estructuras que se usan con procesos, subprocesos, procesadores, objetos de trabajo y programación de modo de usuario (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Estructuras de procesos y subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677844"
---
# <a name="process-and-thread-structures"></a>Estructuras de procesos y subprocesos

En este tema se enumeran las estructuras que se usan con procesos, subprocesos, procesadores, objetos de trabajo y programación de modo de usuario (UMS).

## <a name="process-and-thread-structures"></a>Estructuras de procesos y subprocesos

Las siguientes estructuras se usan con procesos y subprocesos:

-   [**\_información de memoria de la aplicación \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**Estado de AR \_**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**descriptor de caché \_**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**Contadores de e/s \_**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**preferencia de orientación \_**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**datos de PEB \_ LDR \_**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**información del proceso \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**\_información de \_ agotamiento de memoria de proceso \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**\_Directiva de mitigación de procesos \_ ASLR \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**\_ \_ Directiva de firma binaria de mitigación de procesos \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**\_Directiva de protección de flujo de control de mitigación de procesos \_ \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**\_Directiva de DEP de mitigación de procesos \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**\_ \_ Directiva de código dinámico de mitigación de procesos \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**\_punto de extensión de mitigación de procesos \_ \_ \_ deshabilitar \_ Directiva**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**\_fuente de mitigación de procesos \_ \_ deshabilitar \_ Directiva**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**Directiva de carga de la \_ imagen de mitigación de procesos \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**\_Directiva de \_ \_ comprobación de identificador \_ estricto \_ de mitigación de procesos**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**\_llamada del sistema de mitigación de procesos \_ \_ \_ deshabilitar \_ Directiva**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_parámetros de \_ proceso de usuario RTL \_**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Estructuras de procesador

Las siguientes estructuras se utilizan con procesadores y grupos de procesadores:

-   [**relación de caché \_**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**afinidad de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**relación de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**\_relación de nodo Numa \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**\_información del grupo de procesadores \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**número de procesador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**relación de procesador \_**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**\_información de \_ conjunto de CPU del sistema \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**\_información del \_ procesador \_ lógico del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**\_información del procesador lógico del sistema \_ \_ \_ ex**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Estructura de cola del distribuidor

La siguiente estructura se usa para crear un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Estructuras de objetos de trabajo

Las siguientes estructuras se usan con objetos de trabajo:

-   [**JOBOBJECT \_ \_ Puerto de finalización asociado \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**\_información básica de \_ cuentas \_ de JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_ \_ información de cuentas básica y de \_ e/s de \_ JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**\_información de \_ límite \_ básico de JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**JOBOBJECT \_ \_ lista de \_ ID. de proceso básico \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**restricciones de la \_ \_ interfaz de usuario básica de JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JOBOBJECT \_ fin \_ de \_ la \_ información de tiempo de trabajo \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**JOBOBJECT \_ \_ información de límite extendido \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_información de \_ límite de seguridad de JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>User-Mode estructuras de programación

Las siguientes estructuras se usan con UMS:

-   [**\_atributos de creación de \_ SUBproceso UMS \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**\_información de \_ Inicio del programador UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**\_información del \_ subproceso del sistema UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
