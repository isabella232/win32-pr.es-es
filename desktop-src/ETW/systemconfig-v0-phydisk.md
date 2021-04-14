---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk (clase)
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
ms.openlocfilehash: 2f7eab1cec90630e25ee5968e5740f787acb8662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985931"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="49b51-103">SystemConfig \_ V0 \_ PhyDisk (clase)</span><span class="sxs-lookup"><span data-stu-id="49b51-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="49b51-104">Esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.</span><span class="sxs-lookup"><span data-stu-id="49b51-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="49b51-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="49b51-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b51-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49b51-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="49b51-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="49b51-107">Members</span></span>

<span data-ttu-id="49b51-108">La clase **SystemConfig \_ V0 \_ PhyDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="49b51-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="49b51-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49b51-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49b51-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49b51-110">Properties</span></span>

<span data-ttu-id="49b51-111">La clase **SystemConfig \_ V0 \_ PhyDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="49b51-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49b51-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="49b51-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-113">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="49b51-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="49b51-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-115">Calificadores: **WmiDataId** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="49b51-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-116">Letra de unidad de la unidad de arranque en el formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="49b51-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="49b51-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="49b51-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-120">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="49b51-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-121">Número de bytes de cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="49b51-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-122">**Cilindros**</span><span class="sxs-lookup"><span data-stu-id="49b51-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-123">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49b51-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-125">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="49b51-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-126">Número total de cilindros en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="49b51-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="49b51-127">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="49b51-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="49b51-128">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="49b51-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="49b51-129">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="49b51-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-130">**Númerodedisco corresponde**</span><span class="sxs-lookup"><span data-stu-id="49b51-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-133">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="49b51-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-134">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="49b51-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-135">**Le**</span><span class="sxs-lookup"><span data-stu-id="49b51-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-136">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="49b51-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="49b51-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-138">Calificadores: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="49b51-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-139">Nombre del fabricante de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="49b51-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="49b51-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-143">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="49b51-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-144">Número de particiones en esta unidad de disco físico que reconoce el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="49b51-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="49b51-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-148">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="49b51-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-149">Número de unidad lógica (LUN) SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="49b51-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="49b51-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-153">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="49b51-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-154">Número de bus SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="49b51-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="49b51-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-156">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-158">Calificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="49b51-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-159">Número SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="49b51-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="49b51-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-163">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="49b51-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-164">Contiene el número del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="49b51-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="49b51-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-166">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-168">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="49b51-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-169">Número de sectores de cada pista para esta unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="49b51-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="49b51-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49b51-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-173">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="49b51-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-174">Número de pistas en cada cilindro de la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="49b51-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="49b51-175">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="49b51-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="49b51-176">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="49b51-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="49b51-177">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="49b51-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="49b51-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="49b51-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b51-179">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="49b51-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49b51-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49b51-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b51-181">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="49b51-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="49b51-182">True si la memoria caché de escritura está habilitada.</span><span class="sxs-lookup"><span data-stu-id="49b51-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49b51-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49b51-183">Requirements</span></span>



| <span data-ttu-id="49b51-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="49b51-184">Requirement</span></span> | <span data-ttu-id="49b51-185">Value</span><span class="sxs-lookup"><span data-stu-id="49b51-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49b51-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49b51-186">Minimum supported client</span></span><br/> | <span data-ttu-id="49b51-187">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49b51-187">None supported</span></span><br/>                            |
| <span data-ttu-id="49b51-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49b51-188">Minimum supported server</span></span><br/> | <span data-ttu-id="49b51-189">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="49b51-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49b51-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="49b51-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b51-191">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="49b51-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




