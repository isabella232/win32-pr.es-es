---
description: La \_ estructura de encabezado WNODE es un miembro de la \_ estructura de propiedades de seguimiento de eventos \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER estructura (Wmistr. h)
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
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "104987415"
---
# <a name="wnode_header-structure"></a>\_Estructura del encabezado WNODE

La estructura de **\_ encabezado WNODE** es un miembro de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

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

Tamaño total de la memoria asignada, en bytes, para las propiedades de la sesión de seguimiento de eventos. El tamaño de la memoria debe incluir el espacio de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) más la cadena de nombre de sesión y la cadena de nombre de archivo de registro que siguen la estructura en memoria.

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

**Indicaciones**
</dt> <dd>

Hora a la que se actualizó la información de esta estructura, en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.

</dd> <dt>

**Guid**
</dt> <dd>

GUID que se define para la sesión.

En el caso de una sesión del registrador del kernel de NT, establezca este miembro en **SystemTraceControlGuid**.

Si este miembro se establece en **SystemTraceControlGuid** o **GlobalLoggerGuid**, el Registrador será un registrador del sistema.

En el caso de una sesión de registrador privado, establezca este miembro en el GUID del proveedor que va a habilitar para la sesión.

Si inicia una sesión que no es un registrador de kernel o una sesión de registrador privada, no es necesario especificar un GUID de sesión. Si no especifica un GUID, ETW crea uno automáticamente. Solo tiene que especificar un GUID de sesión si desea cambiar los permisos predeterminados asociados a una sesión específica. Para obtener más información, consulte la función EventAccessControl.

No se puede iniciar más de una sesión con el mismo GUID de sesión.

**Antes de Windows Vista:** Puede iniciar más de una sesión con el mismo GUID de sesión.

</dd> <dt>

**ClientContext**
</dt> <dd>

Resolución de reloj que se va a usar al registrar la marca de tiempo para cada evento. El valor predeterminado es contador de rendimiento de consultas (QPC).

**Antes de Windows Vista:** El valor predeterminado es la hora del sistema.

**Antes de Windows 10, versión 1703:** Los registradores del sistema no pueden usar simultáneamente más de 2 tipos de relojes distintos.

**A partir de Windows 10, versión 1703:** Se ha quitado la restricción de tipo de reloj. Los registradores del sistema ahora pueden usar los tres tipos de reloj simultáneamente.

