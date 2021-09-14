---
description: La zona horaria \_ win32&\# 8194; La clase WMI representa la información de zona horaria de un sistema informático que ejecuta Windows, que incluye los cambios necesarios para la transición al horario de verano.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Win32_TimeZone clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974455"
---
# <a name="win32_timezone-class"></a>Clase TimeZone de Win32 \_

La clase  [WMI](../wmisdk/retrieving-a-class.md) **\_ TimeZone de Win32** representa la información de zona horaria de un sistema informático que ejecuta Windows, que incluye los cambios necesarios para la transición a la transición del horario de verano.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a>Members

La **clase \_ TimeZone de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TimeZone de Win32** tiene estas propiedades.

<dl> <dt>

**Sesgo**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE INFORMATION \| [**\_ \_ Bias"),**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Sesgo actual para la traducción de la hora local. El sesgo es la diferencia entre la hora universal coordinada (UTC) y la hora local. Todas las traducciones entre utc y hora local se basan en la fórmula siguiente: UTC = hora local - sesgo. Esta propiedad es obligatoria.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias"), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Valor de sesgo que se usará durante las traducciones de hora local que se producen durante el horario de verano. Esta propiedad se omite si no se proporciona un valor para la propiedad **DaylightDay.** El valor de esta propiedad se agrega a la propiedad **Bias** para formar el sesgo usado durante el horario de verano. En la mayoría de las zonas horarias, el valor de esta propiedad es -60.

</dd> <dt>

**Día de verano**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDay")
</dt> </dl>

**DaylightDayOfWeek del** **Mes** de verano cuando se produce la transición del horario estándar al horario de verano en este sistema operativo.

Ejemplo: si el día de transición (**DaylightDayOfWeek**) se produce en un domingo, el valor "1" indica el primer domingo del mes **de** verano , "2" indica el segundo domingo, y así sucesivamente. El valor "5" indica la última **daylightDayOfWeek** del mes.

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")
</dt> </dl>

Día de la semana en el que se produce la transición del horario estándar al horario de verano en un sistema operativo.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunes** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martes** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Miércoles** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jueves** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Viernes** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (6)


</dt> <dd></dd> </dl>

Ejemplo: 1

</dd> <dt>

**DaylightHour**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")
</dt> </dl>

Hora del día en la que se produce la transición del horario estándar al horario de verano en un sistema operativo.

Ejemplo: 2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")
</dt> </dl>

Milisegundo de **DaylightSecond cuando** se produce la transición del horario estándar al horario de verano en un sistema operativo.

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")
</dt> </dl>

Minuto del **horario de verano cuando** se produce la transición del horario estándar al horario de verano en un sistema operativo.

Ejemplo: 59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")
</dt> </dl>

Mes en el que se produce la transición del horario estándar al horario de verano en un sistema operativo.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Enero** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Febrero** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Marzo** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Abril** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mayo** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Junio** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Julio** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Septiembre** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Octubre** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Noviembre** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Diciembre** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**DaylightName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")
</dt> </dl>

Zona horaria que se representa cuando el horario de verano está en vigor.

Ejemplo: "EDT" (hora de verano del Este)

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")
</dt> </dl>

Segundo de **DaylightMinute** cuando se produce la transición del horario estándar al horario de verano en un sistema operativo.

Ejemplo: 59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")
</dt> </dl>

Año en el que está en vigor el horario de verano. Esta propiedad no es necesaria.

Ejemplo: 1997

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**StandardBias**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Valor de sesgo que se usará cuando el horario de verano no esté en vigor. Esta propiedad se omite si no se proporciona un valor para **StandardDay.** El valor de esta propiedad se agrega a la propiedad **Bias** para formar el sesgo durante el tiempo estándar.

Ejemplo: 0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")
</dt> </dl>

**StandardDayOfWeek del** **Mes** Estándar cuando se produce la transición del horario de verano al horario estándar en un sistema operativo.

Si el día de transición (**StandardDayOfWeek**) se produce en un domingo, el valor "1" indica el primer domingo del **Mes** Estándar, "2" indica el segundo domingo, y así sucesivamente. El valor "5" indica el último **StandardDayOfWeek** del mes.

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")
</dt> </dl>

Día de la semana en el que se produce la transición del horario de verano al horario estándar en un sistema operativo.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunes** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martes** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Miércoles** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jueves** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Viernes** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardHour**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")
</dt> </dl>

Hora del día en la que se produce la transición del horario de verano al horario estándar en un sistema operativo.

