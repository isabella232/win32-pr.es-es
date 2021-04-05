---
title: Enumeración VMFloppyDriveAttachmentType (VPCCOMInterfaces. h)
description: Especifica lo que se adjunta a una unidad de disquete.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- Enumeración de VMFloppyDriveAttachmentType Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996582"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="2d7a7-104">Enumeración VMFloppyDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="2d7a7-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="2d7a7-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d7a7-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d7a7-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2d7a7-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d7a7-107">Especifica lo que se adjunta a una unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="2d7a7-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7a7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d7a7-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="2d7a7-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="2d7a7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2d7a7-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="2d7a7-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="2d7a7-111">No hay nada adjunto.</span><span class="sxs-lookup"><span data-stu-id="2d7a7-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="2d7a7-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**imagen de vmFloppyDrive \_**</span><span class="sxs-lookup"><span data-stu-id="2d7a7-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="2d7a7-113">Hay un archivo de imagen de disquete conectado.</span><span class="sxs-lookup"><span data-stu-id="2d7a7-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="2d7a7-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="2d7a7-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="2d7a7-115">Hay una unidad de disquete de host conectada.</span><span class="sxs-lookup"><span data-stu-id="2d7a7-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d7a7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d7a7-116">Requirements</span></span>



| <span data-ttu-id="2d7a7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d7a7-117">Requirement</span></span> | <span data-ttu-id="2d7a7-118">Value</span><span class="sxs-lookup"><span data-stu-id="2d7a7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7a7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d7a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d7a7-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d7a7-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d7a7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d7a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d7a7-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2d7a7-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d7a7-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2d7a7-123">End of client support</span></span><br/>    | <span data-ttu-id="2d7a7-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d7a7-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d7a7-125">Producto</span><span class="sxs-lookup"><span data-stu-id="2d7a7-125">Product</span></span><br/>                  | <span data-ttu-id="2d7a7-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d7a7-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d7a7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d7a7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d7a7-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d7a7-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d7a7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d7a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7a7-130">**IVMFloppyDrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="2d7a7-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

