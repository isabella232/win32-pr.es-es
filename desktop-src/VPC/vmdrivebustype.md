---
title: Enumeración VMDriveBusType (VPCCOMInterfaces. h)
description: Especifica el tipo de bus.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- Enumeración de VMDriveBusType Virtual PC
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150481"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="6e2e1-104">Enumeración VMDriveBusType</span><span class="sxs-lookup"><span data-stu-id="6e2e1-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="6e2e1-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6e2e1-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6e2e1-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6e2e1-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6e2e1-107">Especifica el tipo de bus.</span><span class="sxs-lookup"><span data-stu-id="6e2e1-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e2e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e2e1-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="6e2e1-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="6e2e1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6e2e1-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="6e2e1-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="6e2e1-111">Sin tipo de bus.</span><span class="sxs-lookup"><span data-stu-id="6e2e1-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="6e2e1-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**IDE de vmDriveBusType \_**</span><span class="sxs-lookup"><span data-stu-id="6e2e1-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="6e2e1-113">Tipo de bus IDE.</span><span class="sxs-lookup"><span data-stu-id="6e2e1-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="6e2e1-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**\_SCSI vmDriveBusType**</span><span class="sxs-lookup"><span data-stu-id="6e2e1-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="6e2e1-115">Tipo de bus SCSI.</span><span class="sxs-lookup"><span data-stu-id="6e2e1-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e2e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e2e1-116">Requirements</span></span>



| <span data-ttu-id="6e2e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e2e1-117">Requirement</span></span> | <span data-ttu-id="6e2e1-118">Value</span><span class="sxs-lookup"><span data-stu-id="6e2e1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2e1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e2e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e2e1-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e2e1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e2e1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e2e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e2e1-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6e2e1-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6e2e1-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6e2e1-123">End of client support</span></span><br/>    | <span data-ttu-id="6e2e1-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e2e1-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6e2e1-125">Producto</span><span class="sxs-lookup"><span data-stu-id="6e2e1-125">Product</span></span><br/>                  | <span data-ttu-id="6e2e1-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6e2e1-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6e2e1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e2e1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e2e1-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e2e1-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

