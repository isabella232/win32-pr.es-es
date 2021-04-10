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
# <a name="obtaining-statistical-performance-data"></a>Obtención de datos de rendimiento estadísticos

En WMI, puede definir datos de rendimiento estadísticos basados en datos de clases de rendimiento con formato derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Las estadísticas disponibles son el promedio, el mínimo, el máximo, el intervalo y la varianza, tal como se define en los [tipos de contador estadísticos](statistical-counter-types.md).

La lista siguiente incluye los tipos de contador estadísticos especiales:

-   [media de COOKER \_](cooker-average.md)
-   [COOKER \_ mín.](cooker-min.md)
-   [COOKER \_ máx.](cooker-max.md)
-   [\_intervalo Cooker](cooker-range.md)
-   [varianza de COOKER \_](cooker-variance.md)

En los siguientes ejemplos se muestra cómo:

-   Cree un archivo MOF que defina una clase de datos calculados.
-   Escriba un script que cree una instancia de la clase y actualice periódicamente los datos de la instancia con los valores estadísticos recalculados.

## <a name="mof-file"></a>Archivo MOF

En el siguiente ejemplo de código MOF se crea una nueva clase de datos calculados denominada **Win32 \_ PerfFormattedData \_ AvailableMBytes**. Esta clase contiene datos de la propiedad **AvailableMBytes** de la clase sin formato [**Win32 PerfRawData de rendimiento de \_ \_ \_ memoria**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). La **clase \_ \_ AvailableBytes de Win32 PerfFormattedData** define las propiedades **Average**, **min**, **Max**, **Range** y **Variance**.

El archivo MOF utiliza los [**calificadores de propiedad para las clases de contador de rendimiento con formato**](property-qualifiers-for-performance-counter-classes.md) para definir el origen de datos de la propiedad y la fórmula de cálculo.

-   La propiedad **Average** obtiene datos sin procesar de la [**\_ \_ \_ memoria PerfRawData de rendimiento de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Propiedad AvailableMBytes** .
-   El **calificador** de contador para la propiedad **Average** especifica el origen de datos sin procesar.
-   El calificador **CookingType** especifica la fórmula [Cooker \_ min](cooker-min.md) para calcular los datos.
-   El calificador **SampleWindow** especifica el número de muestras que se deben llevar a cabo antes de realizar el cálculo.


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



## <a name="script"></a>Script

En el siguiente ejemplo de código de script se obtienen estadísticas sobre la memoria disponible, en megabytes, con el MOF creado previamente. El script utiliza el objeto de scripting de [**SWbemRefresher**](swbemrefresher.md) para crear un actualizador que contenga una instancia de la clase Statistics que crea el archivo MOF, que es **Win32 \_ PerfFormattedData \_ MemoryStatistics**. Para obtener más información sobre el uso de scripts, vea [actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md). Si trabaja en C++, vea [obtener acceso a los datos de rendimiento en c++](accessing-performance-data-in-c--.md).

> [!Note]  
> Se debe llamar a [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) después de obtener el elemento de la llamada a [**SWbemRefresher. Add**](swbemrefresher-add.md) o se producirá un error en el script. Se debe llamar a [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) antes de escribir el bucle para obtener los valores de línea de base, o bien las propiedades estadísticas son cero (0) en el primer paso.

 


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



## <a name="running-the-script"></a>Ejecutar el script

En el procedimiento siguiente se describe cómo ejecutar el ejemplo.

**Para ejecutar el script de ejemplo**

1.  Copie el código MOF y el script en los archivos del equipo.
2.  Asigne a la extensión. mof del archivo MOF y el archivo de script la descripción. vbs.
3.  En la línea de comandos, cambie al directorio donde se almacenan los archivos y ejecute [**MOFCOMP**](mofcomp.md) en el archivo MOF. Por ejemplo, si se denomina el archivo *CalculatedData. mof*, el comando es **MOFCOMP** *CalculatedData. mof*
4.  Ejecute el script.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Obtener acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Calificadores de propiedad para las clases de contador de rendimiento con formato**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipos de contadores estadísticos](statistical-counter-types.md)
</dt> </dl>

 

 
