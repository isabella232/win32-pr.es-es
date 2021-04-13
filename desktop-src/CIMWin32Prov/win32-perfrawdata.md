---
description: La clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539357"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="572d4-103">\_Clase Win32 PerfRawData</span><span class="sxs-lookup"><span data-stu-id="572d4-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="572d4-104">La clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.</span><span class="sxs-lookup"><span data-stu-id="572d4-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="572d4-105">Para que aparezca en el monitor de sistema, las clases de contador de rendimiento se deben agregar al \\ espacio de nombres root cimv2 y derivarse de **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="572d4-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="572d4-106">Los datos de estas clases son proporcionados por el [proveedor de contador de rendimiento](../wmisdk/performance-counter-provider.md)de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="572d4-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="572d4-107">Las siguientes propiedades se heredan cuando una clase se deriva de **Win32 \_ PerfRawData**:</span><span class="sxs-lookup"><span data-stu-id="572d4-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="572d4-108">**Marca de tiempo \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="572d4-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="572d4-109">**Marca de tiempo \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="572d4-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="572d4-110">**Timestamp ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="572d4-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="572d4-111">**Frecuencia \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="572d4-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="572d4-112">**Frecuencia \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="572d4-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="572d4-113">**Frequency ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="572d4-113">**Frequency\_Object**</span></span>

<span data-ttu-id="572d4-114">En cada caso, las propiedades deben ser rellenadas por el proveedor o la clase no se puede mostrar en el monitor del sistema.</span><span class="sxs-lookup"><span data-stu-id="572d4-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="572d4-115">Estas propiedades se utilizan para calcular las fórmulas de tipo de contador por parte de los consumidores de datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="572d4-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="572d4-116">La siguiente sintaxis se simplifica desde el código MOF y muestra todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="572d4-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="572d4-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="572d4-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="572d4-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="572d4-118">Members</span></span>

<span data-ttu-id="572d4-119">La **clase \_ PerfRawData de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="572d4-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="572d4-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="572d4-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="572d4-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="572d4-121">Properties</span></span>

<span data-ttu-id="572d4-122">La **clase \_ PerfRawData de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="572d4-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="572d4-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="572d4-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="572d4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="572d4-126">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="572d4-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="572d4-127">Breve descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="572d4-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="572d4-128">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="572d4-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="572d4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-132">Descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="572d4-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="572d4-133">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-134">**Frequency ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="572d4-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="572d4-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-137">Frecuencia en TICs por segundo de la propiedad **de \_ objeto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="572d4-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="572d4-138">Cuando se subclase, el proveedor define esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="572d4-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="572d4-139">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="572d4-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="572d4-140">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-141">**Frecuencia \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="572d4-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-142">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="572d4-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-144">Frecuencia en TICs por segundo de la propiedad **\_ PerfTime** de la frecuencia.</span><span class="sxs-lookup"><span data-stu-id="572d4-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="572d4-145">Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.</span><span class="sxs-lookup"><span data-stu-id="572d4-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="572d4-146">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="572d4-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="572d4-147">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-148">**Frecuencia \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="572d4-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-149">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="572d4-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-151">Frecuencia en TICs por segundo de la propiedad **timestamp \_ Sys100NS** (10 millones).</span><span class="sxs-lookup"><span data-stu-id="572d4-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="572d4-152">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="572d4-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="572d4-153">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-154">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="572d4-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="572d4-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="572d4-157">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="572d4-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="572d4-158">Etiqueta por la que se conoce la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="572d4-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="572d4-159">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="572d4-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="572d4-160">Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-161">**Timestamp ( \_ objeto)**</span><span class="sxs-lookup"><span data-stu-id="572d4-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-162">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="572d4-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-164">Marca de tiempo definida por el objeto.</span><span class="sxs-lookup"><span data-stu-id="572d4-164">Object-defined timestamp.</span></span> <span data-ttu-id="572d4-165">El proveedor define su propiedad.</span><span class="sxs-lookup"><span data-stu-id="572d4-165">The provider defines his property.</span></span>

<span data-ttu-id="572d4-166">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="572d4-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="572d4-167">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-168">**Marca de tiempo \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="572d4-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-169">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="572d4-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-171">Marca de tiempo de contador de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="572d4-171">High Performance counter timestamp.</span></span> <span data-ttu-id="572d4-172">Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.</span><span class="sxs-lookup"><span data-stu-id="572d4-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="572d4-173">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="572d4-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="572d4-174">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="572d4-175">**Marca de tiempo \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="572d4-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="572d4-176">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="572d4-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="572d4-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="572d4-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="572d4-178">Valor de marca de tiempo en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="572d4-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="572d4-179">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="572d4-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="572d4-180">Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="572d4-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="572d4-181">Remarks</span></span>

<span data-ttu-id="572d4-182">La **clase \_ PerfRawData de Win32** se deriva de los [**\_ rendimientos de Win32**](win32-perf.md), que se derivan de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="572d4-183">Todas las clases derivadas de [**\_ rendimiento de Win32**](win32-perf.md) están diseñadas para usarse con un objeto [*actualizador*](../wmisdk/gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="572d4-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="572d4-184">Para obtener más información sobre cómo crear y usar un objeto actualizador en el lenguaje de programación C++, vea [obtener acceso a los datos de rendimiento en C++](../wmisdk/accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="572d4-185">Para obtener más información sobre cómo crear y usar un objeto actualizador en un lenguaje de programación de scripts, vea [actualizar datos WMI en scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="572d4-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="572d4-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="572d4-186">Requirements</span></span>



| <span data-ttu-id="572d4-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="572d4-187">Requirement</span></span> | <span data-ttu-id="572d4-188">Value</span><span class="sxs-lookup"><span data-stu-id="572d4-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="572d4-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="572d4-189">Minimum supported client</span></span><br/> | <span data-ttu-id="572d4-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="572d4-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="572d4-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="572d4-191">Minimum supported server</span></span><br/> | <span data-ttu-id="572d4-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="572d4-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="572d4-193">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="572d4-193">Namespace</span></span><br/>                | <span data-ttu-id="572d4-194">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="572d4-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="572d4-195">MOF</span><span class="sxs-lookup"><span data-stu-id="572d4-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="572d4-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="572d4-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="572d4-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="572d4-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="572d4-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="572d4-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572d4-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="572d4-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572d4-200">**Rendimiento de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="572d4-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="572d4-201">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="572d4-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="572d4-202">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="572d4-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="572d4-203">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="572d4-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="572d4-204">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="572d4-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
