---
description: La estructura HEADER de WNODE \_ es miembro de la estructura EVENT TRACE \_ \_ PROPERTIES.
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER estructura (Wmistr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 93cecb900b0c62084a3b5ea4e4a7789575c20c27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480691"
---
# <a name="wnode_header-structure"></a>WNODE \_ HEADER (estructura)

La **estructura \_ WNODE HEADER** es miembro de la estructura EVENT TRACE [**\_ \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BufferSize**
</dt> <dd>

Tamaño total de la memoria asignada, en bytes, para las propiedades de la sesión de seguimiento de eventos. El tamaño de la memoria debe incluir el espacio para la estructura [**EVENT \_ TRACE \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) más la cadena de nombre de sesión y la cadena de nombre de archivo de registro que siguen a la estructura en memoria.

</dd> <dt>

**ProviderId**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

En la salida, identificador de la sesión de seguimiento de eventos.

</dd> <dt>

**Versión**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**Vinculación**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**KernelHandle**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**Timestamp**
</dt> <dd>

Hora a la que se actualizó la información de esta estructura, en intervalos de 100 nanosegundos desde la medianoche del 1 de enero de 1601.

</dd> <dt>

**Guid**
</dt> <dd>

GUID que se define para la sesión.

Para una sesión del registrador de kernel de NT, establezca este miembro en **SystemTraceControlGuid.**

Si este miembro se establece en **SystemTraceControlGuid** o **GlobalLoggerGuid,** el registrador será un registrador del sistema.

Para una sesión de registrador privado, establezca este miembro en el GUID del proveedor que va a habilitar para la sesión.

Si inicia una sesión que no es un registrador de kernel o una sesión de registrador privado, no tiene que especificar un GUID de sesión. Si no especifica un GUID, ETW crea uno automáticamente. Solo debe especificar un GUID de sesión si desea cambiar los permisos predeterminados asociados a una sesión específica. Para más información, consulte la función EventAccessControl.

No puede iniciar más de una sesión con el mismo GUID de sesión.

**Antes de Windows Vista:** Puede iniciar más de una sesión con el mismo GUID de sesión.

</dd> <dt>

**ClientContext**
</dt> <dd>

Resolución de reloj que se usará al registrar la marca de tiempo para cada evento. El valor predeterminado es Contador de rendimiento de consultas (QPC).

**Antes de Windows Vista:** El valor predeterminado es la hora del sistema.

**Antes de Windows 10, versión 1703:** Ningún registrador del sistema puede usar simultáneamente más de 2 tipos de reloj distintos.

**A partir Windows 10, versión 1703:** Se ha quitado la restricción de tipo de reloj. Los registradores del sistema ahora pueden usar los tres tipos de reloj simultáneamente.

Puede especificar uno de los siguientes valores.




| Valor | Significado | 
|-------|---------|
| <dl><dt>1</dt></dl> | Contador de rendimiento de consultas (QPC). El contador QPC proporciona una marca de tiempo de alta resolución que no se ve afectada por los ajustes en el reloj del sistema. La marca de tiempo almacenada en el evento es equivalente al valor devuelto por la API QueryPerformanceCounter. Para obtener más información sobre las características de esta marca de tiempo, vea Adquisición de marcas <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">de tiempo de alta resolución.</a><br /> Debe usar esta resolución si tiene altas tasas de eventos o si el consumidor combina eventos de distintos búferes. En estos casos, la precisión y la estabilidad de la marca de tiempo QPC permiten una mayor precisión a la hora de ordenar los eventos de distintos búferes. Sin embargo, la marca de tiempo QPC no reflejará las actualizaciones del reloj del sistema, por ejemplo, si el reloj del sistema se ajusta hacia delante debido a la sincronización con un servidor NTP mientras el seguimiento está en curso, las marcas de tiempo de QPC del seguimiento seguirán reflejando la hora como si no se hubiera producido ninguna actualización.<br /> Para determinar la resolución, use el <strong>miembro PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> al consumir el evento.<br /> Para convertir la marca de tiempo de un evento en unidades de 100 ns, use la siguiente fórmula de conversión: <br /> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart * 10000000.0 / logfileHeader.PerfFreq.QuadPart<br /> Tenga en cuenta que, en equipos anteriores, es posible que la marca de tiempo no sea precisa porque el contador a veces se omite debido a errores de hardware.<br /> | 
| <dl><dt>2</dt></dl> | Hora del sistema. La hora del sistema proporciona una marca de tiempo que realiza un seguimiento de los cambios en el reloj del sistema, por ejemplo, si el reloj del sistema se ajusta hacia delante debido a la sincronización con un servidor NTP mientras el seguimiento está en curso, las marcas de tiempo del sistema en el seguimiento también saltarán hacia delante para coincidir con la nueva configuración del reloj del sistema. <br /><ul><li>En sistemas anteriores a Windows 10, la marca de tiempo almacenada en el evento es equivalente al valor devuelto por la API GetSystemTimeAsFileTime.</li><li>En Windows 10 o posterior, la marca de tiempo almacenada en el evento es equivalente al valor devuelto por la API GetSystemTimePreciseAsFileTime.</li></ul>Antes de Windows 10, la resolución de esta marca de tiempo era la resolución de un tic del reloj del sistema, como indica el miembro TimerResolution de TRACE_LOGFILE_HEADER. A partir Windows 10, la resolución de esta marca de tiempo es la resolución del contador de rendimiento, como indica el miembro PerfFreq de TRACE_LOGFILE_HEADER.<br /> Para convertir la marca de tiempo de un evento en unidades de 100 ns, use la siguiente fórmula de conversión: <br /> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart<br /> Tenga en cuenta que cuando se capturan eventos en un sistema que ejecuta un sistema operativo antes de Windows 10, si el volumen de eventos es alto, es posible que la resolución de la hora del sistema no sea lo suficientemente correcta como para determinar la secuencia de eventos. En este caso, un conjunto de eventos tendrá la misma marca de tiempo, pero el orden en que ETW entrega los eventos puede no ser correcto. A partir Windows 10, la marca de tiempo se captura con precisión adicional, aunque todavía puede producirse cierta inestabilidad en los casos en los que el reloj del sistema se ajustaba mientras se capturaba el seguimiento.<br /> | 
| <dl><dt>3</dt></dl> | Contador de ciclo de CPU. El contador de CPU proporciona la marca de tiempo de resolución más alta y es el que menos recursos consume para recuperar. Sin embargo, el contador de CPU no es confiable y no debe usarse en producción. Por ejemplo, en algunos equipos, los temporizadores cambiarán la frecuencia debido a cambios térmicos y de energía, además de detenerse en algunos estados.<br /> Para determinar la resolución, use el <strong>miembro CpuSpeedInMHz</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>de TRACE_LOGFILE_HEADER</strong></a> al consumir el evento.<br /> Si el hardware no admite este tipo de reloj, ETW usa la hora del sistema.<br /><strong>Windows Server 2003, Windows XP con SP1 y Windows XP:</strong> Este valor no se admite, se introdujo en Windows Server 2003 con SP1 y Windows XP con SP2.<br /> | 




 

**Windows 2000:** No se admite el miembro **ClientContext.**

</dd> <dt>

**Marcas**
</dt> <dd>

Debe contener **el \_ \_ \_ GUID TRACED de WNODE FLAG** para indicar que la estructura contiene información de seguimiento de eventos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Asegúrese de inicializar la memoria de esta estructura en cero antes de establecer los miembros.

Para convertir una marca de tiempo ETW en FILETIME, use el procedimiento siguiente:

<dl> 1. Para cada archivo de registro o sesión que se está procesando (es decir, para cada LOGFILE DE SEGUIMIENTO DE EVENTOS), compruebe el campo \_ \_ logFile.ProcessTraceMode para determinar si la marca PROCESS TRACE MODE RAW TIMESTAMP está \_ \_ \_ \_ establecida. De forma predeterminada, esta marca no está establecida. Si no se establece esta marca, el tiempo de ejecución de ETW convertirá automáticamente la marca de tiempo de cada REGISTRO DE EVENTOS en filetime antes de enviar el registro de eventos a la función \_ EventRecordCallback, por lo que no se necesita ningún procesamiento \_ adicional. Los pasos siguientes solo se deben usar si el seguimiento se está procesando con la marca PROCESS \_ TRACE MODE RAW TIMESTAMP \_ \_ \_ establecida.  
2. Para cada sesión o archivo de registro que se está procesando (es decir, para cada LOGFILE DE SEGUIMIENTO DE EVENTOS), compruebe el campo \_ logFile.LogfileHeader.ReservedFlags para determinar la escala de marca de tiempo para el archivo de \_ registro. En función del valor de ReservedFlags, siga uno de estos pasos para determinar el valor que se usará para timeStampScale en los pasos restantes: <dl> a. Si ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;  
b. Si ReservedFlags == 2 (hora del sistema): DOUBLE timeStampScale = 1.0;  
Tenga en cuenta que los pasos restantes no son necesarios para los eventos que usan la hora del sistema, ya que los eventos ya proporcionan sus marcas de tiempo en unidades FILETIME. Los pasos restantes funcionarán, pero no son necesarios e introducirán un pequeño error de redondeo.  
c. Si ReservedFlags == 3 (contador de ciclo de CPU): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                         |
| Encabezado<br/>                   | <dl> <dt>Wmistr.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**PROPIEDADES DE \_ SEGUIMIENTO \_ DE EVENTOS**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
