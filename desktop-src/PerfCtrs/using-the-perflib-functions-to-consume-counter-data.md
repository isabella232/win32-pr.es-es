---
title: Uso de funciones PerfLib para consumir datos de contadores
description: Las funciones de la API de PerfLib se pueden usar para consumir datos del contador de rendimiento V2 directamente cuando no se puede usar PDH.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "105720178"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>Uso de funciones PerfLib para consumir datos de contadores

Utilice las funciones de consumidor de PerfLib para consumir datos de rendimiento de los proveedores de datos de rendimiento V2 cuando no se pueden usar las funciones de la [aplicación auxiliar de datos de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md). Estas funciones se pueden usar al escribir aplicaciones de OneCore para recopilar los valores de configuración de V2 o cuando es necesario recopilar los valores de configuración de V2 con las dependencias y la sobrecarga mínimas.

> [!TIP]
> Las funciones de consumidor de PerfLib V2 son más difíciles de usar que las funciones de la aplicación auxiliar de datos de rendimiento (PDH) y solo admiten la recopilación de datos de proveedores de V2. Las funciones PDH deben ser preferibles para la mayoría de las aplicaciones.

Las funciones de consumidor de PerfLib V2 son la API de bajo nivel para recopilar datos de **proveedores de V2**. Las funciones de consumidor de PerfLib V2 no admiten la recopilación de datos de **proveedores de v1**.

> [!WARNING]
> Las funciones de consumidor de PerfLib V2 pueden recopilar datos de orígenes que no son de confianza, por ejemplo, de servicios locales con privilegios limitados o de equipos remotos. Las funciones de consumidor de PerfLib V2 no validan los datos para mantener la integridad o la coherencia. Depende de la aplicación de consumidor comprobar que los datos devueltos son coherentes, por ejemplo, que los valores de tamaño del bloque de datos devuelto no superan el tamaño real del bloque de datos devuelto. Esto es especialmente importante cuando la aplicación de consumidor se ejecuta con privilegios elevados.

## <a name="perflib-usage"></a>Uso de PerfLib

El `perflib.h` encabezado incluye las declaraciones usadas por los proveedores de modo de usuario de V2 (es decir, la API del proveedor de Perflib) y los consumidores V2 (es decir, la API de consumidor de Perflib). Declara las siguientes funciones para consumir datos de rendimiento V2:

- Use [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) para obtener los GUID de los contraconjuntos registrados por los proveedores de V2 en el sistema.
- Use [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) para obtener información sobre un CounterSet determinado como el nombre de CounterSet, la descripción, el tipo (instancia única o de varias instancias), los tipos de contador, los nombres de contadores y las descripciones de los contadores.
- Use [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) para obtener los nombres de las instancias actualmente activas de un CounterSet de varias instancias.
- Use [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) para crear un nuevo identificador de consulta que se usará para recopilar datos de uno o más contraconjuntos.
- Use [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) para cerrar un identificador de consulta.
- Use [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) para agregar una consulta a un identificador de consulta.
- Use [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) para quitar una consulta de un identificador de consulta.
- Use [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) para obtener información sobre las consultas actuales en un identificador de consulta.
- Use [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) para recopilar los datos de rendimiento de un identificador de consulta.

Si el consumidor va a consumir datos solo de un proveedor específico en el que los índices GUID y Counter son estables y tiene acceso al archivo de símbolos generado por [CTRPP](ctrpp.md)(desde el `-ch` parámetro CTRPP), puede codificar de forma rígida el GUID de CounterSet y los valores de índice de contador en el consumidor.

De lo contrario, tendrá que cargar los metadatos de CounterSet para determinar los GUID de CounterSet y los índices de contador que se usarán en la consulta de la siguiente manera:

- Use **PerfEnumerateCounterSet** para obtener una lista de GUID de CounterSet admitidos.
- Para cada GUID, use **PerfQueryCounterSetRegistrationInfo** para cargar el nombre de CounterSet. Deténgase cuando encuentre el nombre que está buscando.
- Use **PerfQueryCounterSetRegistrationInfo** para cargar el resto de metadatos (configuración de CounterSet, nombres de contador, índices de contador, tipos de contador) para ese CounterSet.

