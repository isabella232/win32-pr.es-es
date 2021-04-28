---
description: 'SystemConfig_PhyDisk clase : esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.'
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106103"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="84c75-103">Clase SystemConfig \_ PhyDisk</span><span class="sxs-lookup"><span data-stu-id="84c75-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="84c75-104">Esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.</span><span class="sxs-lookup"><span data-stu-id="84c75-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="84c75-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="84c75-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c75-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84c75-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="84c75-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="84c75-107">Members</span></span>

<span data-ttu-id="84c75-108">La **clase SystemConfig \_ PhyDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="84c75-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="84c75-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84c75-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84c75-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84c75-110">Properties</span></span>

<span data-ttu-id="84c75-111">La **clase SystemConfig \_ PhyDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="84c75-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84c75-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="84c75-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-113">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="84c75-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="84c75-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-115">Calificadores: **WmiDataId** (14), **Max** (3), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="84c75-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="84c75-116">Letra de unidad de la unidad de arranque con el formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="84c75-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="84c75-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="84c75-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-118">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-120">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="84c75-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-121">Número de bytes en cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="84c75-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-122">**Cilindros**</span><span class="sxs-lookup"><span data-stu-id="84c75-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-123">Tipo de datos: **uint64**</span><span class="sxs-lookup"><span data-stu-id="84c75-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-125">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="84c75-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-126">Número total de cilindros en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="84c75-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="84c75-127">Nota: El valor de esta propiedad se obtiene a través de funciones extendidas de interrupción del BIOS 13 horas.</span><span class="sxs-lookup"><span data-stu-id="84c75-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="84c75-128">El valor puede ser inexacto si la unidad usa un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="84c75-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="84c75-129">Consulte al fabricante para obtener especificaciones precisas de la unidad.</span><span class="sxs-lookup"><span data-stu-id="84c75-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="84c75-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-131">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-133">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="84c75-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-134">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="84c75-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-135">**Fabricante**</span><span class="sxs-lookup"><span data-stu-id="84c75-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-136">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="84c75-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="84c75-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-138">Calificadores: **WmiDataId** (10), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="84c75-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="84c75-139">Nombre del fabricante de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="84c75-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-140">**Pad**</span><span class="sxs-lookup"><span data-stu-id="84c75-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-141">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="84c75-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-143">Calificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="84c75-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-144">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="84c75-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="84c75-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-146">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-148">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="84c75-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-149">Número de particiones en esta unidad de disco físico que reconoce el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="84c75-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="84c75-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-151">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-153">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="84c75-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-154">Número de unidad lógica (LUN) SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="84c75-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="84c75-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-156">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-158">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="84c75-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-159">Número de bus SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="84c75-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="84c75-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-161">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-163">Calificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="84c75-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-164">Número SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="84c75-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="84c75-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-166">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-168">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="84c75-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-169">Contiene el número del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="84c75-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="84c75-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-171">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-173">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="84c75-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-174">Número de sectores de cada pista para esta unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="84c75-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-175">**Repuesto**</span><span class="sxs-lookup"><span data-stu-id="84c75-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-176">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="84c75-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="84c75-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-178">Calificadores: **WmiDataId** (15), **Max** (2), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="84c75-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="84c75-179">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="84c75-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="84c75-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-181">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="84c75-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-183">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="84c75-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-184">Número de pistas de cada cilindro en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="84c75-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="84c75-185">Nota: El valor de esta propiedad se obtiene a través de funciones extendidas de interrupción de BIOS de 13 horas.</span><span class="sxs-lookup"><span data-stu-id="84c75-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="84c75-186">El valor puede ser inexacto si la unidad usa un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="84c75-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="84c75-187">Consulte al fabricante para obtener especificaciones precisas de la unidad.</span><span class="sxs-lookup"><span data-stu-id="84c75-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="84c75-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="84c75-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c75-189">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="84c75-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84c75-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84c75-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c75-191">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="84c75-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="84c75-192">True si la caché de escritura está habilitada.</span><span class="sxs-lookup"><span data-stu-id="84c75-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84c75-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84c75-193">Requirements</span></span>



| <span data-ttu-id="84c75-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c75-194">Requirement</span></span> | <span data-ttu-id="84c75-195">Valor</span><span class="sxs-lookup"><span data-stu-id="84c75-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84c75-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84c75-196">Minimum supported client</span></span><br/> | <span data-ttu-id="84c75-197">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="84c75-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84c75-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84c75-198">Minimum supported server</span></span><br/> | <span data-ttu-id="84c75-199">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="84c75-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84c75-200">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84c75-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c75-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="84c75-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




