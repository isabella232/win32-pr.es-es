---
description: 'SystemConfig_LogDisk clase : esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.'
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: SystemConfig_LogDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106113"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="0903d-103">Clase SystemConfig \_ LogDisk</span><span class="sxs-lookup"><span data-stu-id="0903d-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="0903d-104">Esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="0903d-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="0903d-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="0903d-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0903d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0903d-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="0903d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0903d-107">Members</span></span>

<span data-ttu-id="0903d-108">La **clase SystemConfig \_ LogDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0903d-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="0903d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0903d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0903d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0903d-110">Properties</span></span>

<span data-ttu-id="0903d-111">La **clase SystemConfig \_ LogDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0903d-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0903d-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="0903d-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-113">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-115">Calificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="0903d-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-116">Número de bytes en cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="0903d-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="0903d-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-118">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-120">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="0903d-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-121">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="0903d-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="0903d-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-123">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="0903d-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="0903d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-125">Calificadores: **WmiDataId** (6), **Max** (4), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="0903d-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="0903d-126">Letra de unidad del disco con el formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="0903d-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="0903d-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="0903d-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-128">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-130">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="0903d-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-131">Tipo de unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="0903d-131">Type of disk drive.</span></span> <span data-ttu-id="0903d-132">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="0903d-132">Possible values are:</span></span>



| <span data-ttu-id="0903d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0903d-133">Value</span></span>                                                                        | <span data-ttu-id="0903d-134">Significado</span><span class="sxs-lookup"><span data-stu-id="0903d-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="0903d-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0903d-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0903d-136">Partition</span><span class="sxs-lookup"><span data-stu-id="0903d-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="0903d-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0903d-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0903d-138">Volumen</span><span class="sxs-lookup"><span data-stu-id="0903d-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="0903d-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0903d-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0903d-140">Partición extendida en varios discos</span><span class="sxs-lookup"><span data-stu-id="0903d-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0903d-141">**Filesystem**</span><span class="sxs-lookup"><span data-stu-id="0903d-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-142">Tipo de datos: **char16**</span><span class="sxs-lookup"><span data-stu-id="0903d-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-144">Calificadores: **WmiDataId** (14), **Max** (16), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="0903d-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="0903d-145">Sistema de archivos en el disco lógico, por ejemplo, NTFS.</span><span class="sxs-lookup"><span data-stu-id="0903d-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="0903d-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-147">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="0903d-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-149">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="0903d-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-150">Número de clústeres libres en el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="0903d-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="0903d-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-152">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-154">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="0903d-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-155">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0903d-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="0903d-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-157">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-159">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="0903d-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-160">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0903d-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="0903d-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-162">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-164">Calificadores: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="0903d-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-165">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0903d-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="0903d-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-167">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-169">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="0903d-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-170">Número de índice de la partición.</span><span class="sxs-lookup"><span data-stu-id="0903d-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="0903d-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-172">Tipo de datos: **uint64**</span><span class="sxs-lookup"><span data-stu-id="0903d-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-174">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="0903d-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-175">Tamaño total de la partición, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0903d-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="0903d-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-177">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-179">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="0903d-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-180">Número de sectores del volumen.</span><span class="sxs-lookup"><span data-stu-id="0903d-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-181">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="0903d-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-182">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-184">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="0903d-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-185">Tamaño de la unidad de disco, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0903d-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="0903d-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-187">Tipo de datos: **uint64**</span><span class="sxs-lookup"><span data-stu-id="0903d-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-189">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="0903d-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-190">Desplazamiento inicial (en bytes) de la partición desde el principio del disco.</span><span class="sxs-lookup"><span data-stu-id="0903d-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="0903d-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-192">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="0903d-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-194">Calificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="0903d-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-195">Número de clústeres usados y libres en el volumen.</span><span class="sxs-lookup"><span data-stu-id="0903d-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="0903d-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="0903d-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0903d-197">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0903d-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0903d-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0903d-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0903d-199">Calificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="0903d-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="0903d-200">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0903d-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0903d-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0903d-201">Requirements</span></span>



| <span data-ttu-id="0903d-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="0903d-202">Requirement</span></span> | <span data-ttu-id="0903d-203">Valor</span><span class="sxs-lookup"><span data-stu-id="0903d-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0903d-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0903d-204">Minimum supported client</span></span><br/> | <span data-ttu-id="0903d-205">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="0903d-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0903d-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0903d-206">Minimum supported server</span></span><br/> | <span data-ttu-id="0903d-207">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0903d-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0903d-208">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0903d-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0903d-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="0903d-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