Si solo necesita conocer los nombres de las instancias actualmente activas de un CounterSet (es decir, si no necesita los valores reales de los datos de rendimiento), puede usar **PerfEnumerateCounterSetInstances**. Esto toma un GUID CounterSet como entrada y devuelve un `PERF_INSTANCE_HEADER` bloque con los nombres y los identificadores de las instancias actualmente activas del CounterSet determinado.

### <a name="queries"></a>Consultas

Para recopilar datos de rendimiento, debe crear un identificador de consulta, agregarle consultas y recopilar los datos de las consultas.

Un identificador de consulta puede tener muchas consultas asociadas. Cuando se llama a **PerfQueryCounterData** para un identificador de consulta, Perflib ejecutará todas las consultas del identificador y recopilará todos los resultados.

Cada consulta especifica un GUID de CounterSet, un filtro de nombre de instancia, un filtro de ID. de instancia opcional y un filtro de ID. de contador opcional.

- El GUID de CounterSet es obligatorio. Indica el GUID del CounterSet desde el que la consulta recopilará los datos. Esto es similar a la `FROM` cláusula de una consulta SQL.
- El filtro de nombre de instancia es obligatorio. Indica un patrón de carácter comodín con el que debe coincidir el nombre de instancia para que la instancia se incluya en la consulta, con `*` lo que se indica "cualquier carácter" y se `?` indica "un carácter". En el caso de los contraconjuntos de instancia única, se **debe** establecer en una cadena de longitud cero `""` . En el caso de los contraconjuntos de varias instancias, **debe** establecerse en una cadena que no esté vacía (use `"*"` para aceptar todos los nombres de instancia). Esto es similar a una `WHERE InstanceName LIKE NameFilter` cláusula de una consulta SQL.
- El filtro de ID. de instancia es opcional. Si está presente (es decir, si se establece en un valor distinto de `0xFFFFFFFF` ), indica que la consulta solo debe recopilar las instancias en las que el identificador de instancia coincide con el identificador especificado. Si no existe (es decir, si `0xFFFFFFFF` está establecido en), indica que la consulta debe aceptar todos los identificadores de instancia. Esto es similar a una `WHERE InstanceId == IdFilter` cláusula de una consulta SQL.
- El filtro de ID. de contador es opcional. Si está presente (es decir, si se establece en un valor distinto de `PERF_WILDCARD_COUNTER` ), indica que la consulta debe recopilar un solo contador, similar a una `SELECT CounterName` cláusula de una consulta SQL. Si no existe (es decir, si `PERF_WILDCARD_COUNTER` está establecido en), indica que la consulta debe recopilar todos los contadores disponibles, de forma similar a una `SELECT *` cláusula de una consulta SQL.

Use **PerfAddCounters** para agregar consultas a un identificador de consulta. Use **PerfDeleteCounters** para quitar las consultas de un identificador de consulta.

Después de cambiar las consultas en un identificador de consulta, use **PerfQueryCounterInfo** para obtener los índices de consulta. Los índices indican el orden en que los resultados de la consulta se devolverán por **PerfQueryCounterData** (los resultados no siempre coincidirán con el orden en el que se agregaron las consultas).

Una vez que el identificador de consulta esté listo, use **PerfQueryCounterData** para recopilar los datos. Normalmente, los datos se recopilan periódicamente (una vez por segundo o una vez por minuto) y después se procesan los datos según sea necesario.

> [!NOTE]
> Los contadores de rendimiento no están diseñados para recopilarse más de una vez por segundo.

**PerfQueryCounterData** devolverá un `PERF_DATA_HEADER` bloque, que consta de un encabezado de datos con marcas de tiempo seguido de una secuencia de `PERF_COUNTER_HEADER` bloques, cada uno de los cuales contiene los resultados de una consulta.

`PERF_COUNTER_HEADER`Puede contener diferentes tipos de datos, como se indica en el valor del `dwType` campo:

