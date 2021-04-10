---
description: En WMI, puede definir datos de rendimiento estadísticos basados en datos de clases de rendimiento con formato derivadas de Win32 \_ PerfFormattedData. Las estadísticas disponibles son el promedio, el mínimo, el máximo, el intervalo y la varianza, tal como se define en los tipos de contador estadísticos.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Obtención de datos de rendimiento estadísticos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153725"
---
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="5f92b-104">Obtención de datos de rendimiento estadísticos</span><span class="sxs-lookup"><span data-stu-id="5f92b-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="5f92b-105">En WMI, puede definir datos de rendimiento estadísticos basados en datos de clases de rendimiento con formato derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="5f92b-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="5f92b-106">Las estadísticas disponibles son el promedio, el mínimo, el máximo, el intervalo y la varianza, tal como se define en los [tipos de contador estadísticos](statistical-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="5f92b-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="5f92b-107">La lista siguiente incluye los tipos de contador estadísticos especiales:</span><span class="sxs-lookup"><span data-stu-id="5f92b-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="5f92b-108">media de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="5f92b-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="5f92b-109">COOKER \_ mín.</span><span class="sxs-lookup"><span data-stu-id="5f92b-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="5f92b-110">COOKER \_ máx.</span><span class="sxs-lookup"><span data-stu-id="5f92b-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="5f92b-111">\_intervalo Cooker</span><span class="sxs-lookup"><span data-stu-id="5f92b-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="5f92b-112">varianza de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="5f92b-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="5f92b-113">En los siguientes ejemplos se muestra cómo:</span><span class="sxs-lookup"><span data-stu-id="5f92b-113">The following examples show how to:</span></span>

-   <span data-ttu-id="5f92b-114">Cree un archivo MOF que defina una clase de datos calculados.</span><span class="sxs-lookup"><span data-stu-id="5f92b-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="5f92b-115">Escriba un script que cree una instancia de la clase y actualice periódicamente los datos de la instancia con los valores estadísticos recalculados.</span><span class="sxs-lookup"><span data-stu-id="5f92b-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="5f92b-116">Archivo MOF</span><span class="sxs-lookup"><span data-stu-id="5f92b-116">MOF File</span></span>

<span data-ttu-id="5f92b-117">En el siguiente ejemplo de código MOF se crea una nueva clase de datos calculados denominada **Win32 \_ PerfFormattedData \_ AvailableMBytes**.</span><span class="sxs-lookup"><span data-stu-id="5f92b-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="5f92b-118">Esta clase contiene datos de la propiedad **AvailableMBytes** de la clase sin formato [**Win32 PerfRawData de rendimiento de \_ \_ \_ memoria**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span><span class="sxs-lookup"><span data-stu-id="5f92b-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="5f92b-119">La **clase \_ \_ AvailableBytes de Win32 PerfFormattedData** define las propiedades **Average**, **min**, **Max**, **Range** y **Variance**.</span><span class="sxs-lookup"><span data-stu-id="5f92b-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="5f92b-120">El archivo MOF utiliza los [**calificadores de propiedad para las clases de contador de rendimiento con formato**](property-qualifiers-for-performance-counter-classes.md) para definir el origen de datos de la propiedad y la fórmula de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5f92b-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="5f92b-121">La propiedad **Average** obtiene datos sin procesar de la [**\_ \_ \_ memoria PerfRawData de rendimiento de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Propiedad AvailableMBytes** .</span><span class="sxs-lookup"><span data-stu-id="5f92b-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="5f92b-122">El **calificador** de contador para la propiedad **Average** especifica el origen de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="5f92b-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="5f92b-123">El calificador **CookingType** especifica la fórmula [Cooker \_ min](cooker-min.md) para calcular los datos.</span><span class="sxs-lookup"><span data-stu-id="5f92b-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="5f92b-124">El calificador **SampleWindow** especifica el número de muestras que se deben llevar a cabo antes de realizar el cálculo.</span><span class="sxs-lookup"><span data-stu-id="5f92b-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a><span data-ttu-id="5f92b-125">Script</span><span class="sxs-lookup"><span data-stu-id="5f92b-125">Script</span></span>

<span data-ttu-id="5f92b-126">En el siguiente ejemplo de código de script se obtienen estadísticas sobre la memoria disponible, en megabytes, con el MOF creado previamente.</span><span class="sxs-lookup"><span data-stu-id="5f92b-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="5f92b-127">El script utiliza el objeto de scripting de [**SWbemRefresher**](swbemrefresher.md) para crear un actualizador que contenga una instancia de la clase Statistics que crea el archivo MOF, que es **Win32 \_ PerfFormattedData \_ MemoryStatistics**.</span><span class="sxs-lookup"><span data-stu-id="5f92b-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="5f92b-128">Para obtener más información sobre el uso de scripts, vea [actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="5f92b-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="5f92b-129">Si trabaja en C++, vea [obtener acceso a los datos de rendimiento en c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="5f92b-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="5f92b-130">Se debe llamar a [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) después de obtener el elemento de la llamada a [**SWbemRefresher. Add**](swbemrefresher-add.md) o se producirá un error en el script.</span><span class="sxs-lookup"><span data-stu-id="5f92b-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="5f92b-131">Se debe llamar a [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) antes de escribir el bucle para obtener los valores de línea de base, o bien las propiedades estadísticas son cero (0) en el primer paso.</span><span class="sxs-lookup"><span data-stu-id="5f92b-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a><span data-ttu-id="5f92b-132">Ejecutar el script</span><span class="sxs-lookup"><span data-stu-id="5f92b-132">Running the Script</span></span>

<span data-ttu-id="5f92b-133">En el procedimiento siguiente se describe cómo ejecutar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5f92b-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="5f92b-134">**Para ejecutar el script de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5f92b-134">**To run the example script**</span></span>

1.  <span data-ttu-id="5f92b-135">Copie el código MOF y el script en los archivos del equipo.</span><span class="sxs-lookup"><span data-stu-id="5f92b-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="5f92b-136">Asigne a la extensión. mof del archivo MOF y el archivo de script la descripción. vbs.</span><span class="sxs-lookup"><span data-stu-id="5f92b-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="5f92b-137">En la línea de comandos, cambie al directorio donde se almacenan los archivos y ejecute [**MOFCOMP**](mofcomp.md) en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="5f92b-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="5f92b-138">Por ejemplo, si se denomina el archivo *CalculatedData. mof*, el comando es **MOFCOMP** *CalculatedData. mof*</span><span class="sxs-lookup"><span data-stu-id="5f92b-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="5f92b-139">Ejecute el script.</span><span class="sxs-lookup"><span data-stu-id="5f92b-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f92b-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f92b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f92b-141">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="5f92b-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="5f92b-142">Obtener acceso a las clases de rendimiento preinstaladas de WMI</span><span class="sxs-lookup"><span data-stu-id="5f92b-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="5f92b-143">**Calificadores de propiedad para las clases de contador de rendimiento con formato**</span><span class="sxs-lookup"><span data-stu-id="5f92b-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="5f92b-144">Tipos de contadores estadísticos</span><span class="sxs-lookup"><span data-stu-id="5f92b-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
