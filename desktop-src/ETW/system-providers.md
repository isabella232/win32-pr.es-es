---
title: Proveedores de sistemas
description: Habilite los eventos del proveedor de seguimiento del sistema con EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: f32b31f1c1a59c3a1507a37279def248f57e66e2
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520312"
---
# <a name="system-providers"></a>Proveedores de sistemas
 
A partir Windows 10 la compilación 20348 del SDK, los eventos del proveedor de seguimiento del sistema se pueden habilitar de la misma manera que otros proveedores de ETW, con [EnableTraceEx2.](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)  Las diferentes marcas y máscaras de grupo [asociadas](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al proveedor de seguimiento del sistema se han asignado a nuevos proveedores de seguimiento, denominados proveedores de sistema, y palabras clave correspondientes.  
 
Al igual que habilitar el proveedor de seguimiento del sistema directamente, los proveedores del sistema solo pueden habilitarse mediante una [sesión con el EVENT_TRACE_SYSTEM_LOGGER_MODE](./logging-mode-constants.md) establecido.

## <a name="system-provider-reference"></a>Referencia del proveedor del sistema

* [Proveedor DE ALPC del sistema](#system-alpc-provider)
* [Proveedor de configuración del sistema](#system-config-provider)
* [Proveedor de CPU del sistema](#system-cpu-provider)
* [Proveedor de hipervisor del sistema](#system-hypervisor-provider)
* [Proveedor de interrupciones del sistema](#system-interrupt-provider)
* [Proveedor de E/S del sistema](#system-io-provider)
* [Proveedor de filtros de E/S del sistema](#system-io-filter-provider)
* [Proveedor de bloqueos del sistema](#system-lock-provider)
* [Proveedor de memoria del sistema](#system-memory-provider)
* [Proveedor de objetos del sistema](#system-object-provider)
* [Proveedor de energía del sistema](#system-power-provider)
* [Proveedor de procesos del sistema](#system-process-provider)
* [Proveedor de perfiles de sistema](#system-profile-provider)
* [Proveedor del Registro del sistema](#system-registry-provider)
* [Proveedor del programador del sistema](#system-scheduler-provider)
* [Proveedor de llamadas del sistema](#system-syscall-provider)
* [Proveedor de temporizadores del sistema](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>Proveedor DE ALPC del sistema

Proporciona eventos relacionados con el sistema ALPC.

GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC, EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>Proveedor de configuración del sistema 

Proporciona eventos de configuración del sistema.

GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>Proveedor de CPU del sistema 

Proporciona eventos relacionados con la CPU.

GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>Proveedor de hipervisor del sistema 

Proporciona eventos relacionados con el hipervisor.

GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>Proveedor de interrupciones del sistema 

Proporciona eventos relacionados con dpc e interrupciones.

GUID: SystemInterruptProviderGuid {d4providere17-b545-4888-858b-744169015b25}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC, EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>Proveedor de E/S del sistema 

Proporciona eventos relacionados con varios tipos de E/S, incluidos el disco, la caché y la red.

GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP |

Nota: Al habilitar la SYSTEM_IO_KW_DRIVERS clave , también se habilitarán SYSTEM_IO_KW_FILENAME automáticamente.  El SYSTEM_IO_KW_FILENAME también se activa automáticamente cuando el proveedor de memoria del sistema está habilitado con la palabra SYSTEM_MEMORY_KW_MEMORY clave.
 
### <a name="system-io-filter-provider"></a>Proveedor de filtros de E/S del sistema 

Proporciona eventos relacionados con el filtrado de E/S, incluido el tiempo y los errores.

GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>Proveedor de bloqueos del sistema 

Proporciona eventos relacionados con los mecanismos de bloqueo del kernel.

GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>Proveedor de memoria del sistema 

Proporciona eventos relacionados con el administrador de memoria.

GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP |

Notas: 
* Al habilitar SYSTEM_MEMORY_KW_MEMORY palabra clave, también se habilitarán SYSTEM_IO_KW_FILENAME en el proveedor de E/S del sistema.
* Los eventos habilitados por el SYSTEM_MEMORY_KW_POOL admiten un filtro de etiquetas de grupo para escribir eventos de forma selectiva solo para determinadas etiquetas de grupo.  Se configura como un filtro [esquematizado en](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) el proveedor de memoria del sistema.  El filtro PoolTag se construye de la siguiente manera:

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* El [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) debe inicializarse con id. establecido en SYSTEM_MEMORY_POOL_FILTER_ID y el campo de tamaño establecido en el tamaño de Encabezado más la parte usada de la matriz PoolTags.  

* Cada etiqueta de grupo es una cadena de 4 caracteres que se almacena como ULONG en el filtro.  
 
 
### <a name="system-object-provider"></a>Proveedor de objetos del sistema 

Proporciona eventos relacionados con el Administrador de objetos.

GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>Proveedor de energía del sistema 

Proporciona eventos relacionados con el estado de energía del sistema.

GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>Proveedor de procesos del sistema 

Proporciona eventos relacionados con el proceso, incluida la información de duración, los eventos de carga de imágenes y los eventos relacionados con subprocesos.

GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB, EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD, EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>Proveedor de perfiles del sistema 

Proporciona eventos de generación de perfiles.

GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>Proveedor del Registro del sistema 

Proporciona eventos relacionados con el registro.

GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>Proveedor del programador del sistema 

Proporciona eventos relacionados con el programador.

GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STARVATION | PERF_ANTI_STARVATION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>Proveedor de syscall del sistema 

Proporciona eventos con información sobre las llamadas del sistema.

GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>Proveedor de temporizador del sistema 

Proporciona eventos relacionados con los temporizadores del kernel.

GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}

| Palabra clave | Marcas y grupos heredados correspondientes |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>Comentarios

Este nuevo mecanismo de habilitación se suma a los métodos ya existentes para habilitar estos eventos.  Cualquier código que solía funcionar, lo seguirá haciendo.
 
Los eventos generados por el proveedor de seguimiento del sistema no cambian debido a esta nueva característica.  Esto significa que los eventos de salida no se marcan como emitidos desde los proveedores de sistema individuales.
 
Para obtener más información sobre el GUID del proveedor y las definiciones de palabras clave, [vea evntrace.h](/windows/win32/api/evntrace/).

## <a name="see-also"></a>Consulte también

[Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)

[encabezado evntrace.h](/windows/win32/api/evntrace/)
