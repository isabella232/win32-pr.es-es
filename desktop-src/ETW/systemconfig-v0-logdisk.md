---
description: 'SystemConfig_V0_LogDisk clase : esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.'
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb0ad959d637a38a03b77bd8d7a812ff608ddc04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105983"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="7ec50-103">Clase LogDisk SystemConfig \_ V0 \_</span><span class="sxs-lookup"><span data-stu-id="7ec50-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="7ec50-104">Esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="7ec50-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="7ec50-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="7ec50-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec50-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ec50-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="7ec50-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ec50-107">Members</span></span>

<span data-ttu-id="7ec50-108">La **clase \_ \_ LogDisk SystemConfig V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ec50-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="7ec50-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ec50-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ec50-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ec50-110">Properties</span></span>

<span data-ttu-id="7ec50-111">La **clase \_ \_ LogDisk SystemConfig V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ec50-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ec50-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="7ec50-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-113">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-115">Calificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="7ec50-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-116">Número de bytes en cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="7ec50-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="7ec50-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-118">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-120">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="7ec50-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-121">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="7ec50-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="7ec50-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-123">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="7ec50-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-125">Calificadores: **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="7ec50-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-126">Letra de unidad del disco con el formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="7ec50-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="7ec50-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-128">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-130">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="7ec50-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-131">Tipo de unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="7ec50-131">Type of disk drive.</span></span> <span data-ttu-id="7ec50-132">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="7ec50-132">Possible values are:</span></span>



| <span data-ttu-id="7ec50-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7ec50-133">Value</span></span>                                                                        | <span data-ttu-id="7ec50-134">Significado</span><span class="sxs-lookup"><span data-stu-id="7ec50-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7ec50-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7ec50-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7ec50-136">Partition</span><span class="sxs-lookup"><span data-stu-id="7ec50-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="7ec50-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7ec50-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7ec50-138">Volumen</span><span class="sxs-lookup"><span data-stu-id="7ec50-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="7ec50-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7ec50-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7ec50-140">Partición extendida en varios discos</span><span class="sxs-lookup"><span data-stu-id="7ec50-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7ec50-141">**Filesystem**</span><span class="sxs-lookup"><span data-stu-id="7ec50-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-142">Tipo de datos: **char16**</span><span class="sxs-lookup"><span data-stu-id="7ec50-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-144">Calificadores: **WmiDataId** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="7ec50-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-145">Sistema de archivos en el disco lógico, por ejemplo, NTFS.</span><span class="sxs-lookup"><span data-stu-id="7ec50-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="7ec50-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-147">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="7ec50-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-149">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="7ec50-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-150">Número de clústeres libres en el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="7ec50-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-151">**Pad**</span><span class="sxs-lookup"><span data-stu-id="7ec50-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-152">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-154">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="7ec50-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-155">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7ec50-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="7ec50-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-157">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-159">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="7ec50-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-160">Número de índice de la partición.</span><span class="sxs-lookup"><span data-stu-id="7ec50-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="7ec50-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-162">Tipo de datos: **uint64**</span><span class="sxs-lookup"><span data-stu-id="7ec50-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-164">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="7ec50-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-165">Tamaño total de la partición, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7ec50-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="7ec50-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-167">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-169">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="7ec50-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-170">Número de sectores del volumen.</span><span class="sxs-lookup"><span data-stu-id="7ec50-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-171">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="7ec50-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-172">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-174">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="7ec50-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-175">Tamaño de la unidad de disco, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7ec50-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="7ec50-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-177">Tipo de datos: **uint64**</span><span class="sxs-lookup"><span data-stu-id="7ec50-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-179">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="7ec50-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-180">Desplazamiento inicial (en bytes) de la partición desde el principio del disco.</span><span class="sxs-lookup"><span data-stu-id="7ec50-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="7ec50-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-182">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="7ec50-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-184">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="7ec50-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-185">Número de clústeres usados y libres en el volumen.</span><span class="sxs-lookup"><span data-stu-id="7ec50-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="7ec50-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="7ec50-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec50-187">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7ec50-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec50-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ec50-189">Calificadores: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="7ec50-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="7ec50-190">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7ec50-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ec50-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ec50-191">Requirements</span></span>



| <span data-ttu-id="7ec50-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec50-192">Requirement</span></span> | <span data-ttu-id="7ec50-193">Valor</span><span class="sxs-lookup"><span data-stu-id="7ec50-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ec50-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ec50-194">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec50-195">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7ec50-195">None supported</span></span><br/>                            |
| <span data-ttu-id="7ec50-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ec50-196">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec50-197">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ec50-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ec50-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ec50-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec50-199">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="7ec50-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




