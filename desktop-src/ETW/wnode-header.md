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
# <a name="wnode_header-structure"></a><span data-ttu-id="931fa-103">\_Estructura del encabezado WNODE</span><span class="sxs-lookup"><span data-stu-id="931fa-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="931fa-104">La estructura de **\_ encabezado WNODE** es un miembro de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="931fa-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="931fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="931fa-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="931fa-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="931fa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="931fa-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="931fa-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-108">Tamaño total de la memoria asignada, en bytes, para las propiedades de la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="931fa-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="931fa-109">El tamaño de la memoria debe incluir el espacio de la estructura de [**\_ \_ propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) más la cadena de nombre de sesión y la cadena de nombre de archivo de registro que siguen la estructura en memoria.</span><span class="sxs-lookup"><span data-stu-id="931fa-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-110">**ProviderId**</span><span class="sxs-lookup"><span data-stu-id="931fa-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-111">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="931fa-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-112">**HistoricalContext**</span><span class="sxs-lookup"><span data-stu-id="931fa-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-113">En la salida, identificador de la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="931fa-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-114">**Versión**</span><span class="sxs-lookup"><span data-stu-id="931fa-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-115">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="931fa-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-116">**Vinculación**</span><span class="sxs-lookup"><span data-stu-id="931fa-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-117">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="931fa-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-118">**KernelHandle**</span><span class="sxs-lookup"><span data-stu-id="931fa-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-119">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="931fa-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-120">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="931fa-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-121">Hora a la que se actualizó la información de esta estructura, en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="931fa-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-122">**Guid**</span><span class="sxs-lookup"><span data-stu-id="931fa-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-123">GUID que se define para la sesión.</span><span class="sxs-lookup"><span data-stu-id="931fa-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="931fa-124">En el caso de una sesión del registrador del kernel de NT, establezca este miembro en **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="931fa-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="931fa-125">Si este miembro se establece en **SystemTraceControlGuid** o **GlobalLoggerGuid**, el Registrador será un registrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="931fa-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="931fa-126">En el caso de una sesión de registrador privado, establezca este miembro en el GUID del proveedor que va a habilitar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="931fa-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="931fa-127">Si inicia una sesión que no es un registrador de kernel o una sesión de registrador privada, no es necesario especificar un GUID de sesión.</span><span class="sxs-lookup"><span data-stu-id="931fa-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="931fa-128">Si no especifica un GUID, ETW crea uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="931fa-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="931fa-129">Solo tiene que especificar un GUID de sesión si desea cambiar los permisos predeterminados asociados a una sesión específica.</span><span class="sxs-lookup"><span data-stu-id="931fa-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="931fa-130">Para obtener más información, consulte la función EventAccessControl.</span><span class="sxs-lookup"><span data-stu-id="931fa-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="931fa-131">No se puede iniciar más de una sesión con el mismo GUID de sesión.</span><span class="sxs-lookup"><span data-stu-id="931fa-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="931fa-132">**Antes de Windows Vista:** Puede iniciar más de una sesión con el mismo GUID de sesión.</span><span class="sxs-lookup"><span data-stu-id="931fa-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="931fa-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-134">Resolución de reloj que se va a usar al registrar la marca de tiempo para cada evento.</span><span class="sxs-lookup"><span data-stu-id="931fa-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="931fa-135">El valor predeterminado es contador de rendimiento de consultas (QPC).</span><span class="sxs-lookup"><span data-stu-id="931fa-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="931fa-136">**Antes de Windows Vista:** El valor predeterminado es la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="931fa-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="931fa-137">**Antes de Windows 10, versión 1703:** Los registradores del sistema no pueden usar simultáneamente más de 2 tipos de relojes distintos.</span><span class="sxs-lookup"><span data-stu-id="931fa-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="931fa-138">**A partir de Windows 10, versión 1703:** Se ha quitado la restricción de tipo de reloj.</span><span class="sxs-lookup"><span data-stu-id="931fa-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="931fa-139">Los registradores del sistema ahora pueden usar los tres tipos de reloj simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="931fa-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="931fa-140">Puede especificar uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="931fa-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="931fa-141">Value</span><span class="sxs-lookup"><span data-stu-id="931fa-141">Value</span></span></th>
<th><span data-ttu-id="931fa-142">Significado</span><span class="sxs-lookup"><span data-stu-id="931fa-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="931fa-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="931fa-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="931fa-144">Contador de rendimiento de consultas (QPC).</span><span class="sxs-lookup"><span data-stu-id="931fa-144">Query performance counter (QPC).</span></span> <span data-ttu-id="931fa-145">El contador QPC proporciona una marca de tiempo de alta resolución que no se ve afectada por los ajustes del reloj del sistema.</span><span class="sxs-lookup"><span data-stu-id="931fa-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="931fa-146">La marca de tiempo almacenada en el evento es equivalente al valor devuelto desde la API de QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="931fa-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="931fa-147">Para obtener más información sobre las características de esta marca de tiempo, vea <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">adquirir marcas de tiempo de alta resolución</a>.</span><span class="sxs-lookup"><span data-stu-id="931fa-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="931fa-148">Debe utilizar esta resolución si tiene tasas de eventos elevadas o si el consumidor combina eventos de distintos búferes.</span><span class="sxs-lookup"><span data-stu-id="931fa-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="931fa-149">En estos casos, la precisión y la estabilidad de la marca de tiempo QPC permiten una mejor precisión en la ordenación de los eventos de distintos búferes.</span><span class="sxs-lookup"><span data-stu-id="931fa-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="931fa-150">Sin embargo, la marca de tiempo QPC no reflejará las actualizaciones del reloj del sistema, por ejemplo, si el reloj del sistema se ajusta hacia delante debido a la sincronización con un servidor NTP mientras el seguimiento está en curso, las marcas de tiempo de QPC en el seguimiento seguirán reflejando el tiempo como si no se hubiera producido ninguna actualización.</span><span class="sxs-lookup"><span data-stu-id="931fa-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="931fa-151">Para determinar la resolución, use el miembro <strong>PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> al utilizar el evento.</span><span class="sxs-lookup"><span data-stu-id="931fa-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="931fa-152">Para convertir la marca de tiempo de un evento en unidades 100-NS, use la siguiente fórmula de conversión:</span><span class="sxs-lookup"><span data-stu-id="931fa-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="931fa-153">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart \* 10000000,0/logfileHeader. PerfFreq. QuadPart</span><span class="sxs-lookup"><span data-stu-id="931fa-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="931fa-154">Tenga en cuenta que en los equipos más antiguos, es posible que la marca de tiempo no sea exacta porque el contador se omite a veces debido a errores de hardware.</span><span class="sxs-lookup"><span data-stu-id="931fa-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="931fa-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="931fa-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="931fa-156">Hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="931fa-156">System time.</span></span> <span data-ttu-id="931fa-157">La hora del sistema proporciona una marca de tiempo que realiza un seguimiento de los cambios en el reloj del sistema, por ejemplo, si el reloj del sistema se ajusta hacia delante debido a la sincronización con un servidor NTP mientras el seguimiento está en curso, las marcas de tiempo de hora del sistema del seguimiento también pasarán a coincidir con el nuevo valor del reloj del sistema.</span><span class="sxs-lookup"><span data-stu-id="931fa-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="931fa-158">En sistemas anteriores a Windows 10, la marca de tiempo almacenada en el evento es equivalente al valor devuelto de la API de GetSystemTimeAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="931fa-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="931fa-159">En Windows 10 o versiones posteriores, la marca de tiempo almacenada en el evento es equivalente al valor devuelto de la API de GetSystemTimePreciseAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="931fa-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="931fa-160">Antes de Windows 10, la resolución de esta marca de tiempo era la resolución de un paso del reloj del sistema, como indica el miembro TimerResolution de TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="931fa-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="931fa-161">A partir de Windows 10, la resolución de esta marca de tiempo es la resolución del contador de rendimiento, como indica el miembro PerfFreq de TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="931fa-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="931fa-162">Para convertir la marca de tiempo de un evento en unidades 100-NS, use la siguiente fórmula de conversión:</span><span class="sxs-lookup"><span data-stu-id="931fa-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="931fa-163">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart</span><span class="sxs-lookup"><span data-stu-id="931fa-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="931fa-164">Tenga en cuenta que cuando se capturan eventos en un sistema que ejecuta un sistema operativo anterior a Windows 10, si el volumen de eventos es alto, es posible que la resolución de la hora del sistema no sea suficiente para determinar la secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="931fa-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="931fa-165">En este caso, un conjunto de eventos tendrá la misma marca de tiempo, pero el orden en el que ETW entrega los eventos puede no ser correcto.</span><span class="sxs-lookup"><span data-stu-id="931fa-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="931fa-166">A partir de Windows 10, la marca de tiempo se captura con precisión adicional, aunque es posible que se siga produciendo una inestabilidad en los casos en los que el reloj del sistema se ajustó mientras se estaba capturando el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="931fa-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="931fa-167"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="931fa-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="931fa-168">Contador de ciclo de CPU.</span><span class="sxs-lookup"><span data-stu-id="931fa-168">CPU cycle counter.</span></span> <span data-ttu-id="931fa-169">El contador de CPU proporciona la marca de tiempo de resolución más alta y es el que requiere menos recursos para recuperar.</span><span class="sxs-lookup"><span data-stu-id="931fa-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="931fa-170">Sin embargo, el contador de CPU no es confiable y no debe usarse en producción.</span><span class="sxs-lookup"><span data-stu-id="931fa-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="931fa-171">Por ejemplo, en algunos equipos, los temporizadores cambiarán la frecuencia debido a cambios térmicos y de energía, además de detenerse en algunos Estados.</span><span class="sxs-lookup"><span data-stu-id="931fa-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="931fa-172">Para determinar la resolución, use el miembro <strong>CpuSpeedInMHz</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> al utilizar el evento.</span><span class="sxs-lookup"><span data-stu-id="931fa-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="931fa-173">Si el hardware no admite este tipo de reloj, ETW usará la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="931fa-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="931fa-174"><strong>Windows Server 2003, Windows XP con SP1 y Windows XP:</strong> Este valor no se admite, ya que se presentó en Windows Server 2003 con SP1 y Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="931fa-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="931fa-175">**Windows 2000:** No se admite el miembro de **ClientContext** .</span><span class="sxs-lookup"><span data-stu-id="931fa-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="931fa-176">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="931fa-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="931fa-177">Debe contener **el \_ \_ \_ GUID de seguimiento de marca WNODE** para indicar que la estructura contiene información de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="931fa-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="931fa-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="931fa-178">Remarks</span></span>

