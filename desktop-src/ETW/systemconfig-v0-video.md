---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de vídeo.
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: b840e3c06e74f8acbd1e43550559385e78c9a638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985098"
---
# <a name="systemconfig_v0_video-class"></a><span data-ttu-id="11b2e-103">\_Clase de \_ vídeo SystemConfig v0</span><span class="sxs-lookup"><span data-stu-id="11b2e-103">SystemConfig\_V0\_Video class</span></span>

<span data-ttu-id="11b2e-104">Esta clase es la clase de tipo de evento para los eventos de configuración de vídeo.</span><span class="sxs-lookup"><span data-stu-id="11b2e-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="11b2e-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="11b2e-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b2e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11b2e-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="11b2e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="11b2e-107">Members</span></span>

<span data-ttu-id="11b2e-108">La clase de **\_ \_ vídeo SystemConfig V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="11b2e-108">The **SystemConfig\_V0\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="11b2e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11b2e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11b2e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11b2e-110">Properties</span></span>

<span data-ttu-id="11b2e-111">La clase de **\_ \_ vídeo SystemConfig V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="11b2e-111">The **SystemConfig\_V0\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11b2e-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="11b2e-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-113">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="11b2e-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-115">Calificadores: **WmiDataId** (8), **máx** . (256)</span><span class="sxs-lookup"><span data-stu-id="11b2e-115">Qualifiers: **WmiDataId** (8), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-116">Nombre o Descripción del adaptador.</span><span class="sxs-lookup"><span data-stu-id="11b2e-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="11b2e-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-118">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="11b2e-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-120">Calificadores: **WmiDataId** (9), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="11b2e-120">Qualifiers: **WmiDataId** (9), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-121">Nombre del BIOS del adaptador.</span><span class="sxs-lookup"><span data-stu-id="11b2e-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="11b2e-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11b2e-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-125">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="11b2e-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-126">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="11b2e-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="11b2e-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-128">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="11b2e-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-130">Calificadores: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="11b2e-130">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-131">Nombre del chip del adaptador.</span><span class="sxs-lookup"><span data-stu-id="11b2e-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="11b2e-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-133">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="11b2e-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-135">Calificadores: **WmiDataId** (7), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="11b2e-135">Qualifiers: **WmiDataId** (7), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-136">Nombre del chip del convertidor digital a analógico (DAC) del adaptador.</span><span class="sxs-lookup"><span data-stu-id="11b2e-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="11b2e-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-138">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="11b2e-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-140">Calificadores: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="11b2e-140">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-141">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="11b2e-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="11b2e-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11b2e-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-145">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="11b2e-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-146">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="11b2e-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="11b2e-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11b2e-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-150">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="11b2e-150">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-151">Marcas de estado de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11b2e-151">Device state flags.</span></span> <span data-ttu-id="11b2e-152">Puede ser cualquier combinación razonable de lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="11b2e-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="11b2e-153">Value</span><span class="sxs-lookup"><span data-stu-id="11b2e-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="11b2e-154">Significado</span><span class="sxs-lookup"><span data-stu-id="11b2e-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="11b2e-155"><dt>**Mostrar \_ DISPOSITIVO \_ conectado \_ al \_ escritorio**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="11b2e-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="11b2e-156">El dispositivo es parte del escritorio.</span><span class="sxs-lookup"><span data-stu-id="11b2e-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="11b2e-157"><dt>**Mostrar \_ \_ \_ Controlador de creación de reflejo de dispositivos**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="11b2e-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="11b2e-158">Representa un pseudo dispositivo que se usa para reflejar el dibujo de la aplicación para conectarse a un equipo remoto o a otros fines.</span><span class="sxs-lookup"><span data-stu-id="11b2e-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="11b2e-159">Un pseudo monitor invisible está asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11b2e-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="11b2e-160">Por ejemplo, NetMeeting lo usa.</span><span class="sxs-lookup"><span data-stu-id="11b2e-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="11b2e-161"><dt>**Mostrar \_ DISPOSITIVO \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="11b2e-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="11b2e-162">El dispositivo tiene más modos de visualización que los dispositivos de salida que admiten.</span><span class="sxs-lookup"><span data-stu-id="11b2e-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="11b2e-163"><dt>**Mostrar \_ Dispositivo \_ primario \_ de dispositivo**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="11b2e-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="11b2e-164">El escritorio principal está en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11b2e-164">The primary desktop is on the device.</span></span> <span data-ttu-id="11b2e-165">Para un sistema con una sola tarjeta de presentación, siempre se establece.</span><span class="sxs-lookup"><span data-stu-id="11b2e-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="11b2e-166">Para un sistema con varias tarjetas de presentación, solo un dispositivo puede tener este conjunto.</span><span class="sxs-lookup"><span data-stu-id="11b2e-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="11b2e-167"><dt>**Mostrar \_ DISPOSITIVO \_ extraíble**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="11b2e-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="11b2e-168">El dispositivo es extraíble; no puede ser la pantalla principal.</span><span class="sxs-lookup"><span data-stu-id="11b2e-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="11b2e-169"><dt>**Mostrar \_ DISPOSITIVO \_ VGA \_ compatible**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="11b2e-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="11b2e-170">El dispositivo es compatible con VGA.</span><span class="sxs-lookup"><span data-stu-id="11b2e-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="11b2e-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="11b2e-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11b2e-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-174">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="11b2e-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-175">Frecuencia de actualización actual, en hercios.</span><span class="sxs-lookup"><span data-stu-id="11b2e-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="11b2e-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11b2e-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-179">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="11b2e-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-180">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="11b2e-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="11b2e-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="11b2e-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b2e-182">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11b2e-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b2e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b2e-184">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="11b2e-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="11b2e-185">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="11b2e-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11b2e-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11b2e-186">Requirements</span></span>



| <span data-ttu-id="11b2e-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="11b2e-187">Requirement</span></span> | <span data-ttu-id="11b2e-188">Value</span><span class="sxs-lookup"><span data-stu-id="11b2e-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11b2e-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11b2e-189">Minimum supported client</span></span><br/> | <span data-ttu-id="11b2e-190">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="11b2e-190">None supported</span></span><br/>                            |
| <span data-ttu-id="11b2e-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11b2e-191">Minimum supported server</span></span><br/> | <span data-ttu-id="11b2e-192">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="11b2e-192">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11b2e-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="11b2e-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b2e-194">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="11b2e-194">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




