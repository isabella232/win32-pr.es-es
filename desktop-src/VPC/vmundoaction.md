---
title: Enumeración VMUndoAction (VPCCOMInterfaces. h)
description: Especifica lo que ocurre para deshacer las unidades cuando una máquina virtual está apagada o apagada.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Enumeración de VMUndoAction Virtual PC
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535290"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="43caf-104">Enumeración VMUndoAction</span><span class="sxs-lookup"><span data-stu-id="43caf-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="43caf-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="43caf-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43caf-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="43caf-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43caf-107">Especifica lo que ocurre para deshacer las unidades cuando una máquina virtual está apagada o apagada.</span><span class="sxs-lookup"><span data-stu-id="43caf-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="43caf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43caf-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="43caf-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="43caf-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="43caf-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**\_descartar vmUndoAction**</span><span class="sxs-lookup"><span data-stu-id="43caf-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="43caf-111">Descartar las unidades de deshacer; las unidades primarias permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="43caf-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="43caf-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ mantener**</span><span class="sxs-lookup"><span data-stu-id="43caf-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="43caf-113">Mantener las unidades de deshacer; las unidades primarias permanecen sin cambios, pero los cambios se mantendrán la próxima vez que se inicie la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43caf-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="43caf-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**confirmación de vmUndoAction \_**</span><span class="sxs-lookup"><span data-stu-id="43caf-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="43caf-115">Confirme los cambios en las unidades principales.</span><span class="sxs-lookup"><span data-stu-id="43caf-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43caf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43caf-116">Requirements</span></span>



| <span data-ttu-id="43caf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43caf-117">Requirement</span></span> | <span data-ttu-id="43caf-118">Value</span><span class="sxs-lookup"><span data-stu-id="43caf-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43caf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43caf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43caf-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="43caf-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43caf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43caf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43caf-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="43caf-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43caf-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="43caf-123">End of client support</span></span><br/>    | <span data-ttu-id="43caf-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43caf-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43caf-125">Producto</span><span class="sxs-lookup"><span data-stu-id="43caf-125">Product</span></span><br/>                  | <span data-ttu-id="43caf-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43caf-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43caf-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43caf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="43caf-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="43caf-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43caf-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="43caf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43caf-130">**IVMVirtualMachine:: UndoAction**</span><span class="sxs-lookup"><span data-stu-id="43caf-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

