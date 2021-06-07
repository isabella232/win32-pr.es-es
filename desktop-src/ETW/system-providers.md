---
title: Proveedores de sistemas
description: Habilite los eventos del proveedor de seguimiento del sistema con EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387818"
---
# <a name="system-providers"></a><span data-ttu-id="b5c40-103">Proveedores de sistemas</span><span class="sxs-lookup"><span data-stu-id="b5c40-103">System Providers</span></span>
 
<span data-ttu-id="b5c40-104">A partir Windows 10 la compilación 20348 del SDK, los eventos del proveedor de seguimiento del sistema se pueden habilitar de la misma manera que otros proveedores de ETW, con [EnableTraceEx2.](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)</span><span class="sxs-lookup"><span data-stu-id="b5c40-104">Beginning in Windows 10 SDK build 20348, the System Trace Provider's events can be enabled in the same way that other ETW providers are, with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).</span></span>  <span data-ttu-id="b5c40-105">Las diferentes marcas y máscaras de grupo [asociadas](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al proveedor de seguimiento del sistema se han asignado a nuevos proveedores de seguimiento, denominados proveedores de sistema, y palabras clave correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b5c40-105">The different flags and [group masks](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associated with the System Trace Provider have been mapped to new trace providers, called System Providers, and matching keywords.</span></span>  
 
<span data-ttu-id="b5c40-106">Al igual que habilitar el proveedor de seguimiento del sistema directamente, los proveedores del sistema solo pueden habilitarse mediante una sesión con [el EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) establecido.</span><span class="sxs-lookup"><span data-stu-id="b5c40-106">Like enabling the System Trace Provider directly, the System Providers can only be enabled by a session with the [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) set.</span></span>

## <a name="system-provider-reference"></a><span data-ttu-id="b5c40-107">Referencia del proveedor del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-107">System Provider reference</span></span>

