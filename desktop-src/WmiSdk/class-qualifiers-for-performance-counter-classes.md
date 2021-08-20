---
description: Especifique información sobre el objeto de rendimiento al que está asignada la clase de contador de rendimiento WMI.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Calificadores de clase para clases de contador de rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b8168dcc0523c629202ac4d5c4a0ea51ecc8bd68d5ac4498fb38059b940fd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820122"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Calificadores de clase para clases de contador de rendimiento

Los calificadores de clase especifican información sobre el objeto de rendimiento al que está asignada la clase de [contador](/windows/desktop/CIMWin32Prov/performance-counter-classes) de rendimiento WMI. Para obtener más información, vea [Supervisión de datos de rendimiento.](monitoring-performance-data.md)

-   [Calificadores para performanceClasses sin formato y sin formato](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Calificadores para clases de rendimiento sin procesar](#)
-   [Calificadores para clases de rendimiento con formato](#)
-   [Temas relacionados](#related-topics)


El proveedor "WbemPerfClass" adjunta automáticamente los calificadores específicos del contador de rendimiento a las clases y propiedades [**\_ de Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) en la \\ CIMv2 raíz.

Esta información se aplica a todas las instancias de la clase . Es posible que algunos **calificadores con** valores booleanos que siempre son **False** no estén presentes en clases específicas.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Calificadores para performanceClasses sin formato y sin formato

Los siguientes calificadores se aplican a todas las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cocinado**
</dt> <dd>

**boolean**

Indica si la clase contiene datos cociados.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
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

Establezca siempre en **True** porque las instancias siempre son dinámicas.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

Indica si la clase procede de una biblioteca de rendimiento heredada. Establezca siempre en **True.**

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Los índices ya no son válidos. Este calificador siempre es cero.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Indica que la clase es una clase de alto rendimiento. Establezca siempre en **True.**

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Configuración regional**
</dt> <dd>

**sint32**

Identificador de configuración regional. El valor siempre es 1033 (inglés de EE. UU.).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

Los índices ya no son válidos. Este calificador siempre es cero.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Proveedor**
</dt> <dd>

**string**

Nombre del proveedor de instancias. El valor es "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**string**

Nombre del controlador en la clave **HKEY \_ LOCAL MACHINE \_ \\ CurrentControlSet \\ Services,** en la que se puede encontrar la clave de rendimiento. Este nombre también es el nombre del servicio que proporciona el contador de rendimiento.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

**boolean**

Si **es True**, indica que solo existe una instancia de la clase .

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Calificadores para clases de rendimiento sin procesar

Los siguientes calificadores se aplican a todas las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costoso**
</dt> <dd>

**boolean**

Indica si la obtención de instancias de esta clase es una operación costosa. Establezca siempre en **True para** las clases con \_ "Costly" anexado al final del nombre de clase.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

No proporciona datos detallados. Siempre contiene el valor 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

El valor siempre es **False.**

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Calificadores para clases de rendimiento con formato

Los siguientes calificadores se aplican a todas las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**
</dt> <dd>

**int32**

Indica que los valores de las instancias de clase se calculan automáticamente a partir de la clase de datos sin procesar correspondiente. El valor siempre es 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook \_ RawClass**
</dt> <dd>

**string**

Nombre de la clase sin formato que se usará para el cálculo de la clase con formato. Este calificador es obligatorio.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> <dt>

[Calificadores específicos de las clases de rendimiento wmi](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acceso a clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
