---
title: Enumeración VMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Especifica los eventos de máquina virtual.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- Enumeración de VMVirtualMachineEvents Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079670"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="8471e-104">Enumeración VMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="8471e-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="8471e-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8471e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8471e-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8471e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8471e-107">Especifica los eventos de máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="8471e-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="8471e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8471e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="8471e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="8471e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8471e-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent \_ StateChanged**</span><span class="sxs-lookup"><span data-stu-id="8471e-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-111">El estado de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8471e-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ RequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="8471e-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-113">Se ha solicitado un cierre.</span><span class="sxs-lookup"><span data-stu-id="8471e-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**restablecimiento de vmVirtualMachineEvent \_**</span><span class="sxs-lookup"><span data-stu-id="8471e-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-115">Una máquina virtual se ha restablecido.</span><span class="sxs-lookup"><span data-stu-id="8471e-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent \_ TripleFault**</span><span class="sxs-lookup"><span data-stu-id="8471e-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-117">Una máquina virtual tiene tres errores.</span><span class="sxs-lookup"><span data-stu-id="8471e-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent \_ HeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="8471e-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-119">El latido de una máquina virtual se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="8471e-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="8471e-120">Esto normalmente indica que el sistema operativo invitado se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8471e-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent \_ ConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="8471e-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-122">Ha cambiado un valor en la configuración de esta máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8471e-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="8471e-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent \_ EnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="8471e-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-124">El modo de vídeo de una máquina virtual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8471e-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent \_ AdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="8471e-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-126">Los componentes de integración se han desinstalado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8471e-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent \_ AdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="8471e-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-128">La integración está disponible en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="8471e-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ GuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="8471e-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-130">Se está cerrando un sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="8471e-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent \_ GuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="8471e-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-132">Un usuario cerró sesión en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="8471e-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent \_ DiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="8471e-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="8471e-134">Espacio insuficiente en el disco que necesita la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8471e-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8471e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8471e-135">Requirements</span></span>



| <span data-ttu-id="8471e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8471e-136">Requirement</span></span> | <span data-ttu-id="8471e-137">Value</span><span class="sxs-lookup"><span data-stu-id="8471e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8471e-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8471e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8471e-139">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8471e-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8471e-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8471e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8471e-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8471e-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8471e-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8471e-142">End of client support</span></span><br/>    | <span data-ttu-id="8471e-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8471e-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8471e-144">Producto</span><span class="sxs-lookup"><span data-stu-id="8471e-144">Product</span></span><br/>                  | <span data-ttu-id="8471e-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8471e-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8471e-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8471e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8471e-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8471e-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8471e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="8471e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8471e-149">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="8471e-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

