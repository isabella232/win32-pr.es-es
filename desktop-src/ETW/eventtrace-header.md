---
description: Clase de tipo de evento para el evento de encabezado del archivo de registro. Esta clase contiene información sobre la sesión de seguimiento de eventos.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542510"
---
# <a name="eventtrace_header-class"></a>\_Clase de encabezado eventtracer

Clase de tipo de evento para el evento de encabezado del archivo de registro. Esta clase contiene información sobre la sesión de seguimiento de eventos.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a>Miembros

La clase de **\_ encabezado eventtracer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ encabezado eventtracer** tiene estas propiedades.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (17)
</dt> </dl>

Hora a la que se inició el sistema, en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Tamaño de los búferes de la sesión de seguimiento de eventos, en kilobytes.

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (21)
</dt> </dl>

Número total de búferes perdidos.

</dd> <dt>

**BuffersWritten**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Número total de búferes escritos por la sesión de seguimiento de eventos.

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13)
</dt> </dl>

Velocidad de la CPU, en megahercios.

**Windows 2000:** No compatible.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Hora a la que se detuvo la sesión de seguimiento de eventos en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601. Este valor puede ser 0 si está consumiendo eventos en tiempo real o desde un archivo de registro en el que el proporcionado todavía está registrando eventos.

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12)
</dt> </dl>

Número de eventos perdidos durante la sesión de seguimiento de eventos.

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), **formato ("x")**
</dt> </dl>

Modo de registro actual para la sesión de seguimiento de eventos. Para obtener una lista de valores, vea constantes del modo de registro.

</dd> <dt>

**NombreDeArchivoDeRegistro**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15), **puntero**
</dt> </dl>

Nombre del archivo de registro de seguimiento de eventos que contiene los eventos.

</dd> <dt>

**LoggerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14), **puntero**
</dt> </dl>

Nombre de la sesión de seguimiento de eventos.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Tamaño máximo del archivo de registro, en megabytes.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Número de procesadores del sistema.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (18)
</dt> </dl>

Frecuencia del contador de rendimiento de alta resolución, si existe.

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Tamaño de un tipo de datos de puntero, en bytes.

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Número de compilación del sistema operativo.

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (20)
</dt> </dl>

Reservado.

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10)
</dt> </dl>

Reservado.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (19)
</dt> </dl>

Hora a la que se inició la sesión de seguimiento de eventos, en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6)
</dt> </dl>

Resolución del temporizador de hardware, en unidades de 100 nanosegundos.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (16), **extensión ("noprint")**, **Max** (176)
</dt> </dl>

Estructura [**de \_ \_ información de zona horaria**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) que contiene la zona horaria para los miembros **BootTime**, **EndTime** y **startTime** .

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Número de versión del sistema operativo. A partir de los bytes de orden inferior, los dos primeros bytes contienen la versión principal, los dos bytes siguientes contienen la versión secundaria, los dos bytes siguientes contienen Service Pack versión principal y los dos últimos bytes contienen Service Pack versión secundaria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente, desea guardar los valores de las siguientes propiedades para su uso posterior al procesar eventos del archivo de registro.

-   **TimerResolution**: se usa con los miembros **KernelTime** y **UserTime** de la estructura de [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para determinar el costo de CPU para un conjunto de instrucciones. Para obtener más información, vea la sección Comentarios del [**\_ \_ encabezado de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).
-   **PointerSize**: para las propiedades que contienen el calificador de **puntero** , use este valor para determinar el tamaño del puntero. Tenga en cuenta que este valor puede no ser preciso. Por ejemplo, en un equipo de 64 bits, una aplicación de 32 bits registra punteros de 4 bytes; sin embargo, la sesión establecerá **PointerSize** en 8.
-   **LogFileMode**: se usa para determinar si esta sesión es una sesión de registrador privada. Hay algunas propiedades que no contienen datos para las sesiones del registrador privado. Por ejemplo, los miembros **KernelTime** y **UserTime** de la estructura de [**\_ \_ encabezado de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**encabezado de archivo de registro de seguimiento \_ \_**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
