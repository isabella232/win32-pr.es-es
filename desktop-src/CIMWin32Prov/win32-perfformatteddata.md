---
description: Una clase base abstracta para las clases de datos calculadas preinstaladas.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000752"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="0420d-103">\_Clase Win32 PerfFormattedData</span><span class="sxs-lookup"><span data-stu-id="0420d-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="0420d-104">Una clase base abstracta para las clases de datos calculadas preinstaladas.</span><span class="sxs-lookup"><span data-stu-id="0420d-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="0420d-105">Un ejemplo de este tipo de clase es [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="0420d-106">Estas clases contienen valores calculados proporcionados por el [proveedor de datos de rendimiento con formato](../wmisdk/formatted-performance-data-provider.md)de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0420d-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="0420d-107">La siguiente sintaxis se simplifica desde el código MOF y muestra todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0420d-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0420d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0420d-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="0420d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0420d-109">Members</span></span>

<span data-ttu-id="0420d-110">La **clase \_ PerfFormattedData de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0420d-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="0420d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0420d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0420d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0420d-112">Properties</span></span>

<span data-ttu-id="0420d-113">La **clase \_ PerfFormattedData de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0420d-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0420d-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0420d-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0420d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0420d-117">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0420d-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0420d-118">Breve descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="0420d-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="0420d-119">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0420d-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0420d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-123">Descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="0420d-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="0420d-124">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-125">**Frequency ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="0420d-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0420d-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-128">Frecuencia en TICs por segundo de la propiedad **de \_ objeto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="0420d-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="0420d-129">Cuando se subclase, el proveedor define esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0420d-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="0420d-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0420d-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="0420d-131">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-132">**Frecuencia \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="0420d-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0420d-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-135">Frecuencia en TICs por segundo de la propiedad **\_ PerfTime** de la frecuencia.</span><span class="sxs-lookup"><span data-stu-id="0420d-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="0420d-136">Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.</span><span class="sxs-lookup"><span data-stu-id="0420d-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="0420d-137">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0420d-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="0420d-138">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-139">**Frecuencia \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="0420d-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-140">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0420d-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-142">Frecuencia en TICs por segundo de la propiedad **timestamp \_ Sys100NS** (10 millones).</span><span class="sxs-lookup"><span data-stu-id="0420d-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="0420d-143">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0420d-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="0420d-144">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-145">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0420d-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0420d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0420d-148">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0420d-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0420d-149">Etiqueta por la que se conoce la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="0420d-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="0420d-150">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="0420d-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0420d-151">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-152">**Timestamp ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="0420d-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-153">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0420d-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-155">Marca de tiempo definida por el objeto.</span><span class="sxs-lookup"><span data-stu-id="0420d-155">Object-defined timestamp.</span></span> <span data-ttu-id="0420d-156">El proveedor define su propiedad.</span><span class="sxs-lookup"><span data-stu-id="0420d-156">The provider defines his property.</span></span>

<span data-ttu-id="0420d-157">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0420d-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="0420d-158">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-159">**Marca de tiempo \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="0420d-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-160">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0420d-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-162">Marca de tiempo de contador de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0420d-162">High Performance counter timestamp.</span></span> <span data-ttu-id="0420d-163">Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.</span><span class="sxs-lookup"><span data-stu-id="0420d-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="0420d-164">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0420d-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="0420d-165">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="0420d-166">**Marca de tiempo \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="0420d-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0420d-167">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0420d-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0420d-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0420d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0420d-169">Valor de marca de tiempo en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="0420d-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="0420d-170">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0420d-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="0420d-171">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0420d-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0420d-172">Remarks</span></span>

<span data-ttu-id="0420d-173">La **clase \_ PerfFormattedData de Win32** se deriva de los [**\_ rendimientos de Win32**](win32-perf.md), que se derivan de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="0420d-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="0420d-174">La clase se encuentra en el espacio de nombres **root \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="0420d-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="0420d-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0420d-175">Requirements</span></span>



| <span data-ttu-id="0420d-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="0420d-176">Requirement</span></span> | <span data-ttu-id="0420d-177">Value</span><span class="sxs-lookup"><span data-stu-id="0420d-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0420d-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0420d-178">Minimum supported client</span></span><br/> | <span data-ttu-id="0420d-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0420d-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="0420d-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0420d-180">Minimum supported server</span></span><br/> | <span data-ttu-id="0420d-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0420d-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="0420d-182">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0420d-182">Namespace</span></span><br/>                | <span data-ttu-id="0420d-183">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0420d-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="0420d-184">MOF</span><span class="sxs-lookup"><span data-stu-id="0420d-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0420d-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0420d-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="0420d-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0420d-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0420d-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0420d-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0420d-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="0420d-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0420d-189">**Rendimiento de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0420d-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="0420d-190">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="0420d-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="0420d-191">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="0420d-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="0420d-192">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="0420d-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="0420d-193">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="0420d-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
