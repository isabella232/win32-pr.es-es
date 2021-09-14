---
description: En WMI, puede definir datos estadísticos de rendimiento basados en datos en clases de rendimiento con formato derivadas de \_ Win32 PerfFormattedData. Las estadísticas disponibles son promedio, mínimo, máximo, intervalo y varianza, tal como se define en Tipos de contadores estadísticos.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Obtener datos estadísticos de rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063959"
---
# <a name="obtaining-statistical-performance-data"></a>Obtener datos estadísticos de rendimiento

En WMI, puede definir datos estadísticos de rendimiento basados en datos en clases de rendimiento con formato derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Las estadísticas disponibles son promedio, mínimo, máximo, intervalo y varianza, tal y como se define en [Tipos de contadores estadísticos](statistical-counter-types.md).

En la lista siguiente se incluyen los tipos de contadores estadísticos especiales:

-   [COOKER \_ AVERAGE](cooker-average.md)
-   [COOKER \_ MIN](cooker-min.md)
-   [COOKER \_ MAX](cooker-max.md)
-   [INTERVALO DE LA \_ COCINA](cooker-range.md)
-   [VARIANZA DE LA \_ COCINA](cooker-variance.md)

En los ejemplos siguientes se muestra cómo:

-   Cree un archivo MOF que defina una clase de datos calculados.
-   Escriba un script que cree una instancia de la clase y actualice periódicamente los datos de la instancia con los valores estadísticos recalculados.

## <a name="mof-file"></a>Archivo MOF

En el ejemplo de código MOF siguiente se crea una nueva clase de datos calculada denominada **Win32 \_ PerfFormattedData \_ AvailableMBytes**. Esta clase contiene datos de la **propiedad AvailableMBytes** de la clase sin formato [**\_ Win32 PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). La **clase \_ PerfFormattedData \_ AvailableBytes de Win32** define las propiedades **Average**, **Min,** **Max,** **Range** y **Variance**.

El archivo MOF usa los calificadores de propiedad para [**las clases de contador**](property-qualifiers-for-performance-counter-classes.md) de rendimiento con formato para definir el origen de datos de propiedad y la fórmula de cálculo.

-   La **propiedad Average** obtiene datos sin procesar de la memoria [**\_ PerfRawData \_ perfOS \_ de Win32.**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)**Propiedad AvailableMBytes.**
-   El **calificador Counter** para **la propiedad Average** especifica el origen de datos sin procesar.
-   El **calificador CookType** especifica la fórmula [COOKER \_ MIN](cooker-min.md) para calcular los datos.
-   El **calificador SampleWindow** especifica el número de muestras que se deben tomar antes de realizar el cálculo.


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

En el siguiente ejemplo de código de script se obtienen estadísticas sobre la memoria disponible, en megabytes, mediante el MOF creado anteriormente. El script usa el objeto de scripting [**SWbemRefresher**](swbemrefresher.md) para crear un actualizador que contiene una instancia de la clase de estadísticas que crea el archivo MOF, que es **\_ Win32 PerfFormattedData \_ MemoryStatistics.** Para obtener más información sobre el uso de scripts, vea [Actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md). Si trabaja en C++, vea [Acceso a datos de rendimiento en C++.](accessing-performance-data-in-c--.md)

> [!Note]  
> [**Se debe llamar a SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) después de obtener el elemento de la llamada a [**SWbemRefresher.Add**](swbemrefresher-add.md) o se producirá un error en el script. [**Se debe llamar a SWbemRefresher.Refresh**](swbemrefresher-refresh.md) antes de entrar en el bucle para obtener valores de línea base, o bien las propiedades estadísticas son cero (0) en el primer paso.

 


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



## <a name="running-the-script"></a>Ejecución del script

En el procedimiento siguiente se describe cómo ejecutar el ejemplo.

**Para ejecutar el script de ejemplo**

1.  Copie el código MOF y el script en los archivos del equipo.
2.  Dé al archivo MOF una extensión .mof y al archivo de script una descripción de .vbs.
3.  En la línea de comandos, cambie al directorio donde se almacenan los archivos y ejecute [**Mofcomp**](mofcomp.md) en el archivo MOF. Por ejemplo, si se llama al *archivo CalculatedData.mof*, el comando es **Mofcomp** *CalculatedData.mof.*
4.  Ejecute el script.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Acceso a clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Calificadores de propiedad para clases de contadores de rendimiento con formato**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipos de contadores estadísticos](statistical-counter-types.md)
</dt> </dl>

 

 
