---
description: Los calificadores de propiedad especifican información sobre el contador de rendimiento al que se asigna la propiedad.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Calificadores de propiedad para las clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278978"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="f07ed-103">Calificadores de propiedad para las clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f07ed-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="f07ed-104">Los calificadores de propiedad especifican información sobre el contador de rendimiento al que se asigna la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f07ed-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="f07ed-105">Calificadores de propiedad para las clases de rendimiento RAW y con formato</span><span class="sxs-lookup"><span data-stu-id="f07ed-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="f07ed-106">Calificadores de propiedad para las clases de rendimiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="f07ed-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="f07ed-107">Calificadores de propiedad para las clases de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="f07ed-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="f07ed-108">Cómo interpretar calificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="f07ed-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="f07ed-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f07ed-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="f07ed-110">El contador de rendimiento forma parte de un objeto de rendimiento representado por un contador de rendimiento de [clase de contador](/windows/desktop/CIMWin32Prov/performance-counter-classes) de rendimiento de WMI: el proveedor WbemPerfClass asocia automáticamente calificadores específicos a las clases y propiedades de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) en la raíz \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="f07ed-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="f07ed-111">Esta información se aplica a todas las instancias de la clase de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f07ed-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="f07ed-112">Algunos calificadores con valores **booleanos** que son siempre false pueden no estar presentes en clases específicas.</span><span class="sxs-lookup"><span data-stu-id="f07ed-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="f07ed-113">Calificadores de propiedad para las clases de rendimiento RAW y con formato</span><span class="sxs-lookup"><span data-stu-id="f07ed-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="f07ed-114">En la lista siguiente se enumeran los calificadores que se aplican a las propiedades de las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) o [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="f07ed-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="f07ed-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**Tipo**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="f07ed-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="f07ed-116">**sint32**</span></span>

<span data-ttu-id="f07ed-117">Valor entero en la enumeración de tipo de contador, tal y como se define en WINPERF. h o Perflib. h.</span><span class="sxs-lookup"><span data-stu-id="f07ed-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="f07ed-118">El calificador de [**contratipo**](countertype-qualifier.md)indica la fórmula o el algoritmo que se usa para calcular el valor que se muestra en el monitor de sistema para el contador que representa la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f07ed-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**</span><span class="sxs-lookup"><span data-stu-id="f07ed-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-120">**string**</span><span class="sxs-lookup"><span data-stu-id="f07ed-120">**string**</span></span>

<span data-ttu-id="f07ed-121">Nombre del contador de rendimiento, según lo especificado por el ayudante de datos de rendimiento (PDH).</span><span class="sxs-lookup"><span data-stu-id="f07ed-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="f07ed-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="f07ed-123">**sint32**</span></span>

<span data-ttu-id="f07ed-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f07ed-124">Not used.</span></span> <span data-ttu-id="f07ed-125">Siempre contiene 0.</span><span class="sxs-lookup"><span data-stu-id="f07ed-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="f07ed-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="f07ed-127">**sint32**</span></span>

<span data-ttu-id="f07ed-128">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f07ed-128">Not used.</span></span> <span data-ttu-id="f07ed-129">Siempre contiene 0.</span><span class="sxs-lookup"><span data-stu-id="f07ed-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="f07ed-130">Calificadores de propiedad para las clases de rendimiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="f07ed-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="f07ed-131">En la lista siguiente se enumeran los calificadores que se aplican a todas las propiedades de las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="f07ed-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="f07ed-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="f07ed-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-133">**boolean**</span><span class="sxs-lookup"><span data-stu-id="f07ed-133">**boolean**</span></span>

<span data-ttu-id="f07ed-134">Indica si esta propiedad es el contador predeterminado que se va a usar en los cuadros de lista.</span><span class="sxs-lookup"><span data-stu-id="f07ed-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="f07ed-135">Este calificador tiene como valor predeterminado **false** para los contadores de rendimiento versión 6,0 porque no proporcionan datos para él.</span><span class="sxs-lookup"><span data-stu-id="f07ed-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="f07ed-136">Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="f07ed-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="f07ed-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="f07ed-138">**sint32**</span></span>

<span data-ttu-id="f07ed-139">Potencia de 10 que se va a usar para mostrar el contador.</span><span class="sxs-lookup"><span data-stu-id="f07ed-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="f07ed-140">Para cero, el máximo estimado es 10 ^ 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="f07ed-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="f07ed-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="f07ed-142">**sint32**</span></span>

