---
title: Enumeración VMDriveType (VPCCOMInterfaces. h)
description: Especifica el tipo de unidad conectado a una ubicación de bus.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- Enumeración de VMDriveType Virtual PC
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802198"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="512bc-104">Enumeración VMDriveType</span><span class="sxs-lookup"><span data-stu-id="512bc-104">VMDriveType enumeration</span></span>

<span data-ttu-id="512bc-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="512bc-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="512bc-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="512bc-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="512bc-107">Especifica el tipo de unidad conectado a una ubicación de bus.</span><span class="sxs-lookup"><span data-stu-id="512bc-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="512bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="512bc-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="512bc-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="512bc-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="512bc-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ null**</span><span class="sxs-lookup"><span data-stu-id="512bc-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="512bc-111">No hay ninguna unidad conectada.</span><span class="sxs-lookup"><span data-stu-id="512bc-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="512bc-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType disco \_ duro**</span><span class="sxs-lookup"><span data-stu-id="512bc-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="512bc-113">Hay un disco duro conectado.</span><span class="sxs-lookup"><span data-stu-id="512bc-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="512bc-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**DVD de vmDriveType \_**</span><span class="sxs-lookup"><span data-stu-id="512bc-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="512bc-115">Hay una unidad de CD o DVD conectada.</span><span class="sxs-lookup"><span data-stu-id="512bc-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="512bc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="512bc-116">Requirements</span></span>



| <span data-ttu-id="512bc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="512bc-117">Requirement</span></span> | <span data-ttu-id="512bc-118">Value</span><span class="sxs-lookup"><span data-stu-id="512bc-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="512bc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="512bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="512bc-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="512bc-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="512bc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="512bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="512bc-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="512bc-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="512bc-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="512bc-123">End of client support</span></span><br/>    | <span data-ttu-id="512bc-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="512bc-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="512bc-125">Producto</span><span class="sxs-lookup"><span data-stu-id="512bc-125">Product</span></span><br/>                  | <span data-ttu-id="512bc-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="512bc-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="512bc-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="512bc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="512bc-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="512bc-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="512bc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="512bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512bc-130">**IVMVirtualMachine::AttachedDriveTypes**</span><span class="sxs-lookup"><span data-stu-id="512bc-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

