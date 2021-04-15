---
title: Enumeración VMShutdownAction (VPCCOMInterfaces. h)
description: Especifica cómo apagar una máquina virtual cuando el host se apaga o finaliza el proceso de vpc.exe.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Enumeración de VMShutdownAction Virtual PC
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695926"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="84db1-104">Enumeración VMShutdownAction</span><span class="sxs-lookup"><span data-stu-id="84db1-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="84db1-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84db1-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84db1-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84db1-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84db1-107">Especifica cómo apagar una máquina virtual (VM) cuando el host se apaga o finaliza el proceso de vpc.exe.</span><span class="sxs-lookup"><span data-stu-id="84db1-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="84db1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84db1-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="84db1-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="84db1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="84db1-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ Guardar**</span><span class="sxs-lookup"><span data-stu-id="84db1-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="84db1-111">Guarde el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="84db1-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="84db1-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**desvmShutdownActionción de la \_**</span><span class="sxs-lookup"><span data-stu-id="84db1-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="84db1-113">Apague la máquina virtual sin deshacer las unidades.</span><span class="sxs-lookup"><span data-stu-id="84db1-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="84db1-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**cierre de vmShutdownAction \_**</span><span class="sxs-lookup"><span data-stu-id="84db1-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="84db1-115">Apague el sistema operativo invitado en la máquina virtual sin deshacer las unidades si los componentes de integración están disponibles y guardará la máquina virtual en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="84db1-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84db1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84db1-116">Requirements</span></span>



| <span data-ttu-id="84db1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="84db1-117">Requirement</span></span> | <span data-ttu-id="84db1-118">Value</span><span class="sxs-lookup"><span data-stu-id="84db1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84db1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84db1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84db1-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="84db1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84db1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84db1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84db1-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="84db1-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84db1-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="84db1-123">End of client support</span></span><br/>    | <span data-ttu-id="84db1-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84db1-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84db1-125">Producto</span><span class="sxs-lookup"><span data-stu-id="84db1-125">Product</span></span><br/>                  | <span data-ttu-id="84db1-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84db1-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84db1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84db1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="84db1-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84db1-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84db1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="84db1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84db1-130">Enumeraciones de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84db1-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="84db1-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="84db1-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

