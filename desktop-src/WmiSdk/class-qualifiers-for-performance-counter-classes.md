---
description: Especifique información sobre el objeto de rendimiento al que está asignada la clase de contador de rendimiento de WMI.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Calificadores de clase para las clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716570"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="334ef-103">Calificadores de clase para las clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="334ef-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="334ef-104">Los calificadores de clase especifican información sobre el objeto de rendimiento al que está asignada la [clase de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI.</span><span class="sxs-lookup"><span data-stu-id="334ef-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="334ef-105">Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="334ef-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="334ef-106">Calificadores para PerformanceClasses sin formato y con formato</span><span class="sxs-lookup"><span data-stu-id="334ef-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="334ef-107">Calificadores para clases de rendimiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="334ef-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="334ef-108">Calificadores para clases de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="334ef-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="334ef-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="334ef-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="334ef-110">El proveedor "WbemPerfClass" asocia automáticamente los calificadores específicos del contador de rendimiento a las clases y propiedades de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) en la raíz \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="334ef-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="334ef-111">Esta información se aplica a todas las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="334ef-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="334ef-112">Algunos calificadores con valores **booleanos** que son siempre **false** pueden no estar presentes en clases específicas.</span><span class="sxs-lookup"><span data-stu-id="334ef-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="334ef-113">Calificadores para PerformanceClasses sin formato y con formato</span><span class="sxs-lookup"><span data-stu-id="334ef-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="334ef-114">Los calificadores siguientes se aplican a todas las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="334ef-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="334ef-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cocida**</span><span class="sxs-lookup"><span data-stu-id="334ef-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-116">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-116">**boolean**</span></span>

<span data-ttu-id="334ef-117">Indica si la clase contiene datos cocidos.</span><span class="sxs-lookup"><span data-stu-id="334ef-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**</span><span class="sxs-lookup"><span data-stu-id="334ef-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-119">**string**</span><span class="sxs-lookup"><span data-stu-id="334ef-119">**string**</span></span>

<span data-ttu-id="334ef-120">Nombre del objeto de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="334ef-120">Performance object name.</span></span> <span data-ttu-id="334ef-121">Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="334ef-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="334ef-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="334ef-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="334ef-123">**sint32**</span></span>

<span data-ttu-id="334ef-124">No proporciona datos detallados.</span><span class="sxs-lookup"><span data-stu-id="334ef-124">Does not provide detail data.</span></span> <span data-ttu-id="334ef-125">Siempre contiene el valor 100.</span><span class="sxs-lookup"><span data-stu-id="334ef-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinámica**</span><span class="sxs-lookup"><span data-stu-id="334ef-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-127">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-127">**boolean**</span></span>

<span data-ttu-id="334ef-128">Siempre se establece en **true** porque las instancias siempre son dinámicas.</span><span class="sxs-lookup"><span data-stu-id="334ef-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span><span class="sxs-lookup"><span data-stu-id="334ef-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-130">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-130">**boolean**</span></span>

<span data-ttu-id="334ef-131">Indica si la clase procede de una biblioteca de rendimiento heredada.</span><span class="sxs-lookup"><span data-stu-id="334ef-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="334ef-132">Siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="334ef-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="334ef-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="334ef-134">**sint32**</span></span>

<span data-ttu-id="334ef-135">Los índices ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="334ef-135">Indexes are no longer valid.</span></span> <span data-ttu-id="334ef-136">Este calificador siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="334ef-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="334ef-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="334ef-138">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-138">**boolean**</span></span>

<span data-ttu-id="334ef-139">Indica que la clase es una clase de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="334ef-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="334ef-140">Siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="334ef-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="334ef-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="334ef-142">**sint32**</span></span>

<span data-ttu-id="334ef-143">Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="334ef-143">Locale identifier.</span></span> <span data-ttu-id="334ef-144">El valor siempre es 1033 (Inglés de EE. UU.).</span><span class="sxs-lookup"><span data-stu-id="334ef-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="334ef-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="334ef-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="334ef-146">**int32**</span></span>

<span data-ttu-id="334ef-147">Los índices ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="334ef-147">Indexes are no longer valid.</span></span> <span data-ttu-id="334ef-148">Este calificador siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="334ef-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Presta**</span><span class="sxs-lookup"><span data-stu-id="334ef-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-150">**string**</span><span class="sxs-lookup"><span data-stu-id="334ef-150">**string**</span></span>

<span data-ttu-id="334ef-151">Nombre del proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="334ef-151">Name of the instance provider.</span></span> <span data-ttu-id="334ef-152">El valor es "WbemPerfV2".</span><span class="sxs-lookup"><span data-stu-id="334ef-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="334ef-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**Rename**</span><span class="sxs-lookup"><span data-stu-id="334ef-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-154">**string**</span><span class="sxs-lookup"><span data-stu-id="334ef-154">**string**</span></span>

<span data-ttu-id="334ef-155">Nombre del controlador en la clave **HKEY \_ local \_ Machine \\ CurrentControlSet \\ Services** , en la que se puede encontrar la clave de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="334ef-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="334ef-156">Este nombre también es el nombre del servicio que proporciona el contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="334ef-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Simple**</span><span class="sxs-lookup"><span data-stu-id="334ef-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-158">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-158">**boolean**</span></span>

<span data-ttu-id="334ef-159">Si **es true**, indica que solo existe una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="334ef-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="334ef-160">Calificadores para clases de rendimiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="334ef-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="334ef-161">Los calificadores siguientes se aplican a todas las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="334ef-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="334ef-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costoso**</span><span class="sxs-lookup"><span data-stu-id="334ef-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-163">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-163">**boolean**</span></span>

<span data-ttu-id="334ef-164">Indica si la obtención de instancias de esta clase es una operación costosa.</span><span class="sxs-lookup"><span data-stu-id="334ef-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="334ef-165">Siempre se establece en **true** para las clases con " \_ Costly" anexadas al final del nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="334ef-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="334ef-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="334ef-167">**uint32**</span></span>

<span data-ttu-id="334ef-168">No proporciona datos detallados.</span><span class="sxs-lookup"><span data-stu-id="334ef-168">Does not provide detail data.</span></span> <span data-ttu-id="334ef-169">Siempre contiene el valor 100.</span><span class="sxs-lookup"><span data-stu-id="334ef-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="334ef-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-171">**boolean**</span><span class="sxs-lookup"><span data-stu-id="334ef-171">**boolean**</span></span>

<span data-ttu-id="334ef-172">El valor siempre es **false**.</span><span class="sxs-lookup"><span data-stu-id="334ef-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="334ef-173">Calificadores para clases de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="334ef-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="334ef-174">Los calificadores siguientes se aplican a todas las clases que se derivan de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="334ef-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="334ef-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autocook**</span><span class="sxs-lookup"><span data-stu-id="334ef-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="334ef-176">**int32**</span></span>

<span data-ttu-id="334ef-177">Indica que los valores de las instancias de clase se calculan automáticamente a partir de la clase de datos sin procesar correspondiente.</span><span class="sxs-lookup"><span data-stu-id="334ef-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="334ef-178">El valor es siempre 1.</span><span class="sxs-lookup"><span data-stu-id="334ef-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="334ef-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**Autocook \_ RawClass**</span><span class="sxs-lookup"><span data-stu-id="334ef-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="334ef-180">**string**</span><span class="sxs-lookup"><span data-stu-id="334ef-180">**string**</span></span>

<span data-ttu-id="334ef-181">Nombre de la clase sin procesar que se va a usar para el cálculo de la clase con formato.</span><span class="sxs-lookup"><span data-stu-id="334ef-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="334ef-182">Este calificador es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="334ef-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="334ef-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="334ef-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="334ef-184">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="334ef-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="334ef-185">Calificadores específicos de las clases de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="334ef-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="334ef-186">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="334ef-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="334ef-187">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="334ef-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="334ef-188">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="334ef-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
