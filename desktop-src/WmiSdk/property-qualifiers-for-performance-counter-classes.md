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
# <a name="property-qualifiers-for-performance-counter-classes"></a>Calificadores de propiedad para las clases de contador de rendimiento

Los calificadores de propiedad especifican información sobre el contador de rendimiento al que se asigna la propiedad.

-   [Calificadores de propiedad para las clases de rendimiento RAW y con formato](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Calificadores de propiedad para las clases de rendimiento sin procesar](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Calificadores de propiedad para las clases de rendimiento con formato](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Cómo interpretar calificadores de propiedad](#how-to-interpret-property-qualifiers)
-   [Temas relacionados](#related-topics)

El contador de rendimiento forma parte de un objeto de rendimiento representado por un contador de rendimiento de [clase de contador](/windows/desktop/CIMWin32Prov/performance-counter-classes) de rendimiento de WMI: el proveedor WbemPerfClass asocia automáticamente calificadores específicos a las clases y propiedades de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) en la raíz \\ CIMv2.

Esta información se aplica a todas las instancias de la clase de rendimiento. Algunos calificadores con valores **booleanos** que son siempre false pueden no estar presentes en clases específicas.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Calificadores de propiedad para las clases de rendimiento RAW y con formato

En la lista siguiente se enumeran los calificadores que se aplican a las propiedades de las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) o [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**Tipo**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Valor entero en la enumeración de tipo de contador, tal y como se define en WINPERF. h o Perflib. h. El calificador de [**contratipo**](countertype-qualifier.md)indica la fórmula o el algoritmo que se usa para calcular el valor que se muestra en el monitor de sistema para el contador que representa la propiedad.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**
</dt> <dd>

**string**

Nombre del contador de rendimiento, según lo especificado por el ayudante de datos de rendimiento (PDH).

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

No se utiliza. Siempre contiene 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

No se utiliza. Siempre contiene 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Calificadores de propiedad para las clases de rendimiento sin procesar

En la lista siguiente se enumeran los calificadores que se aplican a todas las propiedades de las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Indica si esta propiedad es el contador predeterminado que se va a usar en los cuadros de lista. Este calificador tiene como valor predeterminado **false** para los contadores de rendimiento versión 6,0 porque no proporcionan datos para él. Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**
</dt> <dd>

**sint32**

Potencia de 10 que se va a usar para mostrar el contador. Para cero, el máximo estimado es 10 ^ 0 o 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Nivel de conocimientos de audiencia. No se utiliza. El valor siempre es 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Calificadores de propiedad para las clases de rendimiento con formato

En la lista siguiente se enumeran los calificadores que se aplican a todas las propiedades de las clases que se derivan de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**
</dt> <dd>

**string**

Tipo de fórmula usado para generar el resultado. Cada tipo de contador usa los otros calificadores de propiedad para calcular el resultado mostrado como el valor de la propiedad actual. Los calificadores **Counter**, **PerfTimeStamp** y **PerfTimeFreq** se asignan a las propiedades de una clase sin procesar que proporcionan los datos.

Para obtener más información, vea [calificador de tipo contratype](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Bloque**
</dt> <dd>

**string**

Nombre de una propiedad necesaria en la clase sin procesar correspondiente que se va a usar como valor de contador en la fórmula de cocina. El valor debe ser el nombre de la propiedad de origen de datos en la clase sin formato correspondiente.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**string**

Nombre de una propiedad de una clase sin procesar que se va a usar como una frecuencia en la fórmula de cocina. Se usará el valor predeterminado adecuado en el nivel de clase si este calificador no está presente para la propiedad. La frecuencia representa los tics por segundo de la marca de tiempo.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**string**

Nombre de una propiedad de una clase sin procesar que se va a usar como marca de tiempo en la fórmula de cocina. Se utiliza el valor predeterminado adecuado en el nivel de clase si este calificador no está presente para la propiedad. Una marca de tiempo generada automáticamente puede producir un error en un cálculo porque la marca de tiempo es una aproximación y no tiene en cuenta la sobrecarga generada por el cálculo de referencias y la recopilación de datos real.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Cómo interpretar calificadores de propiedad

Las propiedades de las clases [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen los datos calculados proporcionados por el [proveedor de datos de rendimiento con formato](formatted-performance-data-provider.md). El valor de la propiedad es el resultado calculado final. Los calificadores proporcionan una receta.

El **contador** y los calificadores **base** apuntan a los orígenes de datos y **CookingType** especifica la fórmula que se usa para generar el resultado. La marca de tiempo y la frecuencia de muestra también proceden de la clase sin procesar correspondiente y se denominan en **PerfTimeStamp** y **PerfTimeFreq**.

Por ejemplo, una de las clases con formato suministradas por WMI, [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contiene una propiedad denominada **AvgDiskBytesPerRead**. El nombre de la propiedad en la clase con formato debe ser el mismo que el de la propiedad de la clase sin formato. La propiedad **AvgDiskBytesPerRead** tiene los calificadores siguientes.

En la lista siguiente se enumeran los calificadores de propiedad disponibles para las propiedades de todas las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).



| Qualifier         | Value                     |
|-------------------|---------------------------|
| **CookingType**   | media de rendimiento en \_ \_ masa       |
| **Contador**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | Marca de tiempo \_ PerfTime       |
| **PerfTimeFreq**  | Frecuencia \_ PerfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **Básica**          | Base de AvgDiskBytesPerRead \_ |



 

La propiedad **AvgDiskBytesPerRead** informa del número promedio de bytes transferidos desde el disco durante las operaciones de lectura. La fórmula para la \_ media de rendimiento \_ masiva es:

(Sample2-Sample1)/(base Sample2-base Sample1)

La operación de lectura se muestrea con la frecuencia especificada por **PerfTimeFreq** con el valor **PerfTimeStamp** que indica el ejemplo más reciente. Los datos del contador sin formato en bytes se toman de la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) . El número base de datos de operaciones se toma de la propiedad **\_ base AvgDiskBytesPerRead** en esa misma clase.

Para obtener más información, consulte [obtención de datos de rendimiento estadísticos](obtaining-statistical-performance-data.md) y [supervisión de datos de rendimiento](monitoring-performance-data.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Calificadores específicos de las clases de rendimiento de WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Obtener acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tareas WMI: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