- `PERF_ERROR_RETURN` -PerfLib no puede obtener datos de contador válidos de vuelta del proveedor.
- `PERF_SINGLE_COUNTER` -La consulta era para un solo contador de un CounterSet de una sola instancia. Los resultados contienen solo el valor del contador solicitado.
- `PERF_MULTIPLE_COUNTERS` -La consulta era para varios contadores de un CounterSet de una sola instancia. El resultado contiene los valores del contador junto con información para hacer coincidir cada valor con el contador correspondiente (es decir, los encabezados de columna).
- `PERF_MULTIPLE_INSTANCES` -La consulta era para un solo contador de un CounterSet de varias instancias. Los resultados contienen la información de la instancia (es decir, los encabezados de fila) y un valor de contador por instancia.
- `PERF_COUNTERSET` -La consulta era para varios contadores de un CounterSet de varias instancias. Los resultados contienen la información de la instancia (es decir, los encabezados de fila), los valores de contador para cada instancia e información para hacer coincidir cada valor con el contador correspondiente (es decir, los encabezados de columna).

Los valores devueltos por **PerfQueryCounterData** son `UINT32` o `UINT64` valores sin formato. Normalmente, estos requieren algún procesamiento para generar los valores con formato esperados. El procesamiento necesario depende del tipo del contador. Muchos tipos de contador requieren información adicional para el procesamiento completo, como una marca de tiempo o un valor de un contador "base" en el mismo ejemplo.

Algunos tipos de contador son contadores "Delta" que solo son significativos cuando se comparan con los datos de un ejemplo anterior. Por ejemplo, un contador de tipo `PERF_SAMPLE_COUNTER` tiene un valor con formato que se espera que muestre una tasa (el número de veces que se ha producido una cosa determinada por segundo sobre el intervalo de muestra), pero el valor sin formato real es simplemente un recuento (el número de veces que se ha producido una cosa determinada en total). Para generar el valor con formato "rate", debe aplicar la fórmula correspondiente al tipo de contador. La fórmula de `PERF_SAMPLE_COUNTER` es `(N1 - N0) / ((T1 - T0) / F)` : reste el valor del ejemplo actual del valor del ejemplo anterior (que indica el número de veces que se ha producido el evento durante el intervalo de muestra) y, a continuación, divida el resultado por el número de segundos del intervalo de muestra (se obtiene restando la marca de tiempo del ejemplo actual de la marca de tiempo del ejemplo anterior y dividiendo por frecuencia para convertir

Consulte [calcular valores de contadores](calculating-counter-values.md) para obtener más información sobre cómo calcular valores con formato a partir de valores sin formato.

## <a name="sample"></a>Muestra

El código siguiente implementa un consumidor que usa las funciones de consumidor de PerfLib v2 para leer la información de rendimiento de la CPU del CounterSet "información de procesador".

El consumidor se organiza de la manera siguiente:

- La `CpuPerfCounters` clase implementa la lógica para consumir datos de rendimiento. Encapsula un identificador de consulta y un búfer de datos en el que se registran los resultados de la consulta.
- La `CpuPerfTimestamp` estructura almacena la información de marca de tiempo de un ejemplo. Cada vez que se recopilan datos, el autor de la llamada recibe un único `CpuPerfTimestamp` .
- La `CpuPerfData` estructura almacena la información de rendimiento (el nombre de instancia y los valores de rendimiento sin procesar) de una CPU. Cada vez que se recopilan datos, el autor de la llamada recibe una matriz de `CpuPerfData` (una por CPU).

Este ejemplo usa los valores de identificador de contador y GUID de CounterSet codificados de forma rígida porque está optimizado para un CounterSet específico (información del procesador) que no cambiará los valores de GUID o ID. Una clase más genérica que lee los datos de rendimiento de los contraconjuntos arbitrarios necesitaría usar **PerfQueryCounterSetRegistrationInfo** para buscar la asignación entre los identificadores de contador y los valores de contador en tiempo de ejecución.

Un `CpuPerfCountersConsumer.cpp` programa sencillo muestra cómo usar los valores de la `CpuPerfCounters` clase.

### <a name="cpuperfcountersh"></a>CpuPerfCounters. h

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a>CpuPerfCounters. cpp

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a>CpuPerfCountersConsumer. cpp

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
