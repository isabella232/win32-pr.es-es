---
title: Enumeración VMStartupOption (VPCCOMInterfaces. h)
description: Especifica la opción de inicio.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- Enumeración de VMStartupOption Virtual PC
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490432"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="68e7a-104">Enumeración VMStartupOption</span><span class="sxs-lookup"><span data-stu-id="68e7a-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="68e7a-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="68e7a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="68e7a-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="68e7a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="68e7a-107">Especifica la opción de inicio.</span><span class="sxs-lookup"><span data-stu-id="68e7a-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e7a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68e7a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="68e7a-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="68e7a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="68e7a-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption \_ normal**</span><span class="sxs-lookup"><span data-stu-id="68e7a-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="68e7a-111">Iniciar normalmente.</span><span class="sxs-lookup"><span data-stu-id="68e7a-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="68e7a-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption \_ FixParentTimestampMismatch**</span><span class="sxs-lookup"><span data-stu-id="68e7a-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="68e7a-113">Corrija la marca de tiempo principal no coincidente.</span><span class="sxs-lookup"><span data-stu-id="68e7a-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68e7a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e7a-114">Requirements</span></span>



| <span data-ttu-id="68e7a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e7a-115">Requirement</span></span> | <span data-ttu-id="68e7a-116">Value</span><span class="sxs-lookup"><span data-stu-id="68e7a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e7a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e7a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68e7a-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="68e7a-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68e7a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e7a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68e7a-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="68e7a-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="68e7a-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="68e7a-121">End of client support</span></span><br/>    | <span data-ttu-id="68e7a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68e7a-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="68e7a-123">Producto</span><span class="sxs-lookup"><span data-stu-id="68e7a-123">Product</span></span><br/>                  | <span data-ttu-id="68e7a-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="68e7a-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="68e7a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68e7a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="68e7a-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="68e7a-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e7a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="68e7a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e7a-128">**IVMVirtualMachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="68e7a-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

