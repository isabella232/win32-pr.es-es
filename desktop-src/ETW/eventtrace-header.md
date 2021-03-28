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
# <a name="eventtrace_header-class"></a><span data-ttu-id="b4840-104">\_Clase de encabezado eventtracer</span><span class="sxs-lookup"><span data-stu-id="b4840-104">EventTrace\_Header class</span></span>

<span data-ttu-id="b4840-105">Clase de tipo de evento para el evento de encabezado del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b4840-105">The event type class for the log file header event.</span></span> <span data-ttu-id="b4840-106">Esta clase contiene información sobre la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="b4840-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="b4840-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4840-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4840-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b4840-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4840-109">Members</span></span>

<span data-ttu-id="b4840-110">La clase de **\_ encabezado eventtracer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b4840-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="b4840-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4840-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4840-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4840-112">Properties</span></span>

<span data-ttu-id="b4840-113">La clase de **\_ encabezado eventtracer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b4840-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4840-114">**BootTime**</span><span class="sxs-lookup"><span data-stu-id="b4840-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-115">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4840-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-117">Calificadores: **WmiDataId** (17)</span><span class="sxs-lookup"><span data-stu-id="b4840-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-118">Hora a la que se inició el sistema, en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="b4840-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="b4840-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-122">Calificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="b4840-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-123">Tamaño de los búferes de la sesión de seguimiento de eventos, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="b4840-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-124">**BuffersLost**</span><span class="sxs-lookup"><span data-stu-id="b4840-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-127">Calificadores: **WmiDataId** (21)</span><span class="sxs-lookup"><span data-stu-id="b4840-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-128">Número total de búferes perdidos.</span><span class="sxs-lookup"><span data-stu-id="b4840-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-129">**BuffersWritten**</span><span class="sxs-lookup"><span data-stu-id="b4840-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-132">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="b4840-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-133">Número total de búferes escritos por la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-134">**CPUSpeed**</span><span class="sxs-lookup"><span data-stu-id="b4840-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-137">Calificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="b4840-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-138">Velocidad de la CPU, en megahercios.</span><span class="sxs-lookup"><span data-stu-id="b4840-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="b4840-139">**Windows 2000:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="b4840-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="b4840-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4840-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-143">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="b4840-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-144">Hora a la que se detuvo la sesión de seguimiento de eventos en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="b4840-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="b4840-145">Este valor puede ser 0 si está consumiendo eventos en tiempo real o desde un archivo de registro en el que el proporcionado todavía está registrando eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-146">**EventsLost**</span><span class="sxs-lookup"><span data-stu-id="b4840-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-149">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="b4840-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-150">Número de eventos perdidos durante la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-151">**LogFileMode**</span><span class="sxs-lookup"><span data-stu-id="b4840-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-154">Calificadores: **WmiDataId** (8), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="b4840-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="b4840-155">Modo de registro actual para la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="b4840-156">Para obtener una lista de valores, vea constantes del modo de registro.</span><span class="sxs-lookup"><span data-stu-id="b4840-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-157">**NombreDeArchivoDeRegistro**</span><span class="sxs-lookup"><span data-stu-id="b4840-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-158">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-160">Calificadores: **WmiDataId** (15), **puntero**</span><span class="sxs-lookup"><span data-stu-id="b4840-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="b4840-161">Nombre del archivo de registro de seguimiento de eventos que contiene los eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-162">**LoggerName**</span><span class="sxs-lookup"><span data-stu-id="b4840-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-165">Calificadores: **WmiDataId** (14), **puntero**</span><span class="sxs-lookup"><span data-stu-id="b4840-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="b4840-166">Nombre de la sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b4840-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-167">**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="b4840-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-170">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="b4840-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-171">Tamaño máximo del archivo de registro, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="b4840-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="b4840-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-173">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-175">Calificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="b4840-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-176">Número de procesadores del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4840-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-177">**PerfFreq**</span><span class="sxs-lookup"><span data-stu-id="b4840-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-178">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4840-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-180">Calificadores: **WmiDataId** (18)</span><span class="sxs-lookup"><span data-stu-id="b4840-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-181">Frecuencia del contador de rendimiento de alta resolución, si existe.</span><span class="sxs-lookup"><span data-stu-id="b4840-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-182">**PointerSize**</span><span class="sxs-lookup"><span data-stu-id="b4840-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-185">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="b4840-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-186">Tamaño de un tipo de datos de puntero, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4840-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-187">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="b4840-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-188">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-190">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="b4840-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-191">Número de compilación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4840-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-192">**ReservedFlags**</span><span class="sxs-lookup"><span data-stu-id="b4840-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-195">Calificadores: **WmiDataId** (20)</span><span class="sxs-lookup"><span data-stu-id="b4840-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-196">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b4840-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-197">**StartBuffers**</span><span class="sxs-lookup"><span data-stu-id="b4840-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-198">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-200">Calificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="b4840-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-201">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b4840-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="b4840-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-203">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4840-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-205">Calificadores: **WmiDataId** (19)</span><span class="sxs-lookup"><span data-stu-id="b4840-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-206">Hora a la que se inició la sesión de seguimiento de eventos, en intervalos de 100 segundos desde la medianoche del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="b4840-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="b4840-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-210">Calificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="b4840-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-211">Resolución del temporizador de hardware, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="b4840-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-212">**TimeZoneInformation**</span><span class="sxs-lookup"><span data-stu-id="b4840-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-213">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="b4840-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4840-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-215">Calificadores: **WmiDataId** (16), **extensión ("noprint")**, **Max** (176)</span><span class="sxs-lookup"><span data-stu-id="b4840-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-216">Estructura [**de \_ \_ información de zona horaria**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) que contiene la zona horaria para los miembros **BootTime**, **EndTime** y **startTime** .</span><span class="sxs-lookup"><span data-stu-id="b4840-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="b4840-217">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b4840-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4840-218">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4840-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4840-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4840-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4840-220">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="b4840-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="b4840-221">Número de versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4840-221">Version number of the operating system.</span></span> <span data-ttu-id="b4840-222">A partir de los bytes de orden inferior, los dos primeros bytes contienen la versión principal, los dos bytes siguientes contienen la versión secundaria, los dos bytes siguientes contienen Service Pack versión principal y los dos últimos bytes contienen Service Pack versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="b4840-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4840-223">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4840-223">Remarks</span></span>

