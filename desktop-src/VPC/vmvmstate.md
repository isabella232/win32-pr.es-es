---
title: Enumeración VMVMState (VPCCOMInterfaces. h)
description: Especifica el estado de una máquina virtual.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- Enumeración de VMVMState Virtual PC
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696011"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="5a623-104">Enumeración VMVMState</span><span class="sxs-lookup"><span data-stu-id="5a623-104">VMVMState enumeration</span></span>

<span data-ttu-id="5a623-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5a623-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5a623-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5a623-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5a623-107">Especifica el estado de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a623-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a623-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a623-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a><span data-ttu-id="5a623-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="5a623-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5a623-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="5a623-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-111">Un estado no válido (no debe ocurrir si existe la máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="5a623-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="5a623-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState \_ TurnedOff**</span><span class="sxs-lookup"><span data-stu-id="5a623-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-113">Desactivado y no guardado.</span><span class="sxs-lookup"><span data-stu-id="5a623-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ guardado**</span><span class="sxs-lookup"><span data-stu-id="5a623-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-115">Desactivado pero se guarda el invitado.</span><span class="sxs-lookup"><span data-stu-id="5a623-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**Desactivación de vmVMState \_**</span><span class="sxs-lookup"><span data-stu-id="5a623-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-117">En el proceso de activación.</span><span class="sxs-lookup"><span data-stu-id="5a623-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState \_ restauración**</span><span class="sxs-lookup"><span data-stu-id="5a623-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-119">Restaurar el estado.</span><span class="sxs-lookup"><span data-stu-id="5a623-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState en \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="5a623-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-121">En ejecución y no en pausa.</span><span class="sxs-lookup"><span data-stu-id="5a623-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState en \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="5a623-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-123">En ejecución y en pausa.</span><span class="sxs-lookup"><span data-stu-id="5a623-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState \_ Guardar**</span><span class="sxs-lookup"><span data-stu-id="5a623-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-125">Guardar el estado.</span><span class="sxs-lookup"><span data-stu-id="5a623-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState \_ TurningOff**</span><span class="sxs-lookup"><span data-stu-id="5a623-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-127">En el proceso de desactivación.</span><span class="sxs-lookup"><span data-stu-id="5a623-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState \_ MergingDrives**</span><span class="sxs-lookup"><span data-stu-id="5a623-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-129">En el proceso de combinación de las unidades de deshacer.</span><span class="sxs-lookup"><span data-stu-id="5a623-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="5a623-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState \_ DeleteMachine**</span><span class="sxs-lookup"><span data-stu-id="5a623-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="5a623-131">Eliminando la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a623-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a623-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a623-132">Requirements</span></span>



| <span data-ttu-id="5a623-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a623-133">Requirement</span></span> | <span data-ttu-id="5a623-134">Value</span><span class="sxs-lookup"><span data-stu-id="5a623-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a623-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a623-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5a623-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a623-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a623-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a623-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5a623-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5a623-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5a623-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5a623-139">End of client support</span></span><br/>    | <span data-ttu-id="5a623-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5a623-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5a623-141">Producto</span><span class="sxs-lookup"><span data-stu-id="5a623-141">Product</span></span><br/>                  | <span data-ttu-id="5a623-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5a623-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5a623-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a623-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a623-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a623-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a623-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a623-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a623-146">**IVMVirtualMachine:: State**</span><span class="sxs-lookup"><span data-stu-id="5a623-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="5a623-147">**IVMVirtualMachineEvents:: OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a623-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="5a623-148">**IVMVirtualPCEvents::OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a623-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

