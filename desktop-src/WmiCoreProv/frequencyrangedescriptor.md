---
description: Representa un contenedor para las características de un intervalo de frecuencias admitido.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: Clase FrequencyRangeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696367"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="4d580-103">Clase FrequencyRangeDescriptor</span><span class="sxs-lookup"><span data-stu-id="4d580-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="4d580-104">La clase WMI **FrequencyRangeDescriptor** representa un contenedor para las características de un intervalo de frecuencias admitido.</span><span class="sxs-lookup"><span data-stu-id="4d580-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="4d580-105">Las instancias de esta clase son elementos de la matriz **MonitorFreqRanges** en [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span><span class="sxs-lookup"><span data-stu-id="4d580-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d580-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d580-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="4d580-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d580-107">Members</span></span>

<span data-ttu-id="4d580-108">La clase **FrequencyRangeDescriptor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d580-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="4d580-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d580-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d580-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d580-110">Properties</span></span>

<span data-ttu-id="4d580-111">La clase **FrequencyRangeDescriptor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d580-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d580-112">**ActiveHeight**</span><span class="sxs-lookup"><span data-stu-id="4d580-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-115">Alto, en píxeles, de la imagen activa.</span><span class="sxs-lookup"><span data-stu-id="4d580-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-116">**ActiveWidth**</span><span class="sxs-lookup"><span data-stu-id="4d580-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-119">Ancho, en píxeles, de la imagen activa.</span><span class="sxs-lookup"><span data-stu-id="4d580-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="4d580-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-121">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-123">Tipo de restricción para el intervalo de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="4d580-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-124">**MaxHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="4d580-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-127">Denominador de sincronización horizontal máxima.</span><span class="sxs-lookup"><span data-stu-id="4d580-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-128">**MaxHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="4d580-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-131">Numerador de sincronización horizontal máximo en kilohercios (KHz).</span><span class="sxs-lookup"><span data-stu-id="4d580-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="4d580-132">**MaxPixelRate**</span><span class="sxs-lookup"><span data-stu-id="4d580-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-135">Velocidad de píxeles máxima en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="4d580-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="4d580-136">**MaxVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="4d580-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-139">Denominador de sincronización vertical máxima.</span><span class="sxs-lookup"><span data-stu-id="4d580-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-140">**MaxVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="4d580-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-143">Numerador de sincronización vertical máximo, en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="4d580-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="4d580-144">**MinHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="4d580-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-147">Denominador de sincronización horizontal mínima.</span><span class="sxs-lookup"><span data-stu-id="4d580-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-148">**MinHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="4d580-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-151">Numerador de sincronización horizontal mínimo en, kilohercios (KHz).</span><span class="sxs-lookup"><span data-stu-id="4d580-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="4d580-152">**MinVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="4d580-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-155">Denominador de sincronización vertical mínima.</span><span class="sxs-lookup"><span data-stu-id="4d580-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="4d580-156">**MinVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="4d580-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d580-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-159">Numerador de sincronización vertical mínimo, en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="4d580-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="4d580-160">**Origen**</span><span class="sxs-lookup"><span data-stu-id="4d580-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d580-161">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4d580-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4d580-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d580-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d580-163">Pescado.</span><span class="sxs-lookup"><span data-stu-id="4d580-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d580-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d580-164">Requirements</span></span>



| <span data-ttu-id="4d580-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d580-165">Requirement</span></span> | <span data-ttu-id="4d580-166">Value</span><span class="sxs-lookup"><span data-stu-id="4d580-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d580-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d580-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4d580-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d580-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d580-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d580-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4d580-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d580-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d580-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d580-171">Namespace</span></span><br/>                | <span data-ttu-id="4d580-172">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="4d580-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4d580-173">MOF</span><span class="sxs-lookup"><span data-stu-id="4d580-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d580-174"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d580-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d580-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d580-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d580-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d580-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d580-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d580-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d580-178">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="4d580-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




