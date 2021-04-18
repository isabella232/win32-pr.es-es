---
description: Esta estructura contiene información sobre el firmware del dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO estructura (Winioctl. h)
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
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668371"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="210e6-103">\_Estructura de \_ información de firmware de HW de almacenamiento \_</span><span class="sxs-lookup"><span data-stu-id="210e6-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="210e6-104">Esta estructura contiene información sobre el firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="210e6-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="210e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="210e6-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="210e6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="210e6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="210e6-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="210e6-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-108">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="210e6-108">The version of this structure.</span></span> <span data-ttu-id="210e6-109">Debe establecerse en sizeof (STORAGE \_ HW \_ firmware \_ info)</span><span class="sxs-lookup"><span data-stu-id="210e6-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="210e6-110">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="210e6-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-111">Tamaño de esta estructura como un búfer que incluye la ranura.</span><span class="sxs-lookup"><span data-stu-id="210e6-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="210e6-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-113">Indica que este firmware admite una actualización.</span><span class="sxs-lookup"><span data-stu-id="210e6-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="210e6-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="210e6-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="210e6-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-117">El número de ranuras de firmware en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="210e6-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="210e6-118">Esta es la dimensión de la matriz de ranuras.</span><span class="sxs-lookup"><span data-stu-id="210e6-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="210e6-119">Algunos dispositivos pueden almacenar más de una imagen de firmware, si tienen más de 1 ranura de firmware.</span><span class="sxs-lookup"><span data-stu-id="210e6-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="210e6-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="210e6-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-121">La ranura de firmware que contiene la imagen de firmware actualmente activa o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="210e6-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="210e6-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-123">La ranura de firmware que está pendiente de activación.</span><span class="sxs-lookup"><span data-stu-id="210e6-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="210e6-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-125">Indica que el firmware se aplica tanto al dispositivo como al controlador o adaptador, por ejemplo, un SSD de NVMe.</span><span class="sxs-lookup"><span data-stu-id="210e6-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="210e6-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="210e6-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="210e6-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-129">Alineación de la carga de la imagen, en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="210e6-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="210e6-130">El máximo es el \_ tamaño de página.</span><span class="sxs-lookup"><span data-stu-id="210e6-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="210e6-131">El tamaño de la transferencia es un múltiple de este tamaño.</span><span class="sxs-lookup"><span data-stu-id="210e6-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="210e6-132">Algunos protocolos requieren al menos el tamaño del sector.</span><span class="sxs-lookup"><span data-stu-id="210e6-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="210e6-133">Cuando este valor se establece en 0, significa que este valor no es válido.</span><span class="sxs-lookup"><span data-stu-id="210e6-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="210e6-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-135">Tamaño máximo de carga de la imagen, que se usa para un solo comando.</span><span class="sxs-lookup"><span data-stu-id="210e6-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="210e6-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="210e6-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="210e6-137">Contiene la información de la ranura de cada ranura del dispositivo, de tipo información de la [**ranura de firmware de hardware de almacenamiento \_ \_ \_ \_**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="210e6-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="210e6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="210e6-138">Requirements</span></span>



| <span data-ttu-id="210e6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="210e6-139">Requirement</span></span> | <span data-ttu-id="210e6-140">Value</span><span class="sxs-lookup"><span data-stu-id="210e6-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="210e6-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="210e6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="210e6-142">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="210e6-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="210e6-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="210e6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="210e6-144">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="210e6-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="210e6-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="210e6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="210e6-146"><dt>Winioctl. h. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="210e6-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="210e6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="210e6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210e6-148">**\_ \_ Activar firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="210e6-149">**\_ \_ Activar firmware de HW de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="210e6-150">**\_descarga de \_ firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="210e6-151">**\_descarga de \_ firmware de hardware de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="210e6-152">**\_ \_ \_ obtener información de firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="210e6-153">**\_consulta de \_ información de firmware de HW de almacenamiento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="210e6-154">**información de la ranura de firmware de \_ hardware de almacenamiento \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="210e6-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




