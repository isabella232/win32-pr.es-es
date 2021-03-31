---
title: enumeración vmFloppyDriveEvent (VPCCOMInterfaces. h)
description: Especifica los eventos de la unidad de disquete.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- enumeración de vmFloppyDriveEvent Virtual PC
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803458"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="25cc3-104">enumeración vmFloppyDriveEvent</span><span class="sxs-lookup"><span data-stu-id="25cc3-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="25cc3-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25cc3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="25cc3-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="25cc3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="25cc3-107">Especifica los eventos de la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="25cc3-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="25cc3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25cc3-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="25cc3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="25cc3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="25cc3-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent \_ Insert**</span><span class="sxs-lookup"><span data-stu-id="25cc3-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="25cc3-111">Se adjunta una imagen de disquete o se inserta un medio real en una unidad de host.</span><span class="sxs-lookup"><span data-stu-id="25cc3-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="25cc3-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent \_ EJECT**</span><span class="sxs-lookup"><span data-stu-id="25cc3-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="25cc3-113">Se ha expulsado el medio.</span><span class="sxs-lookup"><span data-stu-id="25cc3-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25cc3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25cc3-114">Requirements</span></span>



| <span data-ttu-id="25cc3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25cc3-115">Requirement</span></span> | <span data-ttu-id="25cc3-116">Value</span><span class="sxs-lookup"><span data-stu-id="25cc3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="25cc3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25cc3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25cc3-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="25cc3-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25cc3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25cc3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25cc3-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25cc3-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="25cc3-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="25cc3-121">End of client support</span></span><br/>    | <span data-ttu-id="25cc3-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25cc3-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="25cc3-123">Producto</span><span class="sxs-lookup"><span data-stu-id="25cc3-123">Product</span></span><br/>                  | <span data-ttu-id="25cc3-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="25cc3-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="25cc3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25cc3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25cc3-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="25cc3-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25cc3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="25cc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25cc3-128">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="25cc3-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

