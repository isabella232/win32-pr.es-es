---
description: 'STORAGE_HW_FIRMWARE_INFO_QUERY estructura: esta estructura contiene información sobre el firmware del dispositivo.'
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY estructura (Winioctl.h)
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
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119403"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="a1e10-103">ESTRUCTURA DE CONSULTA DE INFORMACIÓN DE FIRMWARE DE HARDWARE \_ \_ DE \_ \_ ALMACENAMIENTO</span><span class="sxs-lookup"><span data-stu-id="a1e10-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="a1e10-104">Esta estructura contiene información sobre el firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1e10-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1e10-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="a1e10-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1e10-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1e10-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="a1e10-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a1e10-108">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="a1e10-108">The version of this structure.</span></span> <span data-ttu-id="a1e10-109">Debe establecerse en sizeof(STORAGE \_ HW \_ FIRMWARE INFO \_ \_ QUERY)</span><span class="sxs-lookup"><span data-stu-id="a1e10-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="a1e10-110">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="a1e10-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a1e10-111">Tamaño de esta estructura como búfer.</span><span class="sxs-lookup"><span data-stu-id="a1e10-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a1e10-112">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="a1e10-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a1e10-113">Marcas asociadas a la consulta.</span><span class="sxs-lookup"><span data-stu-id="a1e10-113">The flags associated with the query.</span></span> <span data-ttu-id="a1e10-114">Las siguientes son marcas que se pueden establecer en este miembro.</span><span class="sxs-lookup"><span data-stu-id="a1e10-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="a1e10-115">Marcar</span><span class="sxs-lookup"><span data-stu-id="a1e10-115">Flag</span></span>                                             | <span data-ttu-id="a1e10-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1e10-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e10-117">CONTROLADOR DE MARCA DE SOLICITUD DE FIRMWARE DE HARDWARE \_ \_ DE \_ \_ \_ ALMACENAMIENTO</span><span class="sxs-lookup"><span data-stu-id="a1e10-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="a1e10-118">Indica que el destino de la solicitud es distinto de la propia mano o el objeto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1e10-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a1e10-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a1e10-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a1e10-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a1e10-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1e10-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1e10-121">Requirements</span></span>



| <span data-ttu-id="a1e10-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e10-122">Requirement</span></span> | <span data-ttu-id="a1e10-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e10-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e10-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1e10-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e10-125">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="a1e10-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="a1e10-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1e10-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e10-127">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1e10-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="a1e10-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1e10-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e10-129"><dt>Winioctl.h.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1e10-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1e10-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1e10-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e10-131">**ACTIVACIÓN DEL \_ FIRMWARE DE \_ ALMACENAMIENTO DE IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a1e10-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a1e10-132">**ACTIVACIÓN DEL \_ FIRMWARE DEL HW DE \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="a1e10-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a1e10-133">**DESCARGA DE \_ FIRMWARE DE \_ ALMACENAMIENTO DE IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a1e10-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="a1e10-134">**DESCARGA DE \_ FIRMWARE DE HARDWARE DE \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="a1e10-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="a1e10-135">**IOCTL \_ STORAGE \_ FIRMWARE \_ GET \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="a1e10-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="a1e10-136">**INFORMACIÓN \_ DE FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="a1e10-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="a1e10-137">**INFORMACIÓN DE \_ RANURA DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="a1e10-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




