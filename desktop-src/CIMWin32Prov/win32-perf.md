---
description: La clase base para las clases de contador de rendimiento Win32 \_ PerfRawData y Win32 \_ PerfFormattedData.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659695"
---
# <a name="win32_perf-class"></a><span data-ttu-id="94fe5-103">\_Clase de rendimiento Win32</span><span class="sxs-lookup"><span data-stu-id="94fe5-103">Win32\_Perf class</span></span>

<span data-ttu-id="94fe5-104">La clase base para las clases de contador de rendimiento [**Win32 \_ PerfRawData**](win32-perfrawdata.md) y [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="94fe5-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="94fe5-105">**Win32 \_ Perf** define las propiedades de frecuencia y marca de tiempo necesarias que se usan en los algoritmos de [**tipo**](../wmisdk/countertype-qualifier.md) de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="94fe5-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="94fe5-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="94fe5-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="94fe5-107">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="94fe5-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94fe5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94fe5-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="94fe5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="94fe5-109">Members</span></span>

<span data-ttu-id="94fe5-110">La clase de **\_ rendimiento Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="94fe5-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="94fe5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94fe5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94fe5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94fe5-112">Properties</span></span>

<span data-ttu-id="94fe5-113">La clase de **\_ rendimiento Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94fe5-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94fe5-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="94fe5-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94fe5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-117">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="94fe5-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-118">Breve descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="94fe5-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="94fe5-119">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="94fe5-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94fe5-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94fe5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-123">Descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="94fe5-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="94fe5-124">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="94fe5-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-125">**Frequency ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="94fe5-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94fe5-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-128">Frecuencia en TICs por segundo de la propiedad **de \_ objeto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="94fe5-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="94fe5-129">Cuando se subclase, el proveedor define esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="94fe5-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="94fe5-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94fe5-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-131">**Frecuencia \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="94fe5-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-132">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94fe5-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-134">Frecuencia en TICs por segundo de la propiedad **\_ PerfTime** de la frecuencia.</span><span class="sxs-lookup"><span data-stu-id="94fe5-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="94fe5-135">Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.</span><span class="sxs-lookup"><span data-stu-id="94fe5-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="94fe5-136">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94fe5-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-137">**Frecuencia \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="94fe5-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-138">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94fe5-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-140">Frecuencia en TICs por segundo de la propiedad **timestamp \_ Sys100NS** (10 millones).</span><span class="sxs-lookup"><span data-stu-id="94fe5-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="94fe5-141">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94fe5-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="94fe5-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="94fe5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-145">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="94fe5-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-146">Etiqueta por la que se conoce la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="94fe5-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="94fe5-147">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="94fe5-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="94fe5-148">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="94fe5-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-149">**Timestamp ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="94fe5-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-150">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94fe5-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-152">Marca de tiempo definida por el objeto.</span><span class="sxs-lookup"><span data-stu-id="94fe5-152">Object-defined timestamp.</span></span> <span data-ttu-id="94fe5-153">El proveedor define su propiedad.</span><span class="sxs-lookup"><span data-stu-id="94fe5-153">The provider defines his property.</span></span>

<span data-ttu-id="94fe5-154">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94fe5-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-155">**Marca de tiempo \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="94fe5-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-156">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94fe5-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-158">Marca de tiempo de contador de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="94fe5-158">High Performance counter timestamp.</span></span> <span data-ttu-id="94fe5-159">Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.</span><span class="sxs-lookup"><span data-stu-id="94fe5-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="94fe5-160">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94fe5-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94fe5-161">**Marca de tiempo \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="94fe5-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94fe5-162">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94fe5-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94fe5-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94fe5-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94fe5-164">Valor de marca de tiempo en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="94fe5-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="94fe5-165">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94fe5-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94fe5-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94fe5-166">Remarks</span></span>

<span data-ttu-id="94fe5-167">La clase de **\_ rendimiento de Win32** deriva [**de \_ StatisticalInformation de CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="94fe5-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94fe5-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94fe5-168">Requirements</span></span>



| <span data-ttu-id="94fe5-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="94fe5-169">Requirement</span></span> | <span data-ttu-id="94fe5-170">Value</span><span class="sxs-lookup"><span data-stu-id="94fe5-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fe5-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94fe5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="94fe5-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94fe5-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="94fe5-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94fe5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="94fe5-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94fe5-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="94fe5-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94fe5-175">Namespace</span></span><br/>                | <span data-ttu-id="94fe5-176">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94fe5-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="94fe5-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94fe5-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94fe5-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fe5-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94fe5-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="94fe5-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fe5-180">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="94fe5-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="94fe5-181">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="94fe5-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="94fe5-182">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="94fe5-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="94fe5-183">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="94fe5-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="94fe5-184">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="94fe5-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
