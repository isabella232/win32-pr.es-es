---
title: Enumeración VMDVDDriveAttachmentType (VPCCOMInterfaces. h)
description: Especifica lo que se adjunta a una unidad de DVD.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- Enumeración de VMDVDDriveAttachmentType Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491285"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="12781-104">Enumeración VMDVDDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="12781-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="12781-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="12781-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="12781-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="12781-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="12781-107">Especifica lo que se adjunta a una unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="12781-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="12781-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12781-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="12781-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="12781-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12781-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="12781-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="12781-111">No hay nada adjunto.</span><span class="sxs-lookup"><span data-stu-id="12781-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="12781-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**imagen de vmDVDDrive \_**</span><span class="sxs-lookup"><span data-stu-id="12781-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="12781-113">Hay un archivo de imagen ISO adjunto.</span><span class="sxs-lookup"><span data-stu-id="12781-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="12781-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="12781-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="12781-115">Hay una unidad de CD o DVD de host conectada.</span><span class="sxs-lookup"><span data-stu-id="12781-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12781-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12781-116">Requirements</span></span>



| <span data-ttu-id="12781-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="12781-117">Requirement</span></span> | <span data-ttu-id="12781-118">Value</span><span class="sxs-lookup"><span data-stu-id="12781-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="12781-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12781-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12781-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="12781-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12781-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12781-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12781-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="12781-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="12781-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="12781-123">End of client support</span></span><br/>    | <span data-ttu-id="12781-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="12781-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="12781-125">Producto</span><span class="sxs-lookup"><span data-stu-id="12781-125">Product</span></span><br/>                  | <span data-ttu-id="12781-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="12781-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="12781-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12781-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="12781-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="12781-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12781-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="12781-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12781-130">**IVMDVDDrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="12781-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