<span data-ttu-id="b4840-224">Normalmente, desea guardar los valores de las siguientes propiedades para su uso posterior al procesar eventos del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b4840-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="b4840-225">**TimerResolution**: se usa con los miembros **KernelTime** y **UserTime** de la estructura de [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para determinar el costo de CPU para un conjunto de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="b4840-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="b4840-226">Para obtener más información, vea la sección Comentarios del [**\_ \_ encabezado de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span><span class="sxs-lookup"><span data-stu-id="b4840-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="b4840-227">**PointerSize**: para las propiedades que contienen el calificador de **puntero** , use este valor para determinar el tamaño del puntero.</span><span class="sxs-lookup"><span data-stu-id="b4840-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="b4840-228">Tenga en cuenta que este valor puede no ser preciso.</span><span class="sxs-lookup"><span data-stu-id="b4840-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="b4840-229">Por ejemplo, en un equipo de 64 bits, una aplicación de 32 bits registra punteros de 4 bytes; sin embargo, la sesión establecerá **PointerSize** en 8.</span><span class="sxs-lookup"><span data-stu-id="b4840-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="b4840-230">**LogFileMode**: se usa para determinar si esta sesión es una sesión de registrador privada.</span><span class="sxs-lookup"><span data-stu-id="b4840-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="b4840-231">Hay algunas propiedades que no contienen datos para las sesiones del registrador privado.</span><span class="sxs-lookup"><span data-stu-id="b4840-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="b4840-232">Por ejemplo, los miembros **KernelTime** y **UserTime** de la estructura de [**\_ \_ encabezado de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="b4840-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4840-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4840-233">Requirements</span></span>



| <span data-ttu-id="b4840-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4840-234">Requirement</span></span> | <span data-ttu-id="b4840-235">Value</span><span class="sxs-lookup"><span data-stu-id="b4840-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4840-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4840-236">Minimum supported client</span></span><br/> | <span data-ttu-id="b4840-237">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4840-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b4840-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4840-238">Minimum supported server</span></span><br/> | <span data-ttu-id="b4840-239">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4840-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b4840-240">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4840-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4840-241">**EventTraceEvent**</span><span class="sxs-lookup"><span data-stu-id="b4840-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="b4840-242">**encabezado de archivo de registro de seguimiento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4840-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
