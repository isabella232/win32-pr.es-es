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
# <a name="class-qualifiers-for-performance-counter-classes"></a>Calificadores de clase para las clases de contador de rendimiento

Los calificadores de clase especifican información sobre el objeto de rendimiento al que está asignada la [clase de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI. Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md).

-   [Calificadores para PerformanceClasses sin formato y con formato](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Calificadores para clases de rendimiento sin procesar](#)
-   [Calificadores para clases de rendimiento con formato](#)
-   [Temas relacionados](#related-topics)


El proveedor "WbemPerfClass" asocia automáticamente los calificadores específicos del contador de rendimiento a las clases y propiedades de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) en la raíz \\ CIMv2.

Esta información se aplica a todas las instancias de la clase. Algunos calificadores con valores **booleanos** que son siempre **false** pueden no estar presentes en clases específicas.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Calificadores para PerformanceClasses sin formato y con formato

Los calificadores siguientes se aplican a todas las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cocida**
</dt> <dd>

**boolean**

Indica si la clase contiene datos cocidos.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**
</dt> <dd>

**string**

Nombre del objeto de rendimiento. Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

No proporciona datos detallados. Siempre contiene el valor 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinámica**
</dt> <dd>

**boolean**

Siempre se establece en **true** porque las instancias siempre son dinámicas.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

Indica si la clase procede de una biblioteca de rendimiento heredada. Siempre se establece en **true**.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Los índices ya no son válidos. Este calificador siempre es cero.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Indica que la clase es una clase de alto rendimiento. Siempre se establece en **true**.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Configuración regional**
</dt> <dd>

**sint32**

Identificador de configuración regional. El valor siempre es 1033 (Inglés de EE. UU.).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

Los índices ya no son válidos. Este calificador siempre es cero.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Presta**
</dt> <dd>

**string**

Nombre del proveedor de instancias. El valor es "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**Rename**
</dt> <dd>

**string**

Nombre del controlador en la clave **HKEY \_ local \_ Machine \\ CurrentControlSet \\ Services** , en la que se puede encontrar la clave de rendimiento. Este nombre también es el nombre del servicio que proporciona el contador de rendimiento.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Simple**
</dt> <dd>

**boolean**

Si **es true**, indica que solo existe una instancia de la clase.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Calificadores para clases de rendimiento sin procesar

Los calificadores siguientes se aplican a todas las clases que se derivan de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costoso**
</dt> <dd>

**boolean**

Indica si la obtención de instancias de esta clase es una operación costosa. Siempre se establece en **true** para las clases con " \_ Costly" anexadas al final del nombre de clase.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

No proporciona datos detallados. Siempre contiene el valor 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

El valor siempre es **false**.

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Calificadores para clases de rendimiento con formato

Los calificadores siguientes se aplican a todas las clases que se derivan de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autocook**
</dt> <dd>

**int32**

Indica que los valores de las instancias de clase se calculan automáticamente a partir de la clase de datos sin procesar correspondiente. El valor es siempre 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**Autocook \_ RawClass**
</dt> <dd>

**string**

Nombre de la clase sin procesar que se va a usar para el cálculo de la clase con formato. Este calificador es obligatorio.

</dd> </dl>

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

 

 
