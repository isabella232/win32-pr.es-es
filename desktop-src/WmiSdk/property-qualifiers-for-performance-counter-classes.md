---
description: Los calificadores de propiedad especifican información sobre el contador de rendimiento al que se asigna la propiedad.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Calificadores de propiedad para clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 105bd010704364dc3865b2e704b3daeaafdb29a772d4f3b3fe036b88da2d43cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996185"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>Calificadores de propiedad para clases de contador de rendimiento

Los calificadores de propiedad especifican información sobre el contador de rendimiento al que se asigna la propiedad.

-   [Calificadores de propiedad para clases de rendimiento sin formato y con formato](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Calificadores de propiedad para clases de rendimiento sin procesar](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Calificadores de propiedad para clases de rendimiento con formato](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Interpretación de calificadores de propiedad](#how-to-interpret-property-qualifiers)
-   [Temas relacionados](#related-topics)

El contador de rendimiento forma parte de un objeto de rendimiento representado por una clase de contador de rendimiento [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) Los calificadores específicos del contador de rendimiento se adjuntan automáticamente por el proveedor WbemPerfClass a las clases y propiedades [**de Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) en \\ la CIMv2 raíz.

Esta información se aplica a todas las instancias de la clase de rendimiento. Es posible que algunos **calificadores con** valores booleanos que siempre son false no estén presentes en clases específicas.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Calificadores de propiedad para clases de rendimiento sin formato y con formato

En la lista siguiente se enumeran los calificadores que se aplican a las propiedades de las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) o [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Valor entero en la enumeración de tipo de contador, tal como se define en Winperf.h o Perflib.h. El [**calificador CounterType**](countertype-qualifier.md)indica la fórmula o el algoritmo usados para calcular el valor que se muestra en el Monitor de sistema para el contador que representa la propiedad .

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

**string**

Nombre del contador de rendimiento, tal y como especifica el Asistente de datos de rendimiento (PDH).

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

No se usa. Siempre contiene 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

No se usa. Siempre contiene 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Calificadores de propiedad para clases de rendimiento sin procesar

En la lista siguiente se enumeran los calificadores que se aplican a todas las propiedades de las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Indica si esta propiedad es el contador predeterminado que se va a usar en los cuadros de lista. Este calificador tiene como valor **predeterminado False para** los contadores de rendimiento versión 6.0 porque no le suministran datos. Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**
</dt> <dd>

**sint32**

Potencia de 10 que se usará para mostrar el contador. Para cero, el máximo estimado es 10^0 o 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Nivel de conocimiento del público. No se usa. El valor siempre es 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Calificadores de propiedad para clases de rendimiento con formato

En la lista siguiente se enumeran los calificadores que se aplican a todas las propiedades de las clases que se derivan de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Tipo de cocina**
</dt> <dd>

**string**

Tipo de fórmula utilizado para generar el resultado. Cada tipo de contador usa los demás calificadores de propiedad para calcular el resultado que se muestra como el valor de la propiedad actual. Los **calificadores Counter**, **PerfTimeStamp** y **PerfTimeFreq** se asignan a las propiedades de una clase sin formato que proporciona los datos.

Para obtener más información, vea [Calificador CounterType](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contador**
</dt> <dd>

**string**

Nombre de una propiedad obligatoria en la clase sin formato correspondiente que se usará como valor de contador en la fórmula de cocina. El valor debe ser el nombre de propiedad de la propiedad de origen de datos en la clase sin formato correspondiente.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**string**

Nombre de una propiedad de una clase sin formato que se usará como frecuencia en la fórmula de cocina. El valor predeterminado adecuado en el nivel de clase se usará si este calificador no está presente para la propiedad . La frecuencia representa los tics por segundo de la marca de tiempo.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**string**

Nombre de una propiedad de una clase sin formato que se usará como marca de tiempo en la fórmula de cocina. El valor predeterminado adecuado en el nivel de clase se usa si este calificador no está presente para la propiedad . Una marca de tiempo generada automáticamente puede producir un error en un cálculo porque la marca de tiempo es una aproximación y no tiene en cuenta la sobrecarga en la que incurre la serialización y la recopilación de datos reales.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Interpretación de calificadores de propiedad

Las propiedades de [**las clases \_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen los datos calculados proporcionados por el proveedor de datos de rendimiento con [formato](formatted-performance-data-provider.md). El valor de propiedad es el resultado calculado final. Los calificadores suministran una receta.

Los **calificadores Counter** **y Base** apuntan a los orígenes de datos y **CookingType** especifica la fórmula utilizada para generar el resultado. La marca de tiempo y la frecuencia de ejemplo también proceden de la clase sin procesar correspondiente y se denominan **en PerfTimeStamp** y **PerfTimeFreq.**

Por ejemplo, una de las clases con formato proporcionadas por WMI, [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contiene una propiedad denominada **AvgDiskBytesPerRead**. El nombre de la propiedad de la clase con formato debe ser el mismo que la propiedad de la clase sin formato. La **propiedad AvgDiskBytesPerRead** tiene los siguientes calificadores.

En la lista siguiente se enumeran los calificadores de propiedad disponibles para las propiedades de todas las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).



| Qualifier         | Value                     |
|-------------------|---------------------------|
| **Tipo de cocina**   | PERF \_ AVERAGE \_ BULK       |
| **Contador**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | Timestamp \_ PerfTime       |
| **PerfTimeFreq**  | Frequency \_ PerfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **Base**          | AvgDiskBytesPerRead \_ Base |



 

La **propiedad AvgDiskBytesPerRead** informa del número medio de bytes transferidos desde el disco durante las operaciones de lectura. La fórmula de PERF \_ AVERAGE \_ BULK es:

(Sample2 - Sample1) / (Base Sample2 - Base Sample1)

La operación de lectura se muestrea con la frecuencia especificada por **PerfTimeFreq con** el valor **PerfTimeStamp** que indica el ejemplo más reciente. Los datos del contador sin procesar en bytes se toman de la propiedad **AvgDiskBytesPerRead** de la clase [**\_ \_ \_ LogicalDisk PerfRawData de Win32.**](./retrieving-raw-and-formatted-performance-data.md) El número base de datos de operaciones se toma de **la propiedad AvgDiskBytesPerRead \_ Base** en esa misma clase.

Para obtener más información, vea [Obtener datos estadísticos de rendimiento y](obtaining-statistical-performance-data.md) Supervisar datos de [rendimiento](monitoring-performance-data.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Calificadores específicos de las clases de rendimiento wmi](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Clases de contadores de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acceso a clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
