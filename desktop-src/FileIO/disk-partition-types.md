---
description: Tipos de partición válidos usados por los controladores de disco.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Tipos de partición de disco (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668373"
---
# <a name="disk-partition-types"></a><span data-ttu-id="a9c10-103">Tipos de partición de disco</span><span class="sxs-lookup"><span data-stu-id="a9c10-103">Disk Partition Types</span></span>

<span data-ttu-id="a9c10-104">En la tabla siguiente se identifican los tipos de partición válidos que usan los controladores de disco.</span><span class="sxs-lookup"><span data-stu-id="a9c10-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="a9c10-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a9c10-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="a9c10-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9c10-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="a9c10-107"><dt>**Partición \_ de ENTRADA \_ no utilizada**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="a9c10-108">Una partición de entrada sin usar.</span><span class="sxs-lookup"><span data-stu-id="a9c10-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="a9c10-109"><dt>**Partición \_ de 0x05 EXTENDIda**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="a9c10-110">Una partición extendida.</span><span class="sxs-lookup"><span data-stu-id="a9c10-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="a9c10-111"><dt>**Partición \_ de FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="a9c10-112">Una partición del sistema de archivos FAT12.</span><span class="sxs-lookup"><span data-stu-id="a9c10-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="a9c10-113"><dt>**Partición \_ de FAT \_ 16**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="a9c10-114">Una partición del sistema de archivos FAT16.</span><span class="sxs-lookup"><span data-stu-id="a9c10-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="a9c10-115"><dt>**Partición \_ de FAT32**</dt> <dt>0x0B</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="a9c10-116">Una partición del sistema de archivos FAT32.</span><span class="sxs-lookup"><span data-stu-id="a9c10-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="a9c10-117"><dt>**Partición \_ de**</dt> <dt>0X07</dt> de IFS</span><span class="sxs-lookup"><span data-stu-id="a9c10-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="a9c10-118">Una partición IFS.</span><span class="sxs-lookup"><span data-stu-id="a9c10-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="a9c10-119"><dt>**Partición \_ de LDM**</dt> <dt>0x42</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="a9c10-120">Una partición del administrador de discos lógicos (LDM).</span><span class="sxs-lookup"><span data-stu-id="a9c10-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="a9c10-121"><dt>**Partición \_ de NTFT**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="a9c10-122">Una partición NTFT.</span><span class="sxs-lookup"><span data-stu-id="a9c10-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="a9c10-123"><dt>**Válido \_ NTFT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="a9c10-124">Una partición NTFT válida.</span><span class="sxs-lookup"><span data-stu-id="a9c10-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="a9c10-125">El bit alto de un código de tipo de partición indica que una partición forma parte de un reflejo de NTFT o una matriz seccionada.</span><span class="sxs-lookup"><span data-stu-id="a9c10-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a9c10-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9c10-126">Remarks</span></span>

<span data-ttu-id="a9c10-127">Hay varias macros que pueden ayudarle a detectar el tipo de partición: **IsContainerPartition**, **IsFTPartition** y **IsRecognizedPartition**.</span><span class="sxs-lookup"><span data-stu-id="a9c10-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="a9c10-128">Para obtener más información, vea WinIoCtl. h.</span><span class="sxs-lookup"><span data-stu-id="a9c10-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c10-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c10-129">Requirements</span></span>



| <span data-ttu-id="a9c10-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c10-130">Requirement</span></span> | <span data-ttu-id="a9c10-131">Value</span><span class="sxs-lookup"><span data-stu-id="a9c10-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c10-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9c10-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c10-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a9c10-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a9c10-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9c10-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c10-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9c10-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9c10-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9c10-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c10-137"><dt>WinIoCtl. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9c10-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c10-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9c10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c10-139">**información de partición \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="a9c10-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="a9c10-140">**\_MBR de información de partición \_**</span><span class="sxs-lookup"><span data-stu-id="a9c10-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="a9c10-141">**ESTABLECER \_ información de partición \_**</span><span class="sxs-lookup"><span data-stu-id="a9c10-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