<span data-ttu-id="f07ed-143">Nivel de conocimientos de audiencia.</span><span class="sxs-lookup"><span data-stu-id="f07ed-143">Audience level of knowledge.</span></span> <span data-ttu-id="f07ed-144">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f07ed-144">Not used.</span></span> <span data-ttu-id="f07ed-145">El valor siempre es 100.</span><span class="sxs-lookup"><span data-stu-id="f07ed-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="f07ed-146">Calificadores de propiedad para las clases de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="f07ed-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="f07ed-147">En la lista siguiente se enumeran los calificadores que se aplican a todas las propiedades de las clases que se derivan de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="f07ed-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="f07ed-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span><span class="sxs-lookup"><span data-stu-id="f07ed-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-149">**string**</span><span class="sxs-lookup"><span data-stu-id="f07ed-149">**string**</span></span>

<span data-ttu-id="f07ed-150">Tipo de fórmula usado para generar el resultado.</span><span class="sxs-lookup"><span data-stu-id="f07ed-150">Formula type used to produce the result.</span></span> <span data-ttu-id="f07ed-151">Cada tipo de contador usa los otros calificadores de propiedad para calcular el resultado mostrado como el valor de la propiedad actual.</span><span class="sxs-lookup"><span data-stu-id="f07ed-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="f07ed-152">Los calificadores **Counter**, **PerfTimeStamp** y **PerfTimeFreq** se asignan a las propiedades de una clase sin procesar que proporcionan los datos.</span><span class="sxs-lookup"><span data-stu-id="f07ed-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="f07ed-153">Para obtener más información, vea [calificador de tipo contratype](countertype-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="f07ed-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Bloque**</span><span class="sxs-lookup"><span data-stu-id="f07ed-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-155">**string**</span><span class="sxs-lookup"><span data-stu-id="f07ed-155">**string**</span></span>

<span data-ttu-id="f07ed-156">Nombre de una propiedad necesaria en la clase sin procesar correspondiente que se va a usar como valor de contador en la fórmula de cocina.</span><span class="sxs-lookup"><span data-stu-id="f07ed-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="f07ed-157">El valor debe ser el nombre de la propiedad de origen de datos en la clase sin formato correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f07ed-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="f07ed-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-159">**string**</span><span class="sxs-lookup"><span data-stu-id="f07ed-159">**string**</span></span>

<span data-ttu-id="f07ed-160">Nombre de una propiedad de una clase sin procesar que se va a usar como una frecuencia en la fórmula de cocina.</span><span class="sxs-lookup"><span data-stu-id="f07ed-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="f07ed-161">Se usará el valor predeterminado adecuado en el nivel de clase si este calificador no está presente para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f07ed-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="f07ed-162">La frecuencia representa los tics por segundo de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f07ed-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="f07ed-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="f07ed-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="f07ed-164">**string**</span><span class="sxs-lookup"><span data-stu-id="f07ed-164">**string**</span></span>

<span data-ttu-id="f07ed-165">Nombre de una propiedad de una clase sin procesar que se va a usar como marca de tiempo en la fórmula de cocina.</span><span class="sxs-lookup"><span data-stu-id="f07ed-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="f07ed-166">Se utiliza el valor predeterminado adecuado en el nivel de clase si este calificador no está presente para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f07ed-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="f07ed-167">Una marca de tiempo generada automáticamente puede producir un error en un cálculo porque la marca de tiempo es una aproximación y no tiene en cuenta la sobrecarga generada por el cálculo de referencias y la recopilación de datos real.</span><span class="sxs-lookup"><span data-stu-id="f07ed-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="f07ed-168">Cómo interpretar calificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="f07ed-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="f07ed-169">Las propiedades de las clases [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen los datos calculados proporcionados por el [proveedor de datos de rendimiento con formato](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f07ed-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="f07ed-170">El valor de la propiedad es el resultado calculado final.</span><span class="sxs-lookup"><span data-stu-id="f07ed-170">The property value is the final calculated result.</span></span> <span data-ttu-id="f07ed-171">Los calificadores proporcionan una receta.</span><span class="sxs-lookup"><span data-stu-id="f07ed-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="f07ed-172">El **contador** y los calificadores **base** apuntan a los orígenes de datos y **CookingType** especifica la fórmula que se usa para generar el resultado.</span><span class="sxs-lookup"><span data-stu-id="f07ed-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="f07ed-173">La marca de tiempo y la frecuencia de muestra también proceden de la clase sin procesar correspondiente y se denominan en **PerfTimeStamp** y **PerfTimeFreq**.</span><span class="sxs-lookup"><span data-stu-id="f07ed-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="f07ed-174">Por ejemplo, una de las clases con formato suministradas por WMI, [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contiene una propiedad denominada **AvgDiskBytesPerRead**.</span><span class="sxs-lookup"><span data-stu-id="f07ed-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="f07ed-175">El nombre de la propiedad en la clase con formato debe ser el mismo que el de la propiedad de la clase sin formato.</span><span class="sxs-lookup"><span data-stu-id="f07ed-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="f07ed-176">La propiedad **AvgDiskBytesPerRead** tiene los calificadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f07ed-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="f07ed-177">En la lista siguiente se enumeran los calificadores de propiedad disponibles para las propiedades de todas las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="f07ed-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="f07ed-178">Qualifier</span><span class="sxs-lookup"><span data-stu-id="f07ed-178">Qualifier</span></span>         | <span data-ttu-id="f07ed-179">Value</span><span class="sxs-lookup"><span data-stu-id="f07ed-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="f07ed-180">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="f07ed-180">**CookingType**</span></span>   | <span data-ttu-id="f07ed-181">media de rendimiento en \_ \_ masa</span><span class="sxs-lookup"><span data-stu-id="f07ed-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="f07ed-182">**Contador**</span><span class="sxs-lookup"><span data-stu-id="f07ed-182">**Counter**</span></span>       | <span data-ttu-id="f07ed-183">AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="f07ed-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="f07ed-184">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="f07ed-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="f07ed-185">Marca de tiempo \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="f07ed-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="f07ed-186">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="f07ed-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="f07ed-187">Frecuencia \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="f07ed-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="f07ed-188">**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="f07ed-188">**PerfIndex**</span></span>     | <span data-ttu-id="f07ed-189">408</span><span class="sxs-lookup"><span data-stu-id="f07ed-189">408</span></span>                       |
| <span data-ttu-id="f07ed-190">**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="f07ed-190">**HelpIndex**</span></span>     | <span data-ttu-id="f07ed-191">409</span><span class="sxs-lookup"><span data-stu-id="f07ed-191">409</span></span>                       |
| <span data-ttu-id="f07ed-192">**Básica**</span><span class="sxs-lookup"><span data-stu-id="f07ed-192">**Base**</span></span>          | <span data-ttu-id="f07ed-193">Base de AvgDiskBytesPerRead \_</span><span class="sxs-lookup"><span data-stu-id="f07ed-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="f07ed-194">La propiedad **AvgDiskBytesPerRead** informa del número promedio de bytes transferidos desde el disco durante las operaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="f07ed-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="f07ed-195">La fórmula para la \_ media de rendimiento \_ masiva es:</span><span class="sxs-lookup"><span data-stu-id="f07ed-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="f07ed-196">(Sample2-Sample1)/(base Sample2-base Sample1)</span><span class="sxs-lookup"><span data-stu-id="f07ed-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="f07ed-197">La operación de lectura se muestrea con la frecuencia especificada por **PerfTimeFreq** con el valor **PerfTimeStamp** que indica el ejemplo más reciente.</span><span class="sxs-lookup"><span data-stu-id="f07ed-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="f07ed-198">Los datos del contador sin formato en bytes se toman de la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) .</span><span class="sxs-lookup"><span data-stu-id="f07ed-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="f07ed-199">El número base de datos de operaciones se toma de la propiedad **\_ base AvgDiskBytesPerRead** en esa misma clase.</span><span class="sxs-lookup"><span data-stu-id="f07ed-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="f07ed-200">Para obtener más información, consulte [obtención de datos de rendimiento estadísticos](obtaining-statistical-performance-data.md) y [supervisión de datos de rendimiento](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="f07ed-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f07ed-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f07ed-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f07ed-202">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f07ed-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="f07ed-203">Calificadores específicos de las clases de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="f07ed-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="f07ed-204">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f07ed-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="f07ed-205">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="f07ed-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="f07ed-206">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="f07ed-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
