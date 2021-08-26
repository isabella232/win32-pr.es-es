---
description: Clase base para las clases de contador de rendimiento Win32 \_ PerfRawData y Win32 \_ PerfFormattedData.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 356fdba0e2ebb7fb202f4996daa6b1929cd61fc67b028f67e8b041748306c0ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972245"
---
# <a name="win32_perf-class"></a>Win32 \_ Perf (clase)

Clase base para las clases de contador de [**rendimiento Win32 \_ PerfRawData**](win32-perfrawdata.md) y [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

**Win32 \_ Perf define** las propiedades de marca de tiempo y frecuencia necesarias que se usan en los algoritmos [**CounterType**](../wmisdk/countertype-qualifier.md) para las clases de contador de rendimiento.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

La **clase Win32 \_ Perf** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Win32 Perf** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Descripción textual breve de la estadística o métrica.

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

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en tics por segundo de **la propiedad Frequency \_ PerfTime.** Se puede obtener un valor llamando a la Windows [**función QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Frecuencia \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en tics por segundo de la propiedad **\_ Timestamp Sys100NS** (10000000).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

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

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo del contador de alto rendimiento. Se puede obtener un valor llamando a la Windows [**función QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de marca de tiempo en unidades de 100 nanosegundos.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase Win32 \_ Perf** se deriva de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                             |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                     |
| Archivo DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dt>

[Clases de contador de rendimiento](performance-counter-classes.md)
</dt> <dt>

[Acceso a clases de rendimiento preinstaladas de WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Acceso a datos de rendimiento en script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
