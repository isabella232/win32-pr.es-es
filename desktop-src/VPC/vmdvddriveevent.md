---
title: Enumeración VMDVDDriveEvent (VPCCOMInterfaces. h)
description: Especifica los eventos de la unidad de DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Enumeración de VMDVDDriveEvent Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802197"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="9b318-104">Enumeración VMDVDDriveEvent</span><span class="sxs-lookup"><span data-stu-id="9b318-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="9b318-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b318-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9b318-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9b318-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9b318-107">Especifica los eventos de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="9b318-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b318-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b318-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="9b318-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="9b318-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9b318-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ Insert**</span><span class="sxs-lookup"><span data-stu-id="9b318-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="9b318-111">Se adjunta una imagen ISO o se inserta un medio real en una unidad host.</span><span class="sxs-lookup"><span data-stu-id="9b318-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="9b318-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ EJECT**</span><span class="sxs-lookup"><span data-stu-id="9b318-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="9b318-113">Se ha expulsado el medio.</span><span class="sxs-lookup"><span data-stu-id="9b318-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b318-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b318-114">Requirements</span></span>



| <span data-ttu-id="9b318-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b318-115">Requirement</span></span> | <span data-ttu-id="9b318-116">Value</span><span class="sxs-lookup"><span data-stu-id="9b318-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b318-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b318-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9b318-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b318-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b318-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b318-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9b318-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9b318-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9b318-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9b318-121">End of client support</span></span><br/>    | <span data-ttu-id="9b318-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b318-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9b318-123">Producto</span><span class="sxs-lookup"><span data-stu-id="9b318-123">Product</span></span><br/>                  | <span data-ttu-id="9b318-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9b318-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9b318-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b318-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b318-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b318-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b318-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b318-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b318-128">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="9b318-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

