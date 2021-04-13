---
description: La clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData (clase)
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
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539357"
---
# <a name="win32_perfrawdata-class"></a>\_Clase Win32 PerfRawData

La clase base abstracta para todas las clases de contador de rendimiento sin procesar concretas.

Para que aparezca en el monitor de sistema, las clases de contador de rendimiento se deben agregar al \\ espacio de nombres root cimv2 y derivarse de **Win32 \_ PerfRawData**. Los datos de estas clases son proporcionados por el [proveedor de contador de rendimiento](../wmisdk/performance-counter-provider.md)de alto rendimiento.

Las siguientes propiedades se heredan cuando una clase se deriva de **Win32 \_ PerfRawData**:

-   **Marca de tiempo \_ PerfTime**
-   **Marca de tiempo \_ Sys100NS**
-   **Timestamp ( \_ objeto)**
-   **Frecuencia \_ PerfTime**
-   **Frecuencia \_ Sys100NS**
-   **Frequency ( \_ objeto)**

En cada caso, las propiedades deben ser rellenadas por el proveedor o la clase no se puede mostrar en el monitor del sistema. Estas propiedades se utilizan para calcular las fórmulas de tipo de contador por parte de los consumidores de datos de rendimiento.

La siguiente sintaxis se simplifica desde el código MOF y muestra todas las propiedades heredadas.

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

La **clase \_ PerfRawData de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PerfRawData de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual de la estadística o la métrica.

Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual de la estadística o la métrica.

Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**Frequency ( \_ objeto)**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en TICs por segundo de la propiedad **de \_ objeto timestamp** . Cuando se subclase, el proveedor define esta propiedad.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).

</dd> <dt>

**Frecuencia \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en TICs por segundo de la propiedad **\_ PerfTime** de la frecuencia. Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).

</dd> <dt>

**Frecuencia \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Frecuencia en TICs por segundo de la propiedad **timestamp \_ Sys100NS** (10 millones).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Etiqueta por la que se conoce la estadística o la métrica. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

</dd> <dt>

**Timestamp ( \_ objeto)**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo definida por el objeto. El proveedor define su propiedad.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).

</dd> <dt>

**Marca de tiempo \_ PerfTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo de contador de alto rendimiento. Un valor se puede obtener llamando a la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)de Windows.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).

</dd> <dt>

**Marca de tiempo \_ Sys100NS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de marca de tiempo en unidades de 100 nanosegundos.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**los \_ rendimientos de Win32**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ PerfRawData de Win32** se deriva de los [**\_ rendimientos de Win32**](win32-perf.md), que se derivan de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).

Todas las clases derivadas de [**\_ rendimiento de Win32**](win32-perf.md) están diseñadas para usarse con un objeto [*actualizador*](../wmisdk/gloss-r.md) . Para obtener más información sobre cómo crear y usar un objeto actualizador en el lenguaje de programación C++, vea [obtener acceso a los datos de rendimiento en C++](../wmisdk/accessing-performance-data-in-c--.md). Para obtener más información sobre cómo crear y usar un objeto actualizador en un lenguaje de programación de scripts, vea [actualizar datos WMI en scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                             |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Rendimiento de Win32 \_**](win32-perf.md)
</dt> <dt>

[Clases de contador de rendimiento](performance-counter-classes.md)
</dt> <dt>

[Obtener acceso a las clases de rendimiento preinstaladas de WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tareas WMI: supervisión del rendimiento](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Obtener acceso a los datos de rendimiento del script](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
