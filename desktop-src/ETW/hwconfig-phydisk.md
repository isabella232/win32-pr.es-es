---
description: La \_ clase HWConfig PhyDisk es la clase de tipo de evento para los eventos de configuración de disco físico. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984487"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="4ace5-104">HWConfig \_ PhyDisk (clase)</span><span class="sxs-lookup"><span data-stu-id="4ace5-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="4ace5-105">La clase **HWConfig \_ PhyDisk** es la clase de tipo de evento para los eventos de configuración de disco físico.</span><span class="sxs-lookup"><span data-stu-id="4ace5-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="4ace5-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="4ace5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ace5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ace5-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="4ace5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ace5-108">Members</span></span>

<span data-ttu-id="4ace5-109">La clase **HWConfig \_ PhyDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4ace5-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="4ace5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ace5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ace5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ace5-111">Properties</span></span>

<span data-ttu-id="4ace5-112">La clase **HWConfig \_ PhyDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4ace5-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ace5-113">BytesPerSector</span><span class="sxs-lookup"><span data-stu-id="4ace5-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-116">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="4ace5-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-117">Número de bytes de cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="4ace5-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-118">Cilindros</span><span class="sxs-lookup"><span data-stu-id="4ace5-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-119">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ace5-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-121">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="4ace5-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-122">Número total de cilindros en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="4ace5-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="4ace5-123">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4ace5-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="4ace5-124">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="4ace5-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="4ace5-125">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="4ace5-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-126">Númerodedisco corresponde</span><span class="sxs-lookup"><span data-stu-id="4ace5-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-127">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-129">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="4ace5-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-130">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="4ace5-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-131">Fabricante</span><span class="sxs-lookup"><span data-stu-id="4ace5-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ace5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-134">Calificadores: WmiDataId (10), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="4ace5-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-135">Nombre del fabricante de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="4ace5-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-136">SCSILun</span><span class="sxs-lookup"><span data-stu-id="4ace5-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-139">Calificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="4ace5-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-140">Número de unidad lógica (LUN) SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="4ace5-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-141">SCSIPath</span><span class="sxs-lookup"><span data-stu-id="4ace5-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-144">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="4ace5-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-145">Número de bus SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="4ace5-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="4ace5-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-149">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="4ace5-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-150">Número SCSI del adaptador SCSI.</span><span class="sxs-lookup"><span data-stu-id="4ace5-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-151">SCSITarget</span><span class="sxs-lookup"><span data-stu-id="4ace5-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-154">Calificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="4ace5-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-155">Contiene el número del dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="4ace5-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-156">SectorsPerTrack</span><span class="sxs-lookup"><span data-stu-id="4ace5-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-159">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="4ace5-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-160">Número de sectores de cada pista para esta unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="4ace5-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4ace5-161">TracksPerCylinder</span><span class="sxs-lookup"><span data-stu-id="4ace5-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ace5-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ace5-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ace5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ace5-164">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="4ace5-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="4ace5-165">Número de pistas en cada cilindro de la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="4ace5-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="4ace5-166">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4ace5-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="4ace5-167">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="4ace5-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="4ace5-168">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="4ace5-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ace5-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ace5-169">Requirements</span></span>



| <span data-ttu-id="4ace5-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ace5-170">Requirement</span></span> | <span data-ttu-id="4ace5-171">Value</span><span class="sxs-lookup"><span data-stu-id="4ace5-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="4ace5-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ace5-172">Minimum supported client</span></span><br/> | <span data-ttu-id="4ace5-173">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4ace5-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4ace5-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ace5-174">Minimum supported server</span></span><br/> | <span data-ttu-id="4ace5-175">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4ace5-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="4ace5-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ace5-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ace5-177">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="4ace5-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




