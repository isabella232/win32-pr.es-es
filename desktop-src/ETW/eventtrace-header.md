---
description: Clase de tipo de evento para el evento de encabezado del archivo de registro. Esta clase contiene información sobre la sesión de seguimiento de eventos.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header clase
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
ms.openlocfilehash: a5d0515b9d7d720409e0a72aec7aad5dc54561637563976a35d03b3e0dec79f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829995"
---
# <a name="eventtrace_header-class"></a>Clase EventTrace \_ Header

Clase de tipo de evento para el evento de encabezado del archivo de registro. Esta clase contiene información sobre la sesión de seguimiento de eventos.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase EventTrace \_ Header** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase EventTrace \_ Header** tiene estas propiedades.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (17)
</dt> </dl>

Hora a la que se inició el sistema, en intervalos de 100 nanosegundos desde la medianoche del 1 de enero de 1601.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Tamaño de los búferes de la sesión de seguimiento de eventos, en kilobytes.

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (21)
</dt> </dl>

Número total de búferes perdidos.

</dd> <dt>

**BuffersWritten**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Número total de búferes escritos por la sesión de seguimiento de eventos.

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13)
</dt> </dl>

Velocidad de CPU, en megahercios.

**Windows 2000:** No se admite.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Hora a la que se detuvo la sesión de seguimiento de eventos, en intervalos de 100 nanosegundos desde la medianoche del 1 de enero de 1601. Este valor puede ser 0 si está consumiendo eventos en tiempo real o desde un archivo de registro en el que la proporciona todavía está registrando eventos.

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12)
</dt> </dl>

Número de eventos perdidos durante la sesión de seguimiento de eventos.

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), **Format("x")**
</dt> </dl>

Modo de registro actual para la sesión de seguimiento de eventos. Para obtener una lista de valores, vea Constantes de modo de registro.

</dd> <dt>

**LogFileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15), **Pointer**
</dt> </dl>

Nombre del archivo de registro de seguimiento de eventos que contiene los eventos.

</dd> <dt>

**LoggerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14), **Pointer**
</dt> </dl>

Nombre de la sesión de seguimiento de eventos.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Tamaño máximo del archivo de registro, en megabytes.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Número de procesadores del sistema.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (18)
</dt> </dl>

Frecuencia del contador de rendimiento de alta resolución, si existe uno.

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Tamaño de un tipo de datos de puntero, en bytes.

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Número de compilación del sistema operativo.

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (20)
</dt> </dl>

Reservado.

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10)
</dt> </dl>

Reservado.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (19)
</dt> </dl>

Hora a la que se inició la sesión de seguimiento de eventos, en intervalos de 100 nanosegundos desde la medianoche del 1 de enero de 1601.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6)
</dt> </dl>

Resolución del temporizador de hardware, en unidades de 100 nanosegundos.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)
</dt> </dl>

Estructura [**TIME \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) que contiene la zona horaria de los miembros **BootTime**, **EndTime** **y StartTime.**

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Número de versión del sistema operativo. A partir de los bytes de orden bajo, los dos primeros bytes contienen la versión principal, los dos bytes siguientes contienen la versión secundaria, los dos bytes siguientes contienen la versión principal del Service Pack y los dos últimos bytes contienen la versión secundaria del Service Pack.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Normalmente, desea guardar los valores de las siguientes propiedades para usarlos más adelante al procesar eventos desde el archivo de registro.

-   **TimerResolution:** use con los miembros **KernelTime** y **UserTime** de la estructura [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para determinar el costo de CPU de un conjunto de instrucciones. Para obtener más información, vea la sección Comentarios de [**EVENT \_ TRACE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).
-   **PointerSize:** para las propiedades que contienen el calificador **Pointer,** use este valor para determinar el tamaño del puntero. Tenga en cuenta que este valor puede no ser preciso. Por ejemplo, en un equipo de 64 bits, una aplicación de 32 bits registrará punteros de 4 bytes; sin embargo, la sesión establecerá **PointerSize** en 8.
-   **LogFileMode**: se usa para determinar si esta sesión es una sesión de registrador privado. Hay algunas propiedades que no contienen datos para las sesiones del registrador privado. Por ejemplo, los **miembros KernelTime** y **UserTime** de la [**estructura EVENT TRACE \_ \_ HEADER.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**ENCABEZADO \_ LOGFILE \_ DE SEGUIMIENTO**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
