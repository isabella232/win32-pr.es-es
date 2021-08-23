---
description: Clase base abstracta para las clases de datos calculadas preinstaladas.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 55a765102d5fcc40caff41a7fa68184afea114838152dd84157d506a62c15da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020143"
---
# <a name="win32_perfformatteddata-class"></a>Clase \_ PerfFormattedData de Win32

Clase base abstracta para las clases de datos calculadas preinstaladas. Un ejemplo de este tipo de clase [**es Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). Estas clases contienen valores calculados proporcionados por el proveedor de datos de rendimiento con formato [de alto rendimiento](../wmisdk/formatted-performance-data-provider.md).

La sintaxis siguiente se simplifica a partir del código MOF y muestra todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
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

La **clase \_ PerfFormattedData de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PerfFormattedData de Win32** tiene estas propiedades.

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

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Frequency \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en tics por segundo de **la propiedad Frequency \_ PerfTime.** Se puede obtener un valor llamando a la Windows [**función QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Frecuencia \_ sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en tics por segundo de la propiedad **\_ Timestamp Sys100NS** (10000000).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

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

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Timestamp \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo del contador de alto rendimiento. Se puede obtener un valor llamando a la Windows [**función QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Timestamp \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de marca de tiempo en unidades de 100 nanosegundos.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**Win32 \_ Perf**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PerfFormattedData de Win32** se deriva de [**Win32 \_ Perf**](win32-perf.md), que se deriva de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md). La clase se encuentra en el espacio **de \\ nombres cimv2** raíz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                             |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 
