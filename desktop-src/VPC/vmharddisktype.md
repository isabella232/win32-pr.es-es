---
title: Enumeración VMHardDiskType (VPCCOMInterfaces. h)
description: Especifica el tipo de imagen de disco duro.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- Enumeración de VMHardDiskType Virtual PC
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695982"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="c79bf-104">Enumeración VMHardDiskType</span><span class="sxs-lookup"><span data-stu-id="c79bf-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="c79bf-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c79bf-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c79bf-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c79bf-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c79bf-107">Especifica el tipo de imagen de disco duro.</span><span class="sxs-lookup"><span data-stu-id="c79bf-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c79bf-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="c79bf-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="c79bf-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c79bf-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType \_ dinámico**</span><span class="sxs-lookup"><span data-stu-id="c79bf-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="c79bf-111">Una imagen de disco duro de expansión dinámica.</span><span class="sxs-lookup"><span data-stu-id="c79bf-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="c79bf-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType \_ FixedSize**</span><span class="sxs-lookup"><span data-stu-id="c79bf-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="c79bf-113">Una imagen de disco duro de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="c79bf-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="c79bf-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**diferencia de vmDiskType \_**</span><span class="sxs-lookup"><span data-stu-id="c79bf-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="c79bf-115">Una imagen de disco duro de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="c79bf-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c79bf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c79bf-116">Requirements</span></span>



| <span data-ttu-id="c79bf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79bf-117">Requirement</span></span> | <span data-ttu-id="c79bf-118">Value</span><span class="sxs-lookup"><span data-stu-id="c79bf-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79bf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c79bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c79bf-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c79bf-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c79bf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c79bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c79bf-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c79bf-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c79bf-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c79bf-123">End of client support</span></span><br/>    | <span data-ttu-id="c79bf-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c79bf-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c79bf-125">Producto</span><span class="sxs-lookup"><span data-stu-id="c79bf-125">Product</span></span><br/>                  | <span data-ttu-id="c79bf-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c79bf-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c79bf-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c79bf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c79bf-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79bf-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79bf-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c79bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79bf-130">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="c79bf-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

