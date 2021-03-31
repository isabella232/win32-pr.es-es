---
title: Enumeración VMLogoffType (VPCCOMInterfaces. h)
description: Especifica cómo apagar una máquina virtual.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Enumeración de VMLogoffType Virtual PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079328"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="07792-104">Enumeración VMLogoffType</span><span class="sxs-lookup"><span data-stu-id="07792-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="07792-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07792-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="07792-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="07792-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="07792-107">Especifica cómo apagar una máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="07792-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="07792-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07792-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="07792-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="07792-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="07792-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normal**</span><span class="sxs-lookup"><span data-stu-id="07792-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="07792-111">El cierre de sesión en la máquina virtual invitada era normal.</span><span class="sxs-lookup"><span data-stu-id="07792-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="07792-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forzada**</span><span class="sxs-lookup"><span data-stu-id="07792-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="07792-113">Se forzó el cierre de sesión en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="07792-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="07792-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ externo**</span><span class="sxs-lookup"><span data-stu-id="07792-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="07792-115">El cierre de sesión en la máquina virtual invitada se realizó con el método [**IVMGuestOS:: Logoff**](ivmguestos-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="07792-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07792-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07792-116">Requirements</span></span>



| <span data-ttu-id="07792-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07792-117">Requirement</span></span> | <span data-ttu-id="07792-118">Value</span><span class="sxs-lookup"><span data-stu-id="07792-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07792-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07792-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07792-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="07792-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07792-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07792-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07792-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="07792-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="07792-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="07792-123">End of client support</span></span><br/>    | <span data-ttu-id="07792-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07792-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07792-125">Producto</span><span class="sxs-lookup"><span data-stu-id="07792-125">Product</span></span><br/>                  | <span data-ttu-id="07792-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="07792-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="07792-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07792-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07792-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="07792-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07792-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="07792-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07792-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="07792-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

