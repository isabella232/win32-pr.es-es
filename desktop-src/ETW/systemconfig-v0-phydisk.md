---
description: 'SystemConfig_V0_PhyDisk clase : esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105963"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="08bec-103">Clase \_ PhyDisk SystemConfig V0 \_</span><span class="sxs-lookup"><span data-stu-id="08bec-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="08bec-104">Esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.</span><span class="sxs-lookup"><span data-stu-id="08bec-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="08bec-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="08bec-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bec-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08bec-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="08bec-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="08bec-107">Members</span></span>

<span data-ttu-id="08bec-108">La **clase \_ \_ PhyDisk SystemConfig V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="08bec-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="08bec-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08bec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08bec-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08bec-110">Properties</span></span>

<span data-ttu-id="08bec-111">La **clase \_ \_ PhyDisk SystemConfig V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="08bec-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08bec-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="08bec-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-113">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="08bec-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="08bec-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-115">Calificadores: **WmiDataId** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="08bec-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-116">Letra de unidad de la unidad de arranque con el formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="08bec-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="08bec-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="08bec-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-118">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-120">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="08bec-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-121">Número de bytes en cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="08bec-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-122">**Cilindros**</span><span class="sxs-lookup"><span data-stu-id="08bec-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-123">Tipo de datos: **uint64**</span><span class="sxs-lookup"><span data-stu-id="08bec-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-125">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="08bec-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-126">Número total de cilindros en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="08bec-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="08bec-127">Nota: El valor de esta propiedad se obtiene a través de funciones extendidas de interrupción del BIOS 13 horas.</span><span class="sxs-lookup"><span data-stu-id="08bec-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="08bec-128">El valor puede ser inexacto si la unidad usa un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="08bec-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="08bec-129">Consulte al fabricante para obtener especificaciones precisas de la unidad.</span><span class="sxs-lookup"><span data-stu-id="08bec-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="08bec-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-131">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-133">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="08bec-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-134">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="08bec-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-135">**Fabricante**</span><span class="sxs-lookup"><span data-stu-id="08bec-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-136">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="08bec-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="08bec-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-138">Calificadores: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="08bec-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-139">Nombre del fabricante de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="08bec-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="08bec-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-141">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-143">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="08bec-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-144">Número de particiones en esta unidad de disco físico que reconoce el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="08bec-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="08bec-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-146">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-148">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="08bec-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-149">Número de unidad lógica (LUN) SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="08bec-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="08bec-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-151">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-153">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="08bec-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-154">Número de bus SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="08bec-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="08bec-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-156">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-158">Calificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="08bec-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-159">Número SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="08bec-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="08bec-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-161">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-163">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="08bec-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-164">Contiene el número del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="08bec-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="08bec-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-166">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-168">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="08bec-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-169">Número de sectores de cada pista para esta unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="08bec-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="08bec-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-171">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="08bec-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-173">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="08bec-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-174">Número de pistas de cada cilindro en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="08bec-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="08bec-175">Nota: El valor de esta propiedad se obtiene a través de funciones extendidas de interrupción del BIOS 13 horas.</span><span class="sxs-lookup"><span data-stu-id="08bec-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="08bec-176">El valor puede ser inexacto si la unidad usa un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="08bec-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="08bec-177">Consulte al fabricante para obtener especificaciones precisas de la unidad.</span><span class="sxs-lookup"><span data-stu-id="08bec-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="08bec-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="08bec-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bec-179">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08bec-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08bec-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08bec-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bec-181">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="08bec-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="08bec-182">True si la caché de escritura está habilitada.</span><span class="sxs-lookup"><span data-stu-id="08bec-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08bec-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08bec-183">Requirements</span></span>



| <span data-ttu-id="08bec-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bec-184">Requirement</span></span> | <span data-ttu-id="08bec-185">Valor</span><span class="sxs-lookup"><span data-stu-id="08bec-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="08bec-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08bec-186">Minimum supported client</span></span><br/> | <span data-ttu-id="08bec-187">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="08bec-187">None supported</span></span><br/>                            |
| <span data-ttu-id="08bec-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08bec-188">Minimum supported server</span></span><br/> | <span data-ttu-id="08bec-189">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="08bec-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08bec-190">Consulte también</span><span class="sxs-lookup"><span data-stu-id="08bec-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bec-191">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="08bec-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




