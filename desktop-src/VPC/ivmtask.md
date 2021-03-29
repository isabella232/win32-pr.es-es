---
title: Interfaz IVMTask (VPCCOMInterfaces. h)
description: Use la interfaz IVMTask para supervisar y controlar tareas asincrónicas para varios métodos COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Interfaz IVMTask Virtual PC
- Interfaz IVMTask Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534768"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="88c48-105">Interfaz IVMTask</span><span class="sxs-lookup"><span data-stu-id="88c48-105">IVMTask interface</span></span>

<span data-ttu-id="88c48-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88c48-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88c48-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88c48-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88c48-108">Use la interfaz **IVMTask** para supervisar y controlar tareas asincrónicas para varios métodos com.</span><span class="sxs-lookup"><span data-stu-id="88c48-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="88c48-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="88c48-109">Members</span></span>

<span data-ttu-id="88c48-110">La interfaz **IVMTask** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="88c48-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="88c48-111">**IVMTask** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="88c48-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="88c48-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="88c48-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="88c48-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88c48-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88c48-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="88c48-114">Methods</span></span>

<span data-ttu-id="88c48-115">La interfaz **IVMTask** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="88c48-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="88c48-116">Método</span><span class="sxs-lookup"><span data-stu-id="88c48-116">Method</span></span>                                                 | <span data-ttu-id="88c48-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="88c48-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88c48-118">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="88c48-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="88c48-119">Cancela la tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="88c48-120">**WaitForCompletion**</span><span class="sxs-lookup"><span data-stu-id="88c48-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="88c48-121">Espera a que se complete la tarea o a que transcurra el intervalo de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="88c48-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="88c48-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88c48-122">Properties</span></span>

<span data-ttu-id="88c48-123">La interfaz **IVMTask** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="88c48-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="88c48-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88c48-124">Property</span></span>                                                        | <span data-ttu-id="88c48-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="88c48-125">Access type</span></span>          | <span data-ttu-id="88c48-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="88c48-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="88c48-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88c48-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="88c48-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-128">Read-only</span></span><br/> | <span data-ttu-id="88c48-129">Una descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="88c48-130">**Error**</span><span class="sxs-lookup"><span data-stu-id="88c48-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="88c48-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-131">Read-only</span></span><br/> | <span data-ttu-id="88c48-132">Error registrado para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="88c48-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="88c48-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="88c48-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-134">Read-only</span></span><br/> | <span data-ttu-id="88c48-135">La descripción de error localizada registrada para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="88c48-136">**id**</span><span class="sxs-lookup"><span data-stu-id="88c48-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="88c48-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-137">Read-only</span></span><br/> | <span data-ttu-id="88c48-138">Identificador único para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="88c48-139">**IsCancelable**</span><span class="sxs-lookup"><span data-stu-id="88c48-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="88c48-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-140">Read-only</span></span><br/> | <span data-ttu-id="88c48-141">Indica si la tarea se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="88c48-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="88c48-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="88c48-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="88c48-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-143">Read-only</span></span><br/> | <span data-ttu-id="88c48-144">Indica si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="88c48-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="88c48-145">**PercentCompleted**</span><span class="sxs-lookup"><span data-stu-id="88c48-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="88c48-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-146">Read-only</span></span><br/> | <span data-ttu-id="88c48-147">Porcentaje de finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="88c48-148">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="88c48-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="88c48-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88c48-149">Read-only</span></span><br/> | <span data-ttu-id="88c48-150">Resultado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="88c48-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="88c48-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88c48-151">Remarks</span></span>

<span data-ttu-id="88c48-152">Un objeto **IVMTask** es devuelto por métodos que podrían requerir una cantidad considerable de tiempo para completarse.</span><span class="sxs-lookup"><span data-stu-id="88c48-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="88c48-153">Esto permite que la aplicación supervise el progreso de la operación deseada sin forzarla a bloquear la ejecución mientras se espera la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="88c48-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="88c48-154">Los métodos siguientes devuelven un objeto **IVMTask** que se puede usar para realizar el seguimiento del progreso:</span><span class="sxs-lookup"><span data-stu-id="88c48-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="88c48-155">**IVMGuestOS:: Logoff**</span><span class="sxs-lookup"><span data-stu-id="88c48-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="88c48-156">**IVMGuestOS:: restart**</span><span class="sxs-lookup"><span data-stu-id="88c48-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="88c48-157">**IVMGuestOS:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="88c48-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="88c48-158">**IVMHardDisk:: Compact**</span><span class="sxs-lookup"><span data-stu-id="88c48-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="88c48-159">**IVMHardDisk:: Convert**</span><span class="sxs-lookup"><span data-stu-id="88c48-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="88c48-160">**IVMHardDisk:: Merge**</span><span class="sxs-lookup"><span data-stu-id="88c48-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="88c48-161">**IVMHardDisk:: Mergeto**</span><span class="sxs-lookup"><span data-stu-id="88c48-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="88c48-162">**IVMVirtualMachine::MergeUndoDisks**</span><span class="sxs-lookup"><span data-stu-id="88c48-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="88c48-163">**IVMVirtualMachine:: RESET**</span><span class="sxs-lookup"><span data-stu-id="88c48-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="88c48-164">**IVMVirtualMachine:: Save**</span><span class="sxs-lookup"><span data-stu-id="88c48-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="88c48-165">**IVMVirtualMachine:: startup**</span><span class="sxs-lookup"><span data-stu-id="88c48-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="88c48-166">**IVMVirtualMachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="88c48-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="88c48-167">**IVMVirtualMachine:: desapagar**</span><span class="sxs-lookup"><span data-stu-id="88c48-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="88c48-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="88c48-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="88c48-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="88c48-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="88c48-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="88c48-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="88c48-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88c48-171">Requirements</span></span>



| <span data-ttu-id="88c48-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c48-172">Requirement</span></span> | <span data-ttu-id="88c48-173">Value</span><span class="sxs-lookup"><span data-stu-id="88c48-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c48-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88c48-174">Minimum supported client</span></span><br/> | <span data-ttu-id="88c48-175">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="88c48-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88c48-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88c48-176">Minimum supported server</span></span><br/> | <span data-ttu-id="88c48-177">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88c48-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88c48-178">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="88c48-178">End of client support</span></span><br/>    | <span data-ttu-id="88c48-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88c48-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88c48-180">Producto</span><span class="sxs-lookup"><span data-stu-id="88c48-180">Product</span></span><br/>                  | <span data-ttu-id="88c48-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88c48-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88c48-182">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88c48-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c48-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c48-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="88c48-184">IID</span><span class="sxs-lookup"><span data-stu-id="88c48-184">IID</span></span><br/>                      | <span data-ttu-id="88c48-185">IID \_ IVMTask se define como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="88c48-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

