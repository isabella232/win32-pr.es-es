---
description: 'STORAGE_HW_FIRMWARE_INFO estructura: esta estructura contiene información sobre el firmware del dispositivo.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO estructura (Winioctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090963"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="11f1c-103">Estructura DE \_ INFORMACIÓN DE FIRMWARE DE HARDWARE DE \_ \_ ALMACENAMIENTO</span><span class="sxs-lookup"><span data-stu-id="11f1c-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="11f1c-104">Esta estructura contiene información sobre el firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11f1c-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11f1c-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="11f1c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="11f1c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="11f1c-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="11f1c-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-108">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="11f1c-108">The version of this structure.</span></span> <span data-ttu-id="11f1c-109">Debe establecerse en sizeof(STORAGE \_ HW \_ FIRMWARE \_ INFO)</span><span class="sxs-lookup"><span data-stu-id="11f1c-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-110">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="11f1c-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-111">Tamaño de esta estructura como búfer, incluida la ranura.</span><span class="sxs-lookup"><span data-stu-id="11f1c-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="11f1c-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-113">Indica que este firmware admite una actualización.</span><span class="sxs-lookup"><span data-stu-id="11f1c-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="11f1c-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="11f1c-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="11f1c-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-117">Número de ranuras de firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11f1c-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="11f1c-118">Esta es la dimensión de la matriz Slot.</span><span class="sxs-lookup"><span data-stu-id="11f1c-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="11f1c-119">Algunos dispositivos pueden almacenar más de una imagen de firmware, si tienen más de una ranura de firmware.</span><span class="sxs-lookup"><span data-stu-id="11f1c-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="11f1c-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="11f1c-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-121">Ranura de firmware que contiene la imagen de firmware actualmente activa o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="11f1c-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="11f1c-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-123">La ranura de firmware que está pendiente de activación.</span><span class="sxs-lookup"><span data-stu-id="11f1c-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="11f1c-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-125">Indica que el firmware se aplica tanto al dispositivo como al controlador o adaptador, por ejemplo, al SSD NVMe.</span><span class="sxs-lookup"><span data-stu-id="11f1c-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="11f1c-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="11f1c-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="11f1c-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-129">Alineación de la carga de la imagen, en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="11f1c-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="11f1c-130">El máximo es PAGE \_ SIZE.</span><span class="sxs-lookup"><span data-stu-id="11f1c-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="11f1c-131">El tamaño de transferencia es un mutliple de este tamaño.</span><span class="sxs-lookup"><span data-stu-id="11f1c-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="11f1c-132">Algunos protocolos requieren al menos un tamaño de sector.</span><span class="sxs-lookup"><span data-stu-id="11f1c-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="11f1c-133">Cuando este valor se establece en 0, significa que este valor no es válido.</span><span class="sxs-lookup"><span data-stu-id="11f1c-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="11f1c-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-135">Tamaño máximo de la carga de la imagen, que se usa para un solo comando.</span><span class="sxs-lookup"><span data-stu-id="11f1c-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="11f1c-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="11f1c-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="11f1c-137">Contiene la información de ranura para cada ranura del dispositivo, de tipo [**STORAGE HW FIRMWARE SLOT \_ \_ \_ \_ INFO**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="11f1c-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11f1c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f1c-138">Requirements</span></span>



| <span data-ttu-id="11f1c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f1c-139">Requirement</span></span> | <span data-ttu-id="11f1c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="11f1c-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f1c-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f1c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="11f1c-142">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="11f1c-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="11f1c-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f1c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="11f1c-144">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="11f1c-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="11f1c-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11f1c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f1c-146"><dt>Winioctl.h.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="11f1c-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f1c-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11f1c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f1c-148">**ACTIVACIÓN DEL \_ FIRMWARE DE ALMACENAMIENTO \_ DE IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="11f1c-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="11f1c-149">**ACTIVACIÓN \_ DEL FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="11f1c-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="11f1c-150">**DESCARGA DE \_ FIRMWARE DE ALMACENAMIENTO \_ DE IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="11f1c-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="11f1c-151">**DESCARGA \_ DE FIRMWARE DEL HARDWARE DE \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="11f1c-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="11f1c-152">**IOCTL \_ STORAGE \_ FIRMWARE \_ GET \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="11f1c-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="11f1c-153">**CONSULTA \_ DE INFORMACIÓN DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="11f1c-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="11f1c-154">**INFORMACIÓN DE \_ RANURA DE FIRMWARE DEL HARDWARE DE \_ \_ \_ ALMACENAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="11f1c-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