Puede especificar uno de los siguientes valores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>1</dt> </dl></td>
<td>Contador de rendimiento de consultas (QPC). El contador QPC proporciona una marca de tiempo de alta resolución que no se ve afectada por los ajustes del reloj del sistema. La marca de tiempo almacenada en el evento es equivalente al valor devuelto desde la API de QueryPerformanceCounter. Para obtener más información sobre las características de esta marca de tiempo, vea <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">adquirir marcas de tiempo de alta resolución</a>.<br/> Debe utilizar esta resolución si tiene tasas de eventos elevadas o si el consumidor combina eventos de distintos búferes. En estos casos, la precisión y la estabilidad de la marca de tiempo QPC permiten una mejor precisión en la ordenación de los eventos de distintos búferes. Sin embargo, la marca de tiempo QPC no reflejará las actualizaciones del reloj del sistema, por ejemplo, si el reloj del sistema se ajusta hacia delante debido a la sincronización con un servidor NTP mientras el seguimiento está en curso, las marcas de tiempo de QPC en el seguimiento seguirán reflejando el tiempo como si no se hubiera producido ninguna actualización.<br/> Para determinar la resolución, use el miembro <strong>PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> al utilizar el evento.<br/> Para convertir la marca de tiempo de un evento en unidades 100-NS, use la siguiente fórmula de conversión: <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart * 10000000,0/logfileHeader. PerfFreq. QuadPart<br/> Tenga en cuenta que en los equipos más antiguos, es posible que la marca de tiempo no sea exacta porque el contador se omite a veces debido a errores de hardware.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>Hora del sistema. La hora del sistema proporciona una marca de tiempo que realiza un seguimiento de los cambios en el reloj del sistema, por ejemplo, si el reloj del sistema se ajusta hacia delante debido a la sincronización con un servidor NTP mientras el seguimiento está en curso, las marcas de tiempo de hora del sistema del seguimiento también pasarán a coincidir con el nuevo valor del reloj del sistema. <br/>
<ul>
<li>En sistemas anteriores a Windows 10, la marca de tiempo almacenada en el evento es equivalente al valor devuelto de la API de GetSystemTimeAsFileTime.</li>
<li>En Windows 10 o versiones posteriores, la marca de tiempo almacenada en el evento es equivalente al valor devuelto de la API de GetSystemTimePreciseAsFileTime.</li>
</ul>
Antes de Windows 10, la resolución de esta marca de tiempo era la resolución de un paso del reloj del sistema, como indica el miembro TimerResolution de TRACE_LOGFILE_HEADER. A partir de Windows 10, la resolución de esta marca de tiempo es la resolución del contador de rendimiento, como indica el miembro PerfFreq de TRACE_LOGFILE_HEADER.<br/> Para convertir la marca de tiempo de un evento en unidades 100-NS, use la siguiente fórmula de conversión: <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart<br/> Tenga en cuenta que cuando se capturan eventos en un sistema que ejecuta un sistema operativo anterior a Windows 10, si el volumen de eventos es alto, es posible que la resolución de la hora del sistema no sea suficiente para determinar la secuencia de eventos. En este caso, un conjunto de eventos tendrá la misma marca de tiempo, pero el orden en el que ETW entrega los eventos puede no ser correcto. A partir de Windows 10, la marca de tiempo se captura con precisión adicional, aunque es posible que se siga produciendo una inestabilidad en los casos en los que el reloj del sistema se ajustó mientras se estaba capturando el seguimiento.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>3</dt> </dl></td>
<td>Contador de ciclo de CPU. El contador de CPU proporciona la marca de tiempo de resolución más alta y es el que requiere menos recursos para recuperar. Sin embargo, el contador de CPU no es confiable y no debe usarse en producción. Por ejemplo, en algunos equipos, los temporizadores cambiarán la frecuencia debido a cambios térmicos y de energía, además de detenerse en algunos Estados.<br/> Para determinar la resolución, use el miembro <strong>CpuSpeedInMHz</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> al utilizar el evento.<br/> Si el hardware no admite este tipo de reloj, ETW usará la hora del sistema.<br/> <strong>Windows Server 2003, Windows XP con SP1 y Windows XP:</strong> Este valor no se admite, ya que se presentó en Windows Server 2003 con SP1 y Windows XP con SP2.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000:** No se admite el miembro de **ClientContext** .

</dd> <dt>

**Marcas**
</dt> <dd>

Debe contener **el \_ \_ \_ GUID de seguimiento de marca WNODE** para indicar que la estructura contiene información de seguimiento de eventos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Asegúrese de inicializar la memoria para esta estructura en cero antes de establecer los miembros.

Para convertir una marca de tiempo de ETW en un FILETIME, use el siguiente procedimiento:

<dl> 1. Para cada sesión o archivo de registro que se está procesando (es decir, para cada registro de seguimiento de eventos \_ \_ ), compruebe el campo logfile. ProcessTraceMode para determinar si \_ \_ \_ se ha establecido la marca de marca de tiempo sin formato del modo de seguimiento del proceso \_ . De forma predeterminada, esta marca no está establecida. Si no se establece esta marca, el Runtime de ETW convertirá automáticamente la marca de tiempo de cada registro de evento \_ en un FILETIME antes de enviar el registro de eventos \_ a la función EventRecordCallback, por lo que no se necesita ningún procesamiento adicional. Los siguientes pasos solo deben usarse si el seguimiento se está procesando con la \_ marca de marca de tiempo sin procesar del modo de seguimiento del proceso \_ \_ \_ establecida.  
2. Para cada sesión o archivo de registro que se está procesando (es decir, para cada registro de seguimiento de eventos \_ \_ ), compruebe el campo logfile. LogfileHeader. ReservedFlags para determinar la escala de la marca de tiempo para el archivo de registro. Según el valor de ReservedFlags, siga uno de estos pasos para determinar el valor que se va a usar para timeStampScale en los pasos restantes: <dl> a. Si ReservedFlags = = 1 (QPC): DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart;  
b. Si ReservedFlags = = 2 (hora del sistema): DOUBLE timeStampScale = 1,0;  
Tenga en cuenta que los pasos restantes no son necesarios para los eventos que usan la hora del sistema, ya que los eventos ya proporcionan sus marcas de tiempo en unidades de FILETIME. Los pasos restantes funcionarán pero no son necesarios y introducirán un pequeño error de redondeo.  
c. Si ReservedFlags = = 3 (contador de ciclo de CPU): DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                   |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                         |
| Encabezado<br/>                   | <dl> <dt>Wmistr. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**\_propiedades de seguimiento de eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**\_entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