Ejemplo: 11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")
</dt> </dl>

Milisegundo de **StandardSecond cuando** se produce la transición del horario de verano al horario estándar en un sistema operativo.

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")
</dt> </dl>

Minuto de **StandardDay cuando** se produce la transición del horario de verano al horario estándar en un sistema operativo.

Ejemplo: 59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")
</dt> </dl>

Mes en el que se produce la transición del horario de verano al horario estándar en un sistema operativo.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Enero** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Febrero** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Marzo** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Abril** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mayo** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Junio** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Julio** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Septiembre** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Octubre** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Noviembre** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Diciembre** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Nombre de la zona horaria que se representa cuando está en vigor la hora estándar.

Ejemplo: "EST" (Hora estándar del Este)

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")
</dt> </dl>

Segundo de **StandardMinute** cuando se produce la transición del horario de verano al horario estándar en un sistema operativo.

Ejemplo: 59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de tiempo de Win32API \| TIME ZONE \| [**\_ \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")
</dt> </dl>

Año en el que está en vigor la hora estándar. Esta propiedad no es necesaria.

Ejemplo: 1997

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ TimeZone de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

No puede usar formatos de fecha y hora estándar (como 18/10/2002) al escribir consultas WMI. En su lugar, debe convertir las fechas usadas en las consultas al formato UTC. Esto requiere dos pasos: 1) Debe determinar el desplazamiento (diferencia en minutos) entre la zona horaria y la hora media de Greenwich, y 2) debe convertir 10/18/2002 en un valor UTC.

Determinar el desplazamiento de la hora media de Greenwich

Sin embargo, WMI dificulta el trabajo con fechas y horas. Afortunadamente, WMI al menos facilita la determinación del desplazamiento entre la zona horaria y la hora media de Greenwich. La clase WMI Win32 \_ TimeZone incluye una propiedad (Bias) que devuelve el desplazamiento GMT.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



Convertir una fecha en un valor UTC

Después de determinar el desplazamiento GMT, debe convertir una fecha estándar como 10/18/2002 a una fecha UTC. Para convertir una fecha estándar en una fecha UTC, puede usar funciones de fecha de VBScript como Year, Month y Day para aislar los componentes individuales que conste una fecha UTC. Después de tener valores individuales para estos componentes, puede concatenarlos de la misma manera que lo haría con cualquier otro valor de cadena. Las fechas UTC se tratan como cadenas porque el desplazamiento GMT debe anexarse al final. Si la fecha se ha visto como un número, este valor:

`20011018113047.000000-480`

Se trataría erróneamente como una ecuación matemática (paréntesis agregados para mayor claridad):

`(20011018113047.000000) - (480)`

Por ejemplo, en la fecha 18/10/2002, los componentes individuales son:

-   Año: 2002
-   Mes: 10
-   Día: 18

El script tendría que combinar estos tres valores, la cadena "113047.000000" (que representa la hora, incluidos los milisegundos) y el desplazamiento GMT para derivar una fecha UTC. Por ejemplo, (se han agregado paréntesis de nuevo para mayor claridad):

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> Puede usar las funciones de VBScript Hour, Minute y Second para convertir la parte de hora de una fecha UTC. Por lo tanto, una hora como 11:30:47 a.m. se convertiría en 113047.

 

Hay un factor complicante. El mes debe tomar las posiciones 5 y 6 de la cadena; el día debe tomar las posiciones 7 y 8. Esto no es un problema con el mes 10 y el día 18. Pero, ¿cómo se obtiene el 5 de julio (7 de mes, día 5) para rellenar las posiciones necesarias? La respuesta es agregar un cero inicial a cada valor, cambiando así el 7 a 07 y el 5 a 05.

Para ello, use la función VBScript Len para comprobar la longitud (número de caracteres) del mes y el día. Si la longitud es 1 (lo que significa que solo hay un carácter), agregue un cero inicial. Así:


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se convierte la fecha actual en una fecha UTC.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



El siguiente ejemplo de VBScript determina el desplazamiento GMT y, a continuación, convierte una fecha actual especificada (en este caso, 18/10/10/2002) al formato de fecha y hora UTC. Una vez convertida la fecha, ese valor se usa para buscar en un equipo y devuelve una lista de todas las carpetas que se crearon después del 18/10/2002.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



En el siguiente ejemplo de código de VBScript se muestra la configuración de las instancias de Win32 \_ TimeZone.


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Formato de fecha y hora](../wmisdk/date-and-time-format.md)
</dt> <dt>

[Tareas wmi: fechas y horas](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
