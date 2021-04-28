---
description: 'SystemConfig_Video clase : esta clase es la clase de tipo de evento para eventos de configuración de vídeo.'
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716194eb9ceb67b609f886482393795eaef2ef09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105903"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="f22c7-103">Clase SystemConfig \_ Video</span><span class="sxs-lookup"><span data-stu-id="f22c7-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="f22c7-104">Esta clase es la clase de tipo de evento para eventos de configuración de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f22c7-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="f22c7-105">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="f22c7-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22c7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f22c7-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
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

## <a name="members"></a><span data-ttu-id="f22c7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f22c7-107">Members</span></span>

<span data-ttu-id="f22c7-108">La **clase SystemConfig \_ Video** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f22c7-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="f22c7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f22c7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f22c7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f22c7-110">Properties</span></span>

<span data-ttu-id="f22c7-111">La **clase SystemConfig \_ Video** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f22c7-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f22c7-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="f22c7-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-113">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="f22c7-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-115">Calificadores: **WmiDataId** (8), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="f22c7-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-116">Nombre o descripción del adaptador.</span><span class="sxs-lookup"><span data-stu-id="f22c7-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="f22c7-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-118">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="f22c7-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-120">Calificadores: **WmiDataId** (9), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="f22c7-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-121">Nombre del BIOS del adaptador.</span><span class="sxs-lookup"><span data-stu-id="f22c7-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="f22c7-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-123">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22c7-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-125">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="f22c7-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-126">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="f22c7-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="f22c7-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-128">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="f22c7-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-130">Calificadores: **WmiDataId** (6), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="f22c7-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-131">Nombre del chip del adaptador.</span><span class="sxs-lookup"><span data-stu-id="f22c7-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="f22c7-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-133">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="f22c7-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-135">Calificadores: **WmiDataId** (7), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="f22c7-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-136">Nombre del chip del convertidor digital a analógico (DAC) del adaptador.</span><span class="sxs-lookup"><span data-stu-id="f22c7-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="f22c7-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-138">Tipo de datos: **matriz char16**</span><span class="sxs-lookup"><span data-stu-id="f22c7-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-140">Calificadores: **WmiDataId** (10), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="f22c7-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-141">Dirección u otra información de identificación para dar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f22c7-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="f22c7-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-143">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22c7-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-145">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="f22c7-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-146">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f22c7-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="f22c7-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-148">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22c7-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-150">Calificadores: **WmiDataId** (11), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="f22c7-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-151">Marcas de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f22c7-151">Device state flags.</span></span> <span data-ttu-id="f22c7-152">Puede ser cualquier combinación razonable de lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f22c7-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="f22c7-153">Valor</span><span class="sxs-lookup"><span data-stu-id="f22c7-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="f22c7-154">Significado</span><span class="sxs-lookup"><span data-stu-id="f22c7-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="f22c7-155"><dt>**DISPLAY \_ DISPOSITIVO \_ CONECTADO \_ AL \_ ESCRITORIO**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c7-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="f22c7-156">El dispositivo forma parte del escritorio.</span><span class="sxs-lookup"><span data-stu-id="f22c7-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="f22c7-157"><dt>**DISPLAY \_ CONTROLADOR \_ DE CREACIÓN DE REFLEJO \_ DEL**</dt> <dt>DISPOSITIVO 8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c7-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="f22c7-158">Representa un pseudodispositivo que se usa para reflejar el dibujo de la aplicación para conectarse a un equipo remoto u otros propósitos.</span><span class="sxs-lookup"><span data-stu-id="f22c7-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="f22c7-159">Un pseudo monitor invisible está asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f22c7-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="f22c7-160">Por ejemplo, NetMeeting lo usa.</span><span class="sxs-lookup"><span data-stu-id="f22c7-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="f22c7-161"><dt>**DISPLAY \_ MODOS \_ DE DISPOSITIVORUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c7-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="f22c7-162">El dispositivo tiene más modos de presentación de los que admiten sus dispositivos de salida.</span><span class="sxs-lookup"><span data-stu-id="f22c7-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="f22c7-163"><dt>**DISPLAY \_ DISPOSITIVO \_ PRINCIPAL \_ DISPOSITIVO**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c7-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="f22c7-164">El escritorio principal está en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f22c7-164">The primary desktop is on the device.</span></span> <span data-ttu-id="f22c7-165">Para un sistema con una sola tarjeta de presentación, esto siempre se establece.</span><span class="sxs-lookup"><span data-stu-id="f22c7-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="f22c7-166">Para un sistema con varias tarjetas de presentación, solo un dispositivo puede tener este conjunto.</span><span class="sxs-lookup"><span data-stu-id="f22c7-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="f22c7-167"><dt>**DISPLAY \_ DISPOSITIVO \_ EXTRAÍBLE**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c7-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="f22c7-168">El dispositivo es extraíble; no puede ser la pantalla principal.</span><span class="sxs-lookup"><span data-stu-id="f22c7-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="f22c7-169"><dt>**DISPLAY \_ COMPATIBLE \_ CON \_ DEVICE VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c7-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="f22c7-170">El dispositivo es compatible con VGA.</span><span class="sxs-lookup"><span data-stu-id="f22c7-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="f22c7-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="f22c7-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-172">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22c7-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-174">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="f22c7-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-175">Frecuencia de actualización actual, en hertz.</span><span class="sxs-lookup"><span data-stu-id="f22c7-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="f22c7-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-177">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22c7-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-179">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="f22c7-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-180">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="f22c7-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f22c7-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="f22c7-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22c7-182">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22c7-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22c7-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22c7-184">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="f22c7-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="f22c7-185">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="f22c7-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f22c7-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f22c7-186">Requirements</span></span>



| <span data-ttu-id="f22c7-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="f22c7-187">Requirement</span></span> | <span data-ttu-id="f22c7-188">Valor</span><span class="sxs-lookup"><span data-stu-id="f22c7-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f22c7-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f22c7-189">Minimum supported client</span></span><br/> | <span data-ttu-id="f22c7-190">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="f22c7-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f22c7-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f22c7-191">Minimum supported server</span></span><br/> | <span data-ttu-id="f22c7-192">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f22c7-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f22c7-193">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f22c7-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22c7-194">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f22c7-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




