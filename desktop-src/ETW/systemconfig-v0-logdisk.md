---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk (clase)
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
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985934"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="aa374-103">SystemConfig \_ V0 \_ LogDisk (clase)</span><span class="sxs-lookup"><span data-stu-id="aa374-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="aa374-104">Esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="aa374-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="aa374-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="aa374-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa374-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa374-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="aa374-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa374-107">Members</span></span>

<span data-ttu-id="aa374-108">La clase **SystemConfig \_ V0 \_ LogDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aa374-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="aa374-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa374-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa374-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa374-110">Properties</span></span>

<span data-ttu-id="aa374-111">La clase **SystemConfig \_ V0 \_ LogDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa374-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa374-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="aa374-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-115">Calificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="aa374-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-116">Número de bytes de cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa374-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-117">**Númerodedisco corresponde**</span><span class="sxs-lookup"><span data-stu-id="aa374-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-120">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="aa374-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-121">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="aa374-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="aa374-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-123">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="aa374-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa374-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-125">Calificadores: **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="aa374-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-126">Letra de unidad del disco con el formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="aa374-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="aa374-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="aa374-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-130">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="aa374-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-131">Tipo de unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa374-131">Type of disk drive.</span></span> <span data-ttu-id="aa374-132">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="aa374-132">Possible values are:</span></span>



| <span data-ttu-id="aa374-133">Value</span><span class="sxs-lookup"><span data-stu-id="aa374-133">Value</span></span>                                                                        | <span data-ttu-id="aa374-134">Significado</span><span class="sxs-lookup"><span data-stu-id="aa374-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="aa374-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="aa374-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="aa374-136">Partición</span><span class="sxs-lookup"><span data-stu-id="aa374-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="aa374-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="aa374-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="aa374-138">Volumen</span><span class="sxs-lookup"><span data-stu-id="aa374-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="aa374-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="aa374-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="aa374-140">Partición extendida en varios discos</span><span class="sxs-lookup"><span data-stu-id="aa374-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aa374-141">**Systems**</span><span class="sxs-lookup"><span data-stu-id="aa374-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-142">Tipo de datos: **char16**</span><span class="sxs-lookup"><span data-stu-id="aa374-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-144">Calificadores: **WmiDataId** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="aa374-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-145">Sistema de archivos en el disco lógico, por ejemplo, NTFS.</span><span class="sxs-lookup"><span data-stu-id="aa374-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="aa374-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-147">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="aa374-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-149">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="aa374-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-150">Número de clústeres libres en el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="aa374-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-151">**Pad**</span><span class="sxs-lookup"><span data-stu-id="aa374-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-154">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="aa374-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-155">Reservado.</span><span class="sxs-lookup"><span data-stu-id="aa374-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="aa374-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-159">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="aa374-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-160">Número de índice de la partición.</span><span class="sxs-lookup"><span data-stu-id="aa374-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="aa374-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-162">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa374-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-164">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="aa374-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-165">Tamaño total de la partición, en bytes.</span><span class="sxs-lookup"><span data-stu-id="aa374-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="aa374-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-169">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="aa374-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-170">Número de sectores del volumen.</span><span class="sxs-lookup"><span data-stu-id="aa374-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-171">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="aa374-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-174">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="aa374-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-175">Tamaño de la unidad de disco, en bytes.</span><span class="sxs-lookup"><span data-stu-id="aa374-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="aa374-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-177">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa374-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-179">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="aa374-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-180">Desplazamiento inicial (en bytes) de la partición desde el principio del disco.</span><span class="sxs-lookup"><span data-stu-id="aa374-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="aa374-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-182">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="aa374-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-184">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="aa374-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-185">Número de clústeres usados y libres en el volumen.</span><span class="sxs-lookup"><span data-stu-id="aa374-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="aa374-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="aa374-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa374-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa374-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa374-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa374-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa374-189">Calificadores: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="aa374-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="aa374-190">Reservado.</span><span class="sxs-lookup"><span data-stu-id="aa374-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa374-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa374-191">Requirements</span></span>



| <span data-ttu-id="aa374-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa374-192">Requirement</span></span> | <span data-ttu-id="aa374-193">Value</span><span class="sxs-lookup"><span data-stu-id="aa374-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa374-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa374-194">Minimum supported client</span></span><br/> | <span data-ttu-id="aa374-195">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aa374-195">None supported</span></span><br/>                            |
| <span data-ttu-id="aa374-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa374-196">Minimum supported server</span></span><br/> | <span data-ttu-id="aa374-197">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa374-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa374-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa374-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa374-199">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="aa374-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