* [<span data-ttu-id="b5c40-108">Proveedor DE ALPC del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-108">System ALPC Provider</span></span>](#system-alpc-provider)
* [<span data-ttu-id="b5c40-109">Proveedor de configuración del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-109">System Config Provider</span></span>](#system-config-provider)
* [<span data-ttu-id="b5c40-110">Proveedor de CPU del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-110">System CPU Provider</span></span>](#system-cpu-provider)
* [<span data-ttu-id="b5c40-111">Proveedor de hipervisor del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-111">System Hypervisor Provider</span></span>](#system-hypervisor-provider)
* [<span data-ttu-id="b5c40-112">Proveedor de interrupciones del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-112">System Interrupt Provider</span></span>](#system-interrupt-provider)
* [<span data-ttu-id="b5c40-113">Proveedor de E/S del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-113">System IO Provider</span></span>](#system-io-provider)
* [<span data-ttu-id="b5c40-114">Proveedor de filtros de E/S del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-114">System IO Filter Provider</span></span>](#system-io-filter-provider)
* [<span data-ttu-id="b5c40-115">Proveedor de bloqueos del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-115">System Lock Provider</span></span>](#system-lock-provider)
* [<span data-ttu-id="b5c40-116">Proveedor de memoria del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-116">System Memory Provider</span></span>](#system-memory-provider)
* [<span data-ttu-id="b5c40-117">Proveedor de objetos del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-117">System Object Provider</span></span>](#system-object-provider)
* [<span data-ttu-id="b5c40-118">Proveedor de energía del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-118">System Power Provider</span></span>](#system-power-provider)
* [<span data-ttu-id="b5c40-119">Proveedor de procesos del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-119">System Process Provider</span></span>](#system-process-provider)
* [<span data-ttu-id="b5c40-120">Proveedor de perfiles de sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-120">System Profile Provider</span></span>](#system-profile-provider)
* [<span data-ttu-id="b5c40-121">Proveedor del Registro del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-121">System Registry Provider</span></span>](#system-registry-provider)
* [<span data-ttu-id="b5c40-122">Proveedor del programador del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-122">System Scheduler Provider</span></span>](#system-scheduler-provider)
* [<span data-ttu-id="b5c40-123">Proveedor de llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-123">System Syscall Provider</span></span>](#system-syscall-provider)
* [<span data-ttu-id="b5c40-124">Proveedor de temporizadores del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-124">System Timer Provider</span></span>](#system-timer-provider)
 
### <a name="system-alpc-provider"></a><span data-ttu-id="b5c40-125">Proveedor DE ALPC del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-125">System ALPC Provider</span></span>

<span data-ttu-id="b5c40-126">Proporciona eventos relacionados con el sistema ALPC.</span><span class="sxs-lookup"><span data-stu-id="b5c40-126">Provides events related to the ALPC system.</span></span>

<span data-ttu-id="b5c40-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span><span class="sxs-lookup"><span data-stu-id="b5c40-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span></span>

| <span data-ttu-id="b5c40-128">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-128">Keyword</span></span> | <span data-ttu-id="b5c40-129">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-129">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-130">SYSTEM_ALPC_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-130">SYSTEM_ALPC_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span><span class="sxs-lookup"><span data-stu-id="b5c40-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span></span> |
 
### <a name="system-config-provider"></a><span data-ttu-id="b5c40-132">Proveedor de configuración del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-132">System Config Provider</span></span> 

<span data-ttu-id="b5c40-133">Proporciona eventos de configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5c40-133">Provides system configuration events.</span></span>

<span data-ttu-id="b5c40-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span><span class="sxs-lookup"><span data-stu-id="b5c40-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span></span>

| <span data-ttu-id="b5c40-135">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-135">Keyword</span></span> | <span data-ttu-id="b5c40-136">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-136">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-137">SYSTEM_CONFIG_KW_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="b5c40-137">SYSTEM_CONFIG_KW_SYSTEM</span></span> | <span data-ttu-id="b5c40-138">PERF_SYSCFG_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="b5c40-138">PERF_SYSCFG_SYSTEM</span></span> |
| <span data-ttu-id="b5c40-139">SYSTEM_CONFIG_KW_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="b5c40-139">SYSTEM_CONFIG_KW_GRAPHICS</span></span> | <span data-ttu-id="b5c40-140">PERF_SYSCFG_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="b5c40-140">PERF_SYSCFG_GRAPHICS</span></span> |
| <span data-ttu-id="b5c40-141">SYSTEM_CONFIG_KW_STORAGE</span><span class="sxs-lookup"><span data-stu-id="b5c40-141">SYSTEM_CONFIG_KW_STORAGE</span></span> | <span data-ttu-id="b5c40-142">PERF_SYSCFG_STORAGE</span><span class="sxs-lookup"><span data-stu-id="b5c40-142">PERF_SYSCFG_STORAGE</span></span> |
| <span data-ttu-id="b5c40-143">SYSTEM_CONFIG_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="b5c40-143">SYSTEM_CONFIG_KW_NETWORK</span></span> | <span data-ttu-id="b5c40-144">PERF_SYSCFG_NETWORK</span><span class="sxs-lookup"><span data-stu-id="b5c40-144">PERF_SYSCFG_NETWORK</span></span> |
| <span data-ttu-id="b5c40-145">SYSTEM_CONFIG_KW_SERVICES</span><span class="sxs-lookup"><span data-stu-id="b5c40-145">SYSTEM_CONFIG_KW_SERVICES</span></span> | <span data-ttu-id="b5c40-146">PERF_SYSCFG_SERVICES</span><span class="sxs-lookup"><span data-stu-id="b5c40-146">PERF_SYSCFG_SERVICES</span></span> |
| <span data-ttu-id="b5c40-147">SYSTEM_CONFIG_KW_PNP</span><span class="sxs-lookup"><span data-stu-id="b5c40-147">SYSTEM_CONFIG_KW_PNP</span></span> | <span data-ttu-id="b5c40-148">PERF_SYSCFG_PNP</span><span class="sxs-lookup"><span data-stu-id="b5c40-148">PERF_SYSCFG_PNP</span></span> |
| <span data-ttu-id="b5c40-149">SYSTEM_CONFIG_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-149">SYSTEM_CONFIG_KW_OPTICAL</span></span> | <span data-ttu-id="b5c40-150">PERF_SYSCFG_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-150">PERF_SYSCFG_OPTICAL</span></span> |
 
### <a name="system-cpu-provider"></a><span data-ttu-id="b5c40-151">Proveedor de CPU del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-151">System CPU Provider</span></span> 

<span data-ttu-id="b5c40-152">Proporciona eventos relacionados con la CPU.</span><span class="sxs-lookup"><span data-stu-id="b5c40-152">Provides events related to the CPU.</span></span>

<span data-ttu-id="b5c40-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span><span class="sxs-lookup"><span data-stu-id="b5c40-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span></span>

| <span data-ttu-id="b5c40-154">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-154">Keyword</span></span> | <span data-ttu-id="b5c40-155">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-155">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-156">SYSTEM_CPU_KW_CONFIG</span><span class="sxs-lookup"><span data-stu-id="b5c40-156">SYSTEM_CPU_KW_CONFIG</span></span> | <span data-ttu-id="b5c40-157">PERF_CPU_CONFIG</span><span class="sxs-lookup"><span data-stu-id="b5c40-157">PERF_CPU_CONFIG</span></span> |
| <span data-ttu-id="b5c40-158">SYSTEM_CPU_KW_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="b5c40-158">SYSTEM_CPU_KW_CACHE_FLUSH</span></span> | <span data-ttu-id="b5c40-159">PERF_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="b5c40-159">PERF_CACHE_FLUSH</span></span> |
| <span data-ttu-id="b5c40-160">SYSTEM_CPU_KW_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b5c40-160">SYSTEM_CPU_KW_SPEC_CONTROL</span></span> | <span data-ttu-id="b5c40-161">PERF_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b5c40-161">PERF_SPEC_CONTROL</span></span> |
 
### <a name="system-hypervisor-provider"></a><span data-ttu-id="b5c40-162">Proveedor de hipervisor del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-162">System Hypervisor Provider</span></span> 

<span data-ttu-id="b5c40-163">Proporciona eventos relacionados con el hipervisor.</span><span class="sxs-lookup"><span data-stu-id="b5c40-163">Provides events relating to the hypervisor.</span></span>

<span data-ttu-id="b5c40-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span><span class="sxs-lookup"><span data-stu-id="b5c40-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span></span>

| <span data-ttu-id="b5c40-165">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-165">Keyword</span></span> | <span data-ttu-id="b5c40-166">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-166">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-167">SYSTEM_HYPERVISOR_KW_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b5c40-167">SYSTEM_HYPERVISOR_KW_PROFILE</span></span> | <span data-ttu-id="b5c40-168">PERF_HV_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b5c40-168">PERF_HV_PROFILE</span></span> |
| <span data-ttu-id="b5c40-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span></span> | <span data-ttu-id="b5c40-170">PERF_HV_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-170">PERF_HV_CALLOUTS</span></span> |
| <span data-ttu-id="b5c40-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b5c40-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span></span> | <span data-ttu-id="b5c40-172">PERF_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b5c40-172">PERF_VTL_CHANGE</span></span> |
 
### <a name="system-interrupt-provider"></a><span data-ttu-id="b5c40-173">Proveedor de interrupciones del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-173">System Interrupt Provider</span></span> 

<span data-ttu-id="b5c40-174">Proporciona eventos relacionados con dpc e interrupciones.</span><span class="sxs-lookup"><span data-stu-id="b5c40-174">Provides events relating to DPCs and interrupts.</span></span>

<span data-ttu-id="b5c40-175">GUID: SystemInterruptProviderGuid {d4providere17-b545-4888-858b-744169015b25}</span><span class="sxs-lookup"><span data-stu-id="b5c40-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span></span>

| <span data-ttu-id="b5c40-176">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-176">Keyword</span></span> | <span data-ttu-id="b5c40-177">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-177">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-178">SYSTEM_INTERRUPT_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-178">SYSTEM_INTERRUPT_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="b5c40-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span></span> |
| <span data-ttu-id="b5c40-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="b5c40-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span></span> | <span data-ttu-id="b5c40-181">PERF_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="b5c40-181">PERF_CLOCK_INTERRUPT</span></span> |
| <span data-ttu-id="b5c40-182">SYSTEM_INTERRUPT_KW_DPC</span><span class="sxs-lookup"><span data-stu-id="b5c40-182">SYSTEM_INTERRUPT_KW_DPC</span></span> | <span data-ttu-id="b5c40-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span><span class="sxs-lookup"><span data-stu-id="b5c40-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span></span> |
| <span data-ttu-id="b5c40-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="b5c40-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span></span> | <span data-ttu-id="b5c40-185">PERF_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="b5c40-185">PERF_DPC_QUEUE</span></span> |
| <span data-ttu-id="b5c40-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="b5c40-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span></span> | <span data-ttu-id="b5c40-187">PERF_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="b5c40-187">PERF_WDF_DPC</span></span> |
| <span data-ttu-id="b5c40-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="b5c40-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span></span> | <span data-ttu-id="b5c40-189">PERF_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="b5c40-189">PERF_WDF_INTERRUPT</span></span> |
| <span data-ttu-id="b5c40-190">SYSTEM_INTERRUPT_KW_IPI</span><span class="sxs-lookup"><span data-stu-id="b5c40-190">SYSTEM_INTERRUPT_KW_IPI</span></span> | <span data-ttu-id="b5c40-191">PERF_IPI</span><span class="sxs-lookup"><span data-stu-id="b5c40-191">PERF_IPI</span></span> |
 
 
### <a name="system-io-provider"></a><span data-ttu-id="b5c40-192">Proveedor de E/S del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-192">System IO Provider</span></span> 

<span data-ttu-id="b5c40-193">Proporciona eventos relacionados con varios tipos de E/S, incluidos el disco, la caché y la red.</span><span class="sxs-lookup"><span data-stu-id="b5c40-193">Provides events relating to multiple kinds of IO including disk, cache, and network.</span></span>

<span data-ttu-id="b5c40-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span><span class="sxs-lookup"><span data-stu-id="b5c40-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span></span>

| <span data-ttu-id="b5c40-195">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-195">Keyword</span></span> | <span data-ttu-id="b5c40-196">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-196">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-197">SYSTEM_IO_KW_DISK</span><span class="sxs-lookup"><span data-stu-id="b5c40-197">SYSTEM_IO_KW_DISK</span></span> | <span data-ttu-id="b5c40-198">EVENT_TRACE_FLAG_DISK_IO</span><span class="sxs-lookup"><span data-stu-id="b5c40-198">EVENT_TRACE_FLAG_DISK_IO</span></span> |
| <span data-ttu-id="b5c40-199">SYSTEM_IO_KW_DISK_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-199">SYSTEM_IO_KW_DISK_INIT</span></span> | <span data-ttu-id="b5c40-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span></span> |
| <span data-ttu-id="b5c40-201">SYSTEM_IO_KW_FILENAME</span><span class="sxs-lookup"><span data-stu-id="b5c40-201">SYSTEM_IO_KW_FILENAME</span></span> | <span data-ttu-id="b5c40-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="b5c40-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span></span> |
| <span data-ttu-id="b5c40-203">SYSTEM_IO_KW_SPLIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-203">SYSTEM_IO_KW_SPLIT</span></span> | <span data-ttu-id="b5c40-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span><span class="sxs-lookup"><span data-stu-id="b5c40-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span></span> |
| <span data-ttu-id="b5c40-205">SYSTEM_IO_KW_FILE</span><span class="sxs-lookup"><span data-stu-id="b5c40-205">SYSTEM_IO_KW_FILE</span></span> | <span data-ttu-id="b5c40-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="b5c40-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span></span> |
| <span data-ttu-id="b5c40-207">SYSTEM_IO_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-207">SYSTEM_IO_KW_OPTICAL</span></span> | <span data-ttu-id="b5c40-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span></span> |
| <span data-ttu-id="b5c40-209">SYSTEM_IO_KW_OPTICAL_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-209">SYSTEM_IO_KW_OPTICAL_INIT</span></span> | <span data-ttu-id="b5c40-210">PERF_OPTICAL_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-210">PERF_OPTICAL_IO_INIT</span></span> |
| <span data-ttu-id="b5c40-211">SYSTEM_IO_KW_DRIVERS</span><span class="sxs-lookup"><span data-stu-id="b5c40-211">SYSTEM_IO_KW_DRIVERS</span></span> | <span data-ttu-id="b5c40-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span><span class="sxs-lookup"><span data-stu-id="b5c40-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span></span> |
| <span data-ttu-id="b5c40-213">SYSTEM_IO_KW_CC</span><span class="sxs-lookup"><span data-stu-id="b5c40-213">SYSTEM_IO_KW_CC</span></span> | <span data-ttu-id="b5c40-214">PERF_CC</span><span class="sxs-lookup"><span data-stu-id="b5c40-214">PERF_CC</span></span> |
| <span data-ttu-id="b5c40-215">SYSTEM_IO_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="b5c40-215">SYSTEM_IO_KW_NETWORK</span></span> | <span data-ttu-id="b5c40-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span><span class="sxs-lookup"><span data-stu-id="b5c40-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span></span> |

<span data-ttu-id="b5c40-217">Nota: Al habilitar la SYSTEM_IO_KW_DRIVERS clave , también se SYSTEM_IO_KW_FILENAME automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b5c40-217">Note: Enabling the SYSTEM_IO_KW_DRIVERS keyword will automatically enable SYSTEM_IO_KW_FILENAME as well.</span></span>  <span data-ttu-id="b5c40-218">El SYSTEM_IO_KW_FILENAME también se activa automáticamente cuando el proveedor de memoria del sistema está habilitado con la palabra SYSTEM_MEMORY_KW_MEMORY clave.</span><span class="sxs-lookup"><span data-stu-id="b5c40-218">The SYSTEM_IO_KW_FILENAME is also automatically turned on when the System Memory Provider is enabled with the SYSTEM_MEMORY_KW_MEMORY keyword.</span></span>
 
### <a name="system-io-filter-provider"></a><span data-ttu-id="b5c40-219">Proveedor de filtros de E/S del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-219">System IO Filter Provider</span></span> 

<span data-ttu-id="b5c40-220">Proporciona eventos relacionados con el filtrado de E/S, incluido el tiempo y los errores.</span><span class="sxs-lookup"><span data-stu-id="b5c40-220">Provides events related to IO filtering including timing and failures.</span></span>

<span data-ttu-id="b5c40-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span><span class="sxs-lookup"><span data-stu-id="b5c40-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span></span>

| <span data-ttu-id="b5c40-222">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-222">Keyword</span></span> | <span data-ttu-id="b5c40-223">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-223">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-224">SYSTEM_IOFILTER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-224">SYSTEM_IOFILTER_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-225">PERF_FLT_IO</span><span class="sxs-lookup"><span data-stu-id="b5c40-225">PERF_FLT_IO</span></span> |
| <span data-ttu-id="b5c40-226">SYSTEM_IOFILTER_KW_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-226">SYSTEM_IOFILTER_KW_INIT</span></span> | <span data-ttu-id="b5c40-227">PERF_FLT_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="b5c40-227">PERF_FLT_IO_INIT</span></span> |
| <span data-ttu-id="b5c40-228">SYSTEM_IOFILTER_KW_FASTIO</span><span class="sxs-lookup"><span data-stu-id="b5c40-228">SYSTEM_IOFILTER_KW_FASTIO</span></span> | <span data-ttu-id="b5c40-229">PERF_FLT_FASTIO</span><span class="sxs-lookup"><span data-stu-id="b5c40-229">PERF_FLT_FASTIO</span></span> |
| <span data-ttu-id="b5c40-230">SYSTEM_IOFILTER_KW_FAILURE</span><span class="sxs-lookup"><span data-stu-id="b5c40-230">SYSTEM_IOFILTER_KW_FAILURE</span></span> | <span data-ttu-id="b5c40-231">PERF_FLT_IO_FAILURE</span><span class="sxs-lookup"><span data-stu-id="b5c40-231">PERF_FLT_IO_FAILURE</span></span> |
 
### <a name="system-lock-provider"></a><span data-ttu-id="b5c40-232">Proveedor de bloqueos del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-232">System Lock Provider</span></span> 

<span data-ttu-id="b5c40-233">Proporciona eventos relacionados con los mecanismos de bloqueo del kernel.</span><span class="sxs-lookup"><span data-stu-id="b5c40-233">Provides events relating to kernel locking mechanisms.</span></span>

<span data-ttu-id="b5c40-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span><span class="sxs-lookup"><span data-stu-id="b5c40-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span></span>

| <span data-ttu-id="b5c40-235">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-235">Keyword</span></span> | <span data-ttu-id="b5c40-236">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-236">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-237">SYSTEM_LOCK_KW_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="b5c40-237">SYSTEM_LOCK_KW_SPINLOCK</span></span> | <span data-ttu-id="b5c40-238">PERF_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="b5c40-238">PERF_SPINLOCK</span></span> |
| <span data-ttu-id="b5c40-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="b5c40-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span></span> | <span data-ttu-id="b5c40-240">PERF_SPINLOCK_CNTRS</span><span class="sxs-lookup"><span data-stu-id="b5c40-240">PERF_SPINLOCK_CNTRS</span></span> |
| <span data-ttu-id="b5c40-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span></span> | <span data-ttu-id="b5c40-242">PERF_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-242">PERF_SYNC_OBJECTS</span></span> |
 
### <a name="system-memory-provider"></a><span data-ttu-id="b5c40-243">Proveedor de memoria del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-243">System Memory Provider</span></span> 

<span data-ttu-id="b5c40-244">Proporciona eventos relacionados con el administrador de memoria.</span><span class="sxs-lookup"><span data-stu-id="b5c40-244">Provides events relating to the memory manager.</span></span>

<span data-ttu-id="b5c40-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span><span class="sxs-lookup"><span data-stu-id="b5c40-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span></span>

| <span data-ttu-id="b5c40-246">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-246">Keyword</span></span> | <span data-ttu-id="b5c40-247">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-247">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-248">SYSTEM_MEMORY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-248">SYSTEM_MEMORY_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-249">PERF_MEMORY</span><span class="sxs-lookup"><span data-stu-id="b5c40-249">PERF_MEMORY</span></span> |
| <span data-ttu-id="b5c40-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span></span> | <span data-ttu-id="b5c40-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span></span> |
| <span data-ttu-id="b5c40-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span></span> | <span data-ttu-id="b5c40-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span></span> |
| <span data-ttu-id="b5c40-254">SYSTEM_MEMORY_KW_POOL</span><span class="sxs-lookup"><span data-stu-id="b5c40-254">SYSTEM_MEMORY_KW_POOL</span></span> | <span data-ttu-id="b5c40-255">PERF_POOL</span><span class="sxs-lookup"><span data-stu-id="b5c40-255">PERF_POOL</span></span> |
| <span data-ttu-id="b5c40-256">SYSTEM_MEMORY_KW_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="b5c40-256">SYSTEM_MEMORY_KW_MEMINFO</span></span> | <span data-ttu-id="b5c40-257">PERF_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="b5c40-257">PERF_MEMINFO</span></span> |
| <span data-ttu-id="b5c40-258">SYSTEM_MEMORY_KW_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="b5c40-258">SYSTEM_MEMORY_KW_PFSECTION</span></span> | <span data-ttu-id="b5c40-259">PERF_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="b5c40-259">PERF_PFSECTION</span></span> |
| <span data-ttu-id="b5c40-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="b5c40-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span></span> | <span data-ttu-id="b5c40-261">PERF_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="b5c40-261">PERF_MEMINFO_WS</span></span> |
| <span data-ttu-id="b5c40-262">SYSTEM_MEMORY_KW_HEAP</span><span class="sxs-lookup"><span data-stu-id="b5c40-262">SYSTEM_MEMORY_KW_HEAP</span></span> | <span data-ttu-id="b5c40-263">PERF_HEAP</span><span class="sxs-lookup"><span data-stu-id="b5c40-263">PERF_HEAP</span></span> |
| <span data-ttu-id="b5c40-264">SYSTEM_MEMORY_KW_WS</span><span class="sxs-lookup"><span data-stu-id="b5c40-264">SYSTEM_MEMORY_KW_WS</span></span> | <span data-ttu-id="b5c40-265">PERF_WS</span><span class="sxs-lookup"><span data-stu-id="b5c40-265">PERF_WS</span></span> |
| <span data-ttu-id="b5c40-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="b5c40-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span></span> | <span data-ttu-id="b5c40-267">PERF_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="b5c40-267">PERF_CONTMEM_GEN</span></span> |
| <span data-ttu-id="b5c40-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="b5c40-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span></span> | <span data-ttu-id="b5c40-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="b5c40-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span></span> |
| <span data-ttu-id="b5c40-270">SYSTEM_MEMORY_KW_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="b5c40-270">SYSTEM_MEMORY_KW_FOOTPRINT</span></span> | <span data-ttu-id="b5c40-271">PERF_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="b5c40-271">PERF_FOOTPRINT</span></span> |
| <span data-ttu-id="b5c40-272">SYSTEM_MEMORY_KW_SESSION</span><span class="sxs-lookup"><span data-stu-id="b5c40-272">SYSTEM_MEMORY_KW_SESSION</span></span> | <span data-ttu-id="b5c40-273">PERF_SESSION</span><span class="sxs-lookup"><span data-stu-id="b5c40-273">PERF_SESSION</span></span> |
| <span data-ttu-id="b5c40-274">SYSTEM_MEMORY_KW_REFSET</span><span class="sxs-lookup"><span data-stu-id="b5c40-274">SYSTEM_MEMORY_KW_REFSET</span></span> | <span data-ttu-id="b5c40-275">PERF_REFSET</span><span class="sxs-lookup"><span data-stu-id="b5c40-275">PERF_REFSET</span></span> |
| <span data-ttu-id="b5c40-276">SYSTEM_MEMORY_KW_VAMAP</span><span class="sxs-lookup"><span data-stu-id="b5c40-276">SYSTEM_MEMORY_KW_VAMAP</span></span> | <span data-ttu-id="b5c40-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span><span class="sxs-lookup"><span data-stu-id="b5c40-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span></span> |

<span data-ttu-id="b5c40-278">Notas:</span><span class="sxs-lookup"><span data-stu-id="b5c40-278">Notes:</span></span> 
* <span data-ttu-id="b5c40-279">Al habilitar SYSTEM_MEMORY_KW_MEMORY palabra clave, también se habilitarán SYSTEM_IO_KW_FILENAME en el proveedor de E/S del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5c40-279">Enabling the SYSTEM_MEMORY_KW_MEMORY keyword will automatically enable SYSTEM_IO_KW_FILENAME on the System IO Provider as well.</span></span>
* <span data-ttu-id="b5c40-280">Los eventos habilitados por el SYSTEM_MEMORY_KW_POOL admiten un filtro de etiquetas de grupo para escribir eventos de forma selectiva solo para determinadas etiquetas de grupo.</span><span class="sxs-lookup"><span data-stu-id="b5c40-280">The events enabled by the SYSTEM_MEMORY_KW_POOL support a Pool Tag Filter, to selectively write events only for certain pool tags.</span></span>  <span data-ttu-id="b5c40-281">Se configura como un filtro [esquematizado en](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) el proveedor de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5c40-281">This is configured as a [Schematized Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) on the System Memory Provider.</span></span>  <span data-ttu-id="b5c40-282">El filtro PoolTag se construye de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b5c40-282">The PoolTag filter is constructed as follows:</span></span>

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* <span data-ttu-id="b5c40-283">El [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) debe inicializarse con id. establecido en SYSTEM_MEMORY_POOL_FILTER_ID y el campo de tamaño establecido en el tamaño de Header más la parte usada de la matriz PoolTags.</span><span class="sxs-lookup"><span data-stu-id="b5c40-283">The [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) should be initialized with Id set to SYSTEM_MEMORY_POOL_FILTER_ID and the size field set to the size of Header plus the used portion of the PoolTags array.</span></span>  

* <span data-ttu-id="b5c40-284">Cada etiqueta de grupo es una cadena de 4 caracteres que se almacena como ULONG en el filtro.</span><span class="sxs-lookup"><span data-stu-id="b5c40-284">Each Pool Tag is a 4 character string that is stored as a ULONG in the filter.</span></span>  
 
 
### <a name="system-object-provider"></a><span data-ttu-id="b5c40-285">Proveedor de objetos del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-285">System Object Provider</span></span> 

<span data-ttu-id="b5c40-286">Proporciona eventos relacionados con el Administrador de objetos.</span><span class="sxs-lookup"><span data-stu-id="b5c40-286">Provides events relating to the Object Manager.</span></span>

<span data-ttu-id="b5c40-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span><span class="sxs-lookup"><span data-stu-id="b5c40-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span></span>

| <span data-ttu-id="b5c40-288">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-288">Keyword</span></span> | <span data-ttu-id="b5c40-289">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-289">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-290">SYSTEM_OBJECT_KW_HANDLE</span><span class="sxs-lookup"><span data-stu-id="b5c40-290">SYSTEM_OBJECT_KW_HANDLE</span></span> | <span data-ttu-id="b5c40-291">PERF_OB_HANDLE</span><span class="sxs-lookup"><span data-stu-id="b5c40-291">PERF_OB_HANDLE</span></span> |
| <span data-ttu-id="b5c40-292">SYSTEM_OBJECT_KW_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b5c40-292">SYSTEM_OBJECT_KW_OBJECT</span></span> | <span data-ttu-id="b5c40-293">PERF_OB_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b5c40-293">PERF_OB_OBJECT</span></span> |
 
### <a name="system-power-provider"></a><span data-ttu-id="b5c40-294">Proveedor de energía del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-294">System Power Provider</span></span> 

<span data-ttu-id="b5c40-295">Proporciona eventos relacionados con el estado de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5c40-295">Provides events relating to the system's power state.</span></span>

<span data-ttu-id="b5c40-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span><span class="sxs-lookup"><span data-stu-id="b5c40-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span></span>

| <span data-ttu-id="b5c40-297">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-297">Keyword</span></span> | <span data-ttu-id="b5c40-298">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-298">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-299">SYSTEM_POWER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-299">SYSTEM_POWER_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-300">PERF_POWER</span><span class="sxs-lookup"><span data-stu-id="b5c40-300">PERF_POWER</span></span> |
| <span data-ttu-id="b5c40-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="b5c40-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span></span> | <span data-ttu-id="b5c40-302">PERF_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="b5c40-302">PERF_HIBER_RUNDOWN</span></span> |
| <span data-ttu-id="b5c40-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="b5c40-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span></span> | <span data-ttu-id="b5c40-304">PERF_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="b5c40-304">PERF_PROCESSOR_IDLE</span></span> |
| <span data-ttu-id="b5c40-305">SYSTEM_POWER_KW_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="b5c40-305">SYSTEM_POWER_KW_IDLE_SELECTION</span></span> | <span data-ttu-id="b5c40-306">PERF_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="b5c40-306">PERF_IDLE_SELECTION</span></span> |
| <span data-ttu-id="b5c40-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="b5c40-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span></span> | <span data-ttu-id="b5c40-308">PERF_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="b5c40-308">PERF_PPM_EXIT_LATENCY</span></span> |
 
### <a name="system-process-provider"></a><span data-ttu-id="b5c40-309">Proveedor de procesos del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-309">System Process Provider</span></span> 

<span data-ttu-id="b5c40-310">Proporciona eventos relacionados con el proceso, incluida la información de duración, los eventos de carga de imágenes y los eventos relacionados con subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b5c40-310">Provides events relating to the process, including lifetime information, image load events, and thread related events.</span></span>

<span data-ttu-id="b5c40-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span><span class="sxs-lookup"><span data-stu-id="b5c40-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span></span>

| <span data-ttu-id="b5c40-312">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-312">Keyword</span></span> | <span data-ttu-id="b5c40-313">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-313">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-314">SYSTEM_PROCESS_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-314">SYSTEM_PROCESS_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span><span class="sxs-lookup"><span data-stu-id="b5c40-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span></span> |
| <span data-ttu-id="b5c40-316">SYSTEM_PROCESS_KW_INSWAP</span><span class="sxs-lookup"><span data-stu-id="b5c40-316">SYSTEM_PROCESS_KW_INSWAP</span></span> | <span data-ttu-id="b5c40-317">PERF_PROCESS_INSWAP</span><span class="sxs-lookup"><span data-stu-id="b5c40-317">PERF_PROCESS_INSWAP</span></span> |
| <span data-ttu-id="b5c40-318">SYSTEM_PROCESS_KW_FREEZE</span><span class="sxs-lookup"><span data-stu-id="b5c40-318">SYSTEM_PROCESS_KW_FREEZE</span></span> | <span data-ttu-id="b5c40-319">PERF_PROCESS_FREEZE</span><span class="sxs-lookup"><span data-stu-id="b5c40-319">PERF_PROCESS_FREEZE</span></span> |
| <span data-ttu-id="b5c40-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span><span class="sxs-lookup"><span data-stu-id="b5c40-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span></span> | <span data-ttu-id="b5c40-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="b5c40-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span></span> |
| <span data-ttu-id="b5c40-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="b5c40-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span></span> | <span data-ttu-id="b5c40-323">PERF_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="b5c40-323">PERF_WAKE_COUNTER</span></span> |
| <span data-ttu-id="b5c40-324">SYSTEM_PROCESS_KW_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="b5c40-324">SYSTEM_PROCESS_KW_WAKE_DROP</span></span> | <span data-ttu-id="b5c40-325">PERF_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="b5c40-325">PERF_WAKE_DROP</span></span> |
| <span data-ttu-id="b5c40-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="b5c40-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span></span> | <span data-ttu-id="b5c40-327">PERF_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="b5c40-327">PERF_WAKE_EVENT</span></span> |
| <span data-ttu-id="b5c40-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span></span> | <span data-ttu-id="b5c40-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="b5c40-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span></span> |
| <span data-ttu-id="b5c40-330">SYSTEM_PROCESS_KW_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="b5c40-330">SYSTEM_PROCESS_KW_DBGPRINT</span></span> | <span data-ttu-id="b5c40-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="b5c40-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span></span> |
| <span data-ttu-id="b5c40-332">SYSTEM_PROCESS_KW_JOB</span><span class="sxs-lookup"><span data-stu-id="b5c40-332">SYSTEM_PROCESS_KW_JOB</span></span> | <span data-ttu-id="b5c40-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span><span class="sxs-lookup"><span data-stu-id="b5c40-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span></span> |
| <span data-ttu-id="b5c40-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="b5c40-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span></span> | <span data-ttu-id="b5c40-335">PERF_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="b5c40-335">PERF_WORKER_THREAD</span></span> |
| <span data-ttu-id="b5c40-336">SYSTEM_PROCESS_KW_THREAD</span><span class="sxs-lookup"><span data-stu-id="b5c40-336">SYSTEM_PROCESS_KW_THREAD</span></span> | <span data-ttu-id="b5c40-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span><span class="sxs-lookup"><span data-stu-id="b5c40-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span></span> |
| <span data-ttu-id="b5c40-338">SYSTEM_PROCESS_KW_LOADER</span><span class="sxs-lookup"><span data-stu-id="b5c40-338">SYSTEM_PROCESS_KW_LOADER</span></span> | <span data-ttu-id="b5c40-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span><span class="sxs-lookup"><span data-stu-id="b5c40-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span></span> |
 
### <a name="system-profile-provider"></a><span data-ttu-id="b5c40-340">Proveedor de perfiles de sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-340">System Profile Provider</span></span> 

<span data-ttu-id="b5c40-341">Proporciona eventos de generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="b5c40-341">Provides profiling events.</span></span>

<span data-ttu-id="b5c40-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span><span class="sxs-lookup"><span data-stu-id="b5c40-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span></span>

| <span data-ttu-id="b5c40-343">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-343">Keyword</span></span> | <span data-ttu-id="b5c40-344">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-344">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-345">SYSTEM_PROFILE_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-345">SYSTEM_PROFILE_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b5c40-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span></span> |
| <span data-ttu-id="b5c40-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b5c40-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span></span> | <span data-ttu-id="b5c40-348">PERF_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b5c40-348">PERF_PMC_PROFILE</span></span> |
 
### <a name="system-registry-provider"></a><span data-ttu-id="b5c40-349">Proveedor del Registro del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-349">System Registry Provider</span></span> 

<span data-ttu-id="b5c40-350">Proporciona eventos relacionados con el Registro.</span><span class="sxs-lookup"><span data-stu-id="b5c40-350">Provides events relating to the registry.</span></span>

<span data-ttu-id="b5c40-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span><span class="sxs-lookup"><span data-stu-id="b5c40-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span></span>

| <span data-ttu-id="b5c40-352">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-352">Keyword</span></span> | <span data-ttu-id="b5c40-353">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-353">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-354">SYSTEM_REGISTRY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-354">SYSTEM_REGISTRY_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="b5c40-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span></span> |
| <span data-ttu-id="b5c40-356">SYSTEM_REGISTRY_KW_HIVE</span><span class="sxs-lookup"><span data-stu-id="b5c40-356">SYSTEM_REGISTRY_KW_HIVE</span></span> | <span data-ttu-id="b5c40-357">PERF_REG_HIVE</span><span class="sxs-lookup"><span data-stu-id="b5c40-357">PERF_REG_HIVE</span></span> |
| <span data-ttu-id="b5c40-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b5c40-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span></span> | <span data-ttu-id="b5c40-359">PERF_REG_NOTIF</span><span class="sxs-lookup"><span data-stu-id="b5c40-359">PERF_REG_NOTIF</span></span> |
 
### <a name="system-scheduler-provider"></a><span data-ttu-id="b5c40-360">Proveedor de System Scheduler</span><span class="sxs-lookup"><span data-stu-id="b5c40-360">System Scheduler Provider</span></span> 

<span data-ttu-id="b5c40-361">Proporciona eventos relacionados con el programador.</span><span class="sxs-lookup"><span data-stu-id="b5c40-361">Provides events relating to the scheduler.</span></span>

<span data-ttu-id="b5c40-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span><span class="sxs-lookup"><span data-stu-id="b5c40-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span></span>

| <span data-ttu-id="b5c40-363">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-363">Keyword</span></span> | <span data-ttu-id="b5c40-364">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-364">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="b5c40-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span></span> | <span data-ttu-id="b5c40-366">PERF_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="b5c40-366">PERF_XSCHEDULER</span></span> |
| <span data-ttu-id="b5c40-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="b5c40-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span></span> | <span data-ttu-id="b5c40-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="b5c40-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span></span> |
| <span data-ttu-id="b5c40-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="b5c40-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span></span> | <span data-ttu-id="b5c40-370">PERF_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="b5c40-370">PERF_KERNEL_QUEUE</span></span> |
| <span data-ttu-id="b5c40-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="b5c40-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span></span> | <span data-ttu-id="b5c40-372">PERF_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="b5c40-372">PERF_SHOULD_YIELD</span></span> |
| <span data-ttu-id="b5c40-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="b5c40-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span></span> | <span data-ttu-id="b5c40-374">PERF_ANTI_STARVATION</span><span class="sxs-lookup"><span data-stu-id="b5c40-374">PERF_ANTI_STARVATION</span></span> |
| <span data-ttu-id="b5c40-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="b5c40-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span></span> | <span data-ttu-id="b5c40-376">PERF_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="b5c40-376">PERF_LOAD_BALANCER</span></span> |
| <span data-ttu-id="b5c40-377">SYSTEM_SCHEDULER_KW_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="b5c40-377">SYSTEM_SCHEDULER_KW_AFFINITY</span></span> | <span data-ttu-id="b5c40-378">PERF_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="b5c40-378">PERF_AFFINITY</span></span> |
| <span data-ttu-id="b5c40-379">SYSTEM_SCHEDULER_KW_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="b5c40-379">SYSTEM_SCHEDULER_KW_PRIORITY</span></span> | <span data-ttu-id="b5c40-380">PERF_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="b5c40-380">PERF_PRIORITY</span></span> |
| <span data-ttu-id="b5c40-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="b5c40-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span></span> | <span data-ttu-id="b5c40-382">PERF_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="b5c40-382">PERF_IDEAL_PROCESSOR</span></span> |
| <span data-ttu-id="b5c40-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span><span class="sxs-lookup"><span data-stu-id="b5c40-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span></span> | <span data-ttu-id="b5c40-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span><span class="sxs-lookup"><span data-stu-id="b5c40-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span></span> |
 
### <a name="system-syscall-provider"></a><span data-ttu-id="b5c40-385">Proveedor de llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-385">System Syscall Provider</span></span> 

<span data-ttu-id="b5c40-386">Proporciona eventos con información sobre las llamadas del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5c40-386">Provides events with information about system calls.</span></span>

<span data-ttu-id="b5c40-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span><span class="sxs-lookup"><span data-stu-id="b5c40-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span></span>

| <span data-ttu-id="b5c40-388">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-388">Keyword</span></span> | <span data-ttu-id="b5c40-389">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-389">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-390">SYSTEM_SYSCALL_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-390">SYSTEM_SYSCALL_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span><span class="sxs-lookup"><span data-stu-id="b5c40-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span></span> |
 
### <a name="system-timer-provider"></a><span data-ttu-id="b5c40-392">Proveedor de temporizadores del sistema</span><span class="sxs-lookup"><span data-stu-id="b5c40-392">System Timer Provider</span></span> 

<span data-ttu-id="b5c40-393">Proporciona eventos relacionados con los temporizadores del kernel.</span><span class="sxs-lookup"><span data-stu-id="b5c40-393">Provides events relating to timers in the kernel.</span></span>

<span data-ttu-id="b5c40-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span><span class="sxs-lookup"><span data-stu-id="b5c40-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span></span>

| <span data-ttu-id="b5c40-395">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="b5c40-395">Keyword</span></span> | <span data-ttu-id="b5c40-396">Marcas y grupos heredados correspondientes</span><span class="sxs-lookup"><span data-stu-id="b5c40-396">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="b5c40-397">SYSTEM_TIMER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="b5c40-397">SYSTEM_TIMER_KW_GENERAL</span></span> | <span data-ttu-id="b5c40-398">PERF_TIMER</span><span class="sxs-lookup"><span data-stu-id="b5c40-398">PERF_TIMER</span></span> |
| <span data-ttu-id="b5c40-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="b5c40-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span></span> | <span data-ttu-id="b5c40-400">PERF_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="b5c40-400">PERF_CLOCK_TIMER</span></span> |
 
## <a name="remarks"></a><span data-ttu-id="b5c40-401">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5c40-401">Remarks</span></span>

<span data-ttu-id="b5c40-402">Este nuevo mecanismo de habilitación se suma a los métodos ya existentes para habilitar estos eventos.</span><span class="sxs-lookup"><span data-stu-id="b5c40-402">This new enablement mechanism is in addition to the pre-existing methods for enabling these events.</span></span>  <span data-ttu-id="b5c40-403">Cualquier código que solía funcionar, lo seguirá haciendo.</span><span class="sxs-lookup"><span data-stu-id="b5c40-403">Any code that used to work, will continue to do so.</span></span>
 
<span data-ttu-id="b5c40-404">Los eventos generados por el proveedor de seguimiento del sistema no cambian debido a esta nueva característica.</span><span class="sxs-lookup"><span data-stu-id="b5c40-404">The events generated by the System Trace Provider are not changing due to this new feature.</span></span>  <span data-ttu-id="b5c40-405">Esto significa que los eventos de salida no se marcan como emitidos desde los proveedores de sistema individuales.</span><span class="sxs-lookup"><span data-stu-id="b5c40-405">This means that the outputted events are not marked as being emitted from the individual system providers.</span></span>
 
<span data-ttu-id="b5c40-406">Para obtener más información sobre el GUID del proveedor y las definiciones de palabras clave, [vea evntrace.h](/windows/win32/api/evntrace/).</span><span class="sxs-lookup"><span data-stu-id="b5c40-406">For more information on provider GUID and keyword definitions see [evntrace.h](/windows/win32/api/evntrace/).</span></span>

## <a name="see-also"></a><span data-ttu-id="b5c40-407">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b5c40-407">See Also</span></span>

[<span data-ttu-id="b5c40-408">Configuración e inicio de una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="b5c40-408">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)

[<span data-ttu-id="b5c40-409">encabezado evntrace.h</span><span class="sxs-lookup"><span data-stu-id="b5c40-409">evntrace.h header</span></span>](/windows/win32/api/evntrace/)