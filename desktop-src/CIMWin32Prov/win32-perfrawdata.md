---
description: Clase base abstracta para todas las clases de contadores de rendimiento sin procesar concretas.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData clase
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
ms.openlocfilehash: f6500706b7e2298ad98aa894e33436b0306e406e003562fcb6533265abd0b2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020133"
---
# <a name="win32_perfrawdata-class"></a>Clase \_ Win32 PerfRawData

Clase base abstracta para todas las clases de contadores de rendimiento sin procesar concretas.

Para aparecer en el Monitor de sistema, las clases de contador de rendimiento deben agregarse al espacio de nombres cimv2 raíz y \\ derivarse de **Win32 \_ PerfRawData**. El proveedor de contadores de rendimiento de alto rendimiento proporciona los datos [de estas clases.](../wmisdk/performance-counter-provider.md)

Las propiedades siguientes se heredan cuando una clase se deriva de **Win32 \_ PerfRawData**:

-   **Timestamp \_ PerfTime**
-   **Timestamp \_ Sys100NS**
-   **Objeto \_ Timestamp**
-   **Frequency \_ PerfTime**
-   **Frecuencia \_ Sys100NS**
-   **Frequency \_ (objeto)**

En cada caso, el proveedor debe rellenar las propiedades o la clase no se puede mostrar en el Monitor de sistema. Estas propiedades se usan para calcular las fórmulas de tipo de contador por parte de los consumidores de datos de rendimiento.

La sintaxis siguiente se simplifica a partir del código MOF y muestra todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La **clase \_ Win32 PerfRawData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Win32 PerfRawData** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual de la estadística o métrica.

Esta propiedad se hereda de [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual de la estadística o métrica.

Esta propiedad se hereda de [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Frequency \_ (objeto)**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en tics por segundo de la propiedad **Timestamp \_ Object.** Cuando se clasifica con subclases, el proveedor define esta propiedad.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en pasos por segundo de la **propiedad Frequency \_ PerfTime.** Se puede obtener un valor llamando a la Windows función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Frecuencia \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en pasos por segundo de la propiedad **\_ Timestamp Sys100NS** (10000000).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Etiqueta por la que se conoce la estadística o métrica. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ StatisticalInformation.**](cim-statisticalinformation.md)

</dd> <dt>

**Objeto \_ Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo definida por el objeto. El proveedor define su propiedad .

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo del contador de alto rendimiento. Se puede obtener un valor llamando a la Windows función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de marca de tiempo en unidades de 100 nanosegundos.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ Win32 PerfRawData** se deriva de [**Win32 \_ Perf**](win32-perf.md), que se deriva de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

Todas las clases derivadas de [**Win32 \_ Perf**](win32-perf.md) están diseñadas para usarse con un [*objeto de actualizador.*](../wmisdk/gloss-r.md) Para obtener más información sobre cómo crear y usar un objeto de actualizador en el lenguaje de programación C++, vea Acceso a datos [de rendimiento en C++.](../wmisdk/accessing-performance-data-in-c--.md) Para obtener más información sobre cómo crear y usar un objeto de actualizador en un lenguaje de programación de script, vea [Actualizar datos WMI en scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                             |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dt>

[Clases de contador de rendimiento](performance-counter-classes.md)
</dt> <dt>

[Acceso a clases de rendimiento preinstaladas de WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Acceso a datos de rendimiento en script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
