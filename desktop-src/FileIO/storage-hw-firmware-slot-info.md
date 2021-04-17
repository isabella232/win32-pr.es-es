---
description: Esta estructura contiene información sobre una ranura de un dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: STORAGE_HW_FIRMWARE_SLOT_INFO estructura (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687009"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="4fc3e-103">\_Estructura de \_ información de ranura de firmware de hardware de \_ almacenamiento \_</span><span class="sxs-lookup"><span data-stu-id="4fc3e-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="4fc3e-104">Esta estructura contiene información sobre una ranura de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc3e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fc3e-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="4fc3e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4fc3e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4fc3e-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-108">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-108">The version of this structure.</span></span> <span data-ttu-id="4fc3e-109">Debe establecerse en sizeof (STORAGE \_ HW \_ firmware \_ slot \_ info).</span><span class="sxs-lookup"><span data-stu-id="4fc3e-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="4fc3e-110">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-111">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fc3e-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-113">El número de ranura de esta ranura.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="4fc3e-114">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-115">Indica si esta ranura es de solo lectura o no.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="4fc3e-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-117">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4fc3e-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4fc3e-120">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="4fc3e-121">La revisión del firmware en esta ranura.</span><span class="sxs-lookup"><span data-stu-id="4fc3e-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc3e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fc3e-122">Requirements</span></span>



| <span data-ttu-id="4fc3e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc3e-123">Requirement</span></span> | <span data-ttu-id="4fc3e-124">Value</span><span class="sxs-lookup"><span data-stu-id="4fc3e-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc3e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fc3e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc3e-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fc3e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="4fc3e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fc3e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc3e-128">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fc3e-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="4fc3e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fc3e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc3e-130"><dt>Winioctl. h. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fc3e-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc3e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fc3e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc3e-132">**\_ \_ Activar firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="4fc3e-133">**\_ \_ Activar firmware de HW de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="4fc3e-134">**\_descarga de \_ firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="4fc3e-135">**\_descarga de \_ firmware de hardware de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="4fc3e-136">**\_ \_ \_ obtener información de firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="4fc3e-137">**\_información de \_ firmware de HW de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="4fc3e-138">**\_consulta de \_ información de firmware de HW de almacenamiento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4fc3e-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




