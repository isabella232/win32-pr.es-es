---
description: Esta estructura contiene información sobre el firmware del dispositivo.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY estructura (Winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687537"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="98bf7-103">\_Estructura de \_ consulta de información de firmware de hardware de \_ almacenamiento \_</span><span class="sxs-lookup"><span data-stu-id="98bf7-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="98bf7-104">Esta estructura contiene información sobre el firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98bf7-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="98bf7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98bf7-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="98bf7-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="98bf7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="98bf7-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="98bf7-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="98bf7-108">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="98bf7-108">The version of this structure.</span></span> <span data-ttu-id="98bf7-109">Debe establecerse en sizeof (STORAGE \_ HW \_ firmware \_ info \_ Query).</span><span class="sxs-lookup"><span data-stu-id="98bf7-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="98bf7-110">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="98bf7-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="98bf7-111">Tamaño de esta estructura como un búfer.</span><span class="sxs-lookup"><span data-stu-id="98bf7-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="98bf7-112">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="98bf7-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="98bf7-113">Marcas asociadas a la consulta.</span><span class="sxs-lookup"><span data-stu-id="98bf7-113">The flags associated with the query.</span></span> <span data-ttu-id="98bf7-114">A continuación se indican las marcas que se pueden establecer en este miembro.</span><span class="sxs-lookup"><span data-stu-id="98bf7-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="98bf7-115">Marca</span><span class="sxs-lookup"><span data-stu-id="98bf7-115">Flag</span></span>                                             | <span data-ttu-id="98bf7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="98bf7-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98bf7-117">\_controlador de \_ indicador de solicitud de firmware de hardware de \_ \_ almacenamiento \_</span><span class="sxs-lookup"><span data-stu-id="98bf7-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="98bf7-118">Indica que el destino de la solicitud que no sea la mano del dispositivo o el propio objeto.</span><span class="sxs-lookup"><span data-stu-id="98bf7-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="98bf7-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="98bf7-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="98bf7-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="98bf7-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98bf7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98bf7-121">Requirements</span></span>



| <span data-ttu-id="98bf7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="98bf7-122">Requirement</span></span> | <span data-ttu-id="98bf7-123">Value</span><span class="sxs-lookup"><span data-stu-id="98bf7-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98bf7-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98bf7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="98bf7-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="98bf7-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="98bf7-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98bf7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="98bf7-127">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="98bf7-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="98bf7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98bf7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="98bf7-129"><dt>Winioctl. h. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98bf7-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98bf7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="98bf7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bf7-131">**\_ \_ Activar firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="98bf7-132">**\_ \_ Activar firmware de HW de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="98bf7-133">**\_descarga de \_ firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="98bf7-134">**\_descarga de \_ firmware de hardware de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="98bf7-135">**\_ \_ \_ obtener información de firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="98bf7-136">**\_información de \_ firmware de HW de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="98bf7-137">**información de la ranura de firmware de \_ hardware de almacenamiento \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="98bf7-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




