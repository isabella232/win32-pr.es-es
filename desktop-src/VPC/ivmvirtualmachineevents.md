---
title: Interfaz IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Define la interfaz de eventos salientes para la interfaz IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Interfaz IVMVirtualMachineEvents Virtual PC
- Interfaz IVMVirtualMachineEvents Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492562"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="812be-105">Interfaz IVMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="812be-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="812be-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="812be-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="812be-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="812be-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="812be-108">Define la interfaz de eventos salientes para la interfaz [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="812be-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="812be-109">El cliente implementa estos métodos para recibir los eventos enviados desde [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="812be-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="812be-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="812be-110">Members</span></span>

<span data-ttu-id="812be-111">La interfaz **IVMVirtualMachineEvents** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="812be-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="812be-112">**IVMVirtualMachineEvents** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="812be-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="812be-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="812be-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="812be-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="812be-114">Methods</span></span>

<span data-ttu-id="812be-115">La interfaz **IVMVirtualMachineEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="812be-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="812be-116">Método</span><span class="sxs-lookup"><span data-stu-id="812be-116">Method</span></span>                                                                                   | <span data-ttu-id="812be-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="812be-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="812be-118">**OnAdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="812be-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="812be-119">Recibe una notificación de que los componentes de integración están disponibles en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="812be-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="812be-120">**OnAdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="812be-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="812be-121">Recibe la notificación de que los componentes de integración se desinstalan en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="812be-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="812be-122">**OnConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="812be-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="812be-123">Recibe la notificación de que ha cambiado un valor de la configuración de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="812be-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="812be-124">**OnDiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="812be-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="812be-125">Recibe la notificación de que un disco necesario para una máquina virtual está sin espacio y la máquina virtual no se puede ejecutar.</span><span class="sxs-lookup"><span data-stu-id="812be-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="812be-126">**OnEnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="812be-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="812be-127">Recibe una notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.</span><span class="sxs-lookup"><span data-stu-id="812be-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="812be-128">**OnGuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="812be-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="812be-129">Recibe la notificación de que un usuario ha cerrado la sesión del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="812be-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="812be-130">**OnGuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="812be-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="812be-131">Recibe la notificación de que el sistema operativo invitado se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="812be-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="812be-132">**OnHeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="812be-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="812be-133">Recibe la notificación de que el latido de una máquina virtual se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="812be-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="812be-134">Esto normalmente indica que el sistema operativo invitado se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="812be-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="812be-135">**OnRequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="812be-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="812be-136">Recibe la notificación de que se ha realizado una solicitud de cierre.</span><span class="sxs-lookup"><span data-stu-id="812be-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="812be-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="812be-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="812be-138">Recibe la notificación de que una máquina virtual se ha restablecido.</span><span class="sxs-lookup"><span data-stu-id="812be-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="812be-139">**OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="812be-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="812be-140">Recibe la notificación de que el estado de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="812be-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="812be-141">**OnTripleFault**</span><span class="sxs-lookup"><span data-stu-id="812be-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="812be-142">Recibe la notificación de que una máquina virtual tiene un error triple.</span><span class="sxs-lookup"><span data-stu-id="812be-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="812be-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="812be-143">Requirements</span></span>



| <span data-ttu-id="812be-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="812be-144">Requirement</span></span> | <span data-ttu-id="812be-145">Value</span><span class="sxs-lookup"><span data-stu-id="812be-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="812be-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="812be-146">Minimum supported client</span></span><br/> | <span data-ttu-id="812be-147">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="812be-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="812be-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="812be-148">Minimum supported server</span></span><br/> | <span data-ttu-id="812be-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="812be-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="812be-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="812be-150">End of client support</span></span><br/>    | <span data-ttu-id="812be-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="812be-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="812be-152">Producto</span><span class="sxs-lookup"><span data-stu-id="812be-152">Product</span></span><br/>                  | <span data-ttu-id="812be-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="812be-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="812be-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="812be-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="812be-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="812be-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="812be-156">IID</span><span class="sxs-lookup"><span data-stu-id="812be-156">IID</span></span><br/>                      | <span data-ttu-id="812be-157">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="812be-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

