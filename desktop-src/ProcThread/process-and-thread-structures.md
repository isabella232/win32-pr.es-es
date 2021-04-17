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
# <a name="process-and-thread-structures"></a><span data-ttu-id="64187-103">Estructuras de procesos y subprocesos</span><span class="sxs-lookup"><span data-stu-id="64187-103">Process and Thread Structures</span></span>

<span data-ttu-id="64187-104">En este tema se enumeran las estructuras que se usan con procesos, subprocesos, procesadores, objetos de trabajo y programación de modo de usuario (UMS).</span><span class="sxs-lookup"><span data-stu-id="64187-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="64187-105">Estructuras de procesos y subprocesos</span><span class="sxs-lookup"><span data-stu-id="64187-105">Process and Thread Structures</span></span>

<span data-ttu-id="64187-106">Las siguientes estructuras se usan con procesos y subprocesos:</span><span class="sxs-lookup"><span data-stu-id="64187-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="64187-107">**\_información de memoria de la aplicación \_**</span><span class="sxs-lookup"><span data-stu-id="64187-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="64187-108">**Estado de AR \_**</span><span class="sxs-lookup"><span data-stu-id="64187-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="64187-109">**descriptor de caché \_**</span><span class="sxs-lookup"><span data-stu-id="64187-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="64187-110">**Contadores de e/s \_**</span><span class="sxs-lookup"><span data-stu-id="64187-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="64187-111">**preferencia de orientación \_**</span><span class="sxs-lookup"><span data-stu-id="64187-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="64187-112">**PEB**</span><span class="sxs-lookup"><span data-stu-id="64187-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="64187-113">**datos de PEB \_ LDR \_**</span><span class="sxs-lookup"><span data-stu-id="64187-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="64187-114">**información del proceso \_**</span><span class="sxs-lookup"><span data-stu-id="64187-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="64187-115">**\_información de \_ agotamiento de memoria de proceso \_**</span><span class="sxs-lookup"><span data-stu-id="64187-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="64187-116">**\_Directiva de mitigación de procesos \_ ASLR \_**</span><span class="sxs-lookup"><span data-stu-id="64187-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="64187-117">**\_ \_ Directiva de firma binaria de mitigación de procesos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64187-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="64187-118">**\_Directiva de protección de flujo de control de mitigación de procesos \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64187-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="64187-119">**\_Directiva de DEP de mitigación de procesos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64187-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="64187-120">**\_ \_ Directiva de código dinámico de mitigación de procesos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64187-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="64187-121">**\_punto de extensión de mitigación de procesos \_ \_ \_ deshabilitar \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="64187-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="64187-122">**\_fuente de mitigación de procesos \_ \_ deshabilitar \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="64187-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="64187-123">**Directiva de carga de la \_ imagen de mitigación de procesos \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64187-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="64187-124">**\_Directiva de \_ \_ comprobación de identificador \_ estricto \_ de mitigación de procesos**</span><span class="sxs-lookup"><span data-stu-id="64187-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="64187-125">**\_llamada del sistema de mitigación de procesos \_ \_ \_ deshabilitar \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="64187-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="64187-126">**\_parámetros de \_ proceso de usuario RTL \_**</span><span class="sxs-lookup"><span data-stu-id="64187-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="64187-127">**STARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="64187-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="64187-128">**STARTUPINFOEX**</span><span class="sxs-lookup"><span data-stu-id="64187-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="64187-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="64187-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="64187-130">Estructuras de procesador</span><span class="sxs-lookup"><span data-stu-id="64187-130">Processor Structures</span></span>

<span data-ttu-id="64187-131">Las siguientes estructuras se utilizan con procesadores y grupos de procesadores:</span><span class="sxs-lookup"><span data-stu-id="64187-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="64187-132">**relación de caché \_**</span><span class="sxs-lookup"><span data-stu-id="64187-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="64187-133">**afinidad de grupo \_**</span><span class="sxs-lookup"><span data-stu-id="64187-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="64187-134">**relación de grupo \_**</span><span class="sxs-lookup"><span data-stu-id="64187-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="64187-135">**\_relación de nodo Numa \_**</span><span class="sxs-lookup"><span data-stu-id="64187-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="64187-136">**\_información del grupo de procesadores \_**</span><span class="sxs-lookup"><span data-stu-id="64187-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="64187-137">**número de procesador \_**</span><span class="sxs-lookup"><span data-stu-id="64187-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="64187-138">**relación de procesador \_**</span><span class="sxs-lookup"><span data-stu-id="64187-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="64187-139">**\_información de \_ conjunto de CPU del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="64187-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="64187-140">**\_información del \_ procesador \_ lógico del sistema**</span><span class="sxs-lookup"><span data-stu-id="64187-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="64187-141">**\_información del procesador lógico del sistema \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="64187-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="64187-142">Estructura de cola del distribuidor</span><span class="sxs-lookup"><span data-stu-id="64187-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="64187-143">La siguiente estructura se usa para crear un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span><span class="sxs-lookup"><span data-stu-id="64187-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="64187-144">**DispatcherQueueOptions**</span><span class="sxs-lookup"><span data-stu-id="64187-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="64187-145">Estructuras de objetos de trabajo</span><span class="sxs-lookup"><span data-stu-id="64187-145">Job Object Structures</span></span>

<span data-ttu-id="64187-146">Las siguientes estructuras se usan con objetos de trabajo:</span><span class="sxs-lookup"><span data-stu-id="64187-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="64187-147">**JOBOBJECT \_ \_ Puerto de finalización asociado \_**</span><span class="sxs-lookup"><span data-stu-id="64187-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="64187-148">**\_información básica de \_ cuentas \_ de JOBOBJECT**</span><span class="sxs-lookup"><span data-stu-id="64187-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="64187-149">**\_ \_ información de cuentas básica y de \_ e/s de \_ JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="64187-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="64187-150">**\_información de \_ límite \_ básico de JOBOBJECT**</span><span class="sxs-lookup"><span data-stu-id="64187-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="64187-151">**JOBOBJECT \_ \_ lista de \_ ID. de proceso básico \_**</span><span class="sxs-lookup"><span data-stu-id="64187-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="64187-152">**restricciones de la \_ \_ interfaz de usuario básica de JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="64187-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="64187-153">**JOBOBJECT \_ fin \_ de \_ la \_ información de tiempo de trabajo \_**</span><span class="sxs-lookup"><span data-stu-id="64187-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="64187-154">**JOBOBJECT \_ \_ información de límite extendido \_**</span><span class="sxs-lookup"><span data-stu-id="64187-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="64187-155">**\_información de \_ límite de seguridad de JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="64187-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="64187-156">User-Mode estructuras de programación</span><span class="sxs-lookup"><span data-stu-id="64187-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="64187-157">Las siguientes estructuras se usan con UMS:</span><span class="sxs-lookup"><span data-stu-id="64187-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="64187-158">**\_atributos de creación de \_ SUBproceso UMS \_**</span><span class="sxs-lookup"><span data-stu-id="64187-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="64187-159">**\_información de \_ Inicio del programador UMS \_**</span><span class="sxs-lookup"><span data-stu-id="64187-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="64187-160">**\_información del \_ subproceso del sistema UMS \_**</span><span class="sxs-lookup"><span data-stu-id="64187-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