<span data-ttu-id="931fa-179">Asegúrese de inicializar la memoria para esta estructura en cero antes de establecer los miembros.</span><span class="sxs-lookup"><span data-stu-id="931fa-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="931fa-180">Para convertir una marca de tiempo de ETW en un FILETIME, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="931fa-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="931fa-181">Para cada sesión o archivo de registro que se está procesando (es decir, para cada registro de seguimiento de eventos \_ \_ ), compruebe el campo logfile. ProcessTraceMode para determinar si \_ \_ \_ se ha establecido la marca de marca de tiempo sin formato del modo de seguimiento del proceso \_ .</span><span class="sxs-lookup"><span data-stu-id="931fa-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="931fa-182">De forma predeterminada, esta marca no está establecida.</span><span class="sxs-lookup"><span data-stu-id="931fa-182">By default, this flag is not set.</span></span> <span data-ttu-id="931fa-183">Si no se establece esta marca, el Runtime de ETW convertirá automáticamente la marca de tiempo de cada registro de evento \_ en un FILETIME antes de enviar el registro de eventos \_ a la función EventRecordCallback, por lo que no se necesita ningún procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="931fa-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="931fa-184">Los siguientes pasos solo deben usarse si el seguimiento se está procesando con la \_ marca de marca de tiempo sin procesar del modo de seguimiento del proceso \_ \_ \_ establecida.</span><span class="sxs-lookup"><span data-stu-id="931fa-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="931fa-185">Para cada sesión o archivo de registro que se está procesando (es decir, para cada registro de seguimiento de eventos \_ \_ ), compruebe el campo logfile. LogfileHeader. ReservedFlags para determinar la escala de la marca de tiempo para el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="931fa-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="931fa-186">Según el valor de ReservedFlags, siga uno de estos pasos para determinar el valor que se va a usar para timeStampScale en los pasos restantes:</span><span class="sxs-lookup"><span data-stu-id="931fa-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="931fa-187">a.</span><span class="sxs-lookup"><span data-stu-id="931fa-187">a.</span></span> <span data-ttu-id="931fa-188">Si ReservedFlags = = 1 (QPC): DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart;</span><span class="sxs-lookup"><span data-stu-id="931fa-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="931fa-189">b.</span><span class="sxs-lookup"><span data-stu-id="931fa-189">b.</span></span> <span data-ttu-id="931fa-190">Si ReservedFlags = = 2 (hora del sistema): DOUBLE timeStampScale = 1,0;</span><span class="sxs-lookup"><span data-stu-id="931fa-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="931fa-191">Tenga en cuenta que los pasos restantes no son necesarios para los eventos que usan la hora del sistema, ya que los eventos ya proporcionan sus marcas de tiempo en unidades de FILETIME.</span><span class="sxs-lookup"><span data-stu-id="931fa-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="931fa-192">Los pasos restantes funcionarán pero no son necesarios y introducirán un pequeño error de redondeo.</span><span class="sxs-lookup"><span data-stu-id="931fa-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="931fa-193">c.</span><span class="sxs-lookup"><span data-stu-id="931fa-193">c.</span></span> <span data-ttu-id="931fa-194">Si ReservedFlags = = 3 (contador de ciclo de CPU): DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz;</span><span class="sxs-lookup"><span data-stu-id="931fa-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="931fa-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="931fa-195">Requirements</span></span>



| <span data-ttu-id="931fa-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="931fa-196">Requirement</span></span> | <span data-ttu-id="931fa-197">Value</span><span class="sxs-lookup"><span data-stu-id="931fa-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="931fa-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="931fa-198">Minimum supported client</span></span><br/> | <span data-ttu-id="931fa-199">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="931fa-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="931fa-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="931fa-200">Minimum supported server</span></span><br/> | <span data-ttu-id="931fa-201">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="931fa-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="931fa-202">Encabezado</span><span class="sxs-lookup"><span data-stu-id="931fa-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="931fa-203"><dt>Wmistr. h</dt></span><span class="sxs-lookup"><span data-stu-id="931fa-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="931fa-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="931fa-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931fa-205">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="931fa-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="931fa-206">**\_propiedades de seguimiento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="931fa-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="931fa-207">**GetTraceLoggerHandle**</span><span class="sxs-lookup"><span data-stu-id="931fa-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="931fa-208">**\_entero grande**</span><span class="sxs-lookup"><span data-stu-id="931fa-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
