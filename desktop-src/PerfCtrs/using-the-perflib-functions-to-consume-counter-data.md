---
title: Uso de funciones PerfLib para consumir datos de contadores
description: Las funciones de LA API de PerfLib se pueden usar para consumir datos del contador de rendimiento V2 directamente cuando no se puede usar PDH.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 154ce2e60df34fc91f83f2b51b48d78cf170191091df55b85b44560ae271ce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033155"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>Uso de funciones PerfLib para consumir datos de contadores

Use las funciones consumidoras de PerfLib para consumir datos de rendimiento de proveedores de datos de rendimiento V2 cuando no se puedan usar las funciones del asistente de datos de rendimiento [(PDH).](using-the-pdh-functions-to-consume-counter-data.md) Estas funciones se pueden usar al escribir OneCore para recopilar contraconjuntos V2 o cuando necesite recopilar conjuntos de contadores V2 con dependencias mínimas y sobrecarga.

> [!TIP]
> Las funciones perfLib V2 Consumer son más difíciles de usar que las funciones del asistente de datos de rendimiento (PDH) y solo admiten la recopilación de datos de proveedores V2. Las funciones PDH deben ser preferibles para la mayoría de las aplicaciones.

Las funciones de consumidor de PerfLib V2 son la API de bajo nivel para recopilar datos de **proveedores V2.** Las funciones consumidoras de PerfLib V2 no admiten la recopilación de datos de **proveedores V1.**

> [!WARNING]
> Las funciones de consumidor perfLib V2 pueden recopilar datos de orígenes que no son de confianza, por ejemplo, de servicios locales con privilegios limitados o de máquinas remotas. Las funciones de consumidor de PerfLib V2 no validan la integridad ni la coherencia de los datos. La aplicación consumidora debe comprobar que los datos devueltos son coherentes, por ejemplo, que los valores size del bloque de datos devuelto no superan el tamaño real del bloque de datos devuelto. Esto es especialmente importante cuando la aplicación de consumidor se ejecuta con privilegios elevados.

## <a name="perflib-usage"></a>Uso de PerfLib

El encabezado incluye las declaraciones que usan los proveedores de modo de usuario V2 (es decir, la API del proveedor perfLib) y los `perflib.h` consumidores V2 (es decir, perfLib Consumer API). Declara las siguientes funciones para consumir datos de rendimiento V2:

- Use [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) para obtener los GUID de los contraconjuntos registrados por los proveedores V2 en el sistema.
- Use [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) para obtener información sobre un conjunto de contadores determinado, como el nombre, la descripción, el tipo (instancia única o de varias instancias), los tipos de contador, los nombres de contador y las descripciones de los contadores.
- Use [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) para obtener los nombres de las instancias actualmente activas de un conjunto de contadores de varias instancias.
- Use [**PerfOpenQueryHandle para**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) crear un nuevo identificador de consulta que se usará para recopilar datos de uno o varios conjuntos de contadores.
- Use [**PerfCloseQueryHandle para**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) cerrar un identificador de consulta.
- Use [**PerfAddCounters para**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) agregar una consulta a un identificador de consulta.
- Use [**PerfDeleteCounters para**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) quitar una consulta de un identificador de consulta.
- Use [**PerfQueryCounterInfo para**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) obtener información sobre las consultas actuales en un identificador de consulta.
- Use [**PerfQueryCounterData para**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) recopilar los datos de rendimiento de un identificador de consulta.

Si el consumidor va a consumir datos solo de un proveedor específico en el que el GUID y los índices de contador son estables y tiene acceso al archivo de símbolos generado por [CTRPP](ctrpp.md)(desde el parámetro CTRPP), puede codificar de forma hard-code los valores guid y de índice de contador en `-ch` el consumidor.

De lo contrario, deberá cargar los metadatos del conjunto de contadores para determinar los GUID del conjunto de contadores y los índices de contadores que se usarán en la consulta de la siguiente manera:

- Use **PerfEnumerateCounterSet para** obtener una lista de GUID de conjuntos de contadores admitidos.
- Para cada GUID, use **PerfQueryCounterSetRegistrationInfo para** cargar el nombre del contraconjunto. Detén cuando encuentre el nombre que está buscando.
- Use **PerfQueryCounterSetRegistrationInfo** para cargar los metadatos restantes (configuración del conjunto de contadores, nombres de contador, índices de contadores, tipos de contadores) para ese conjunto de contadores.

Si solo necesita conocer los nombres de las instancias actualmente activas de un conjunto de contadores (es decir, si no necesita los valores de datos de rendimiento reales), puede usar **PerfEnumerateCounterSetInstances**. Esto toma un GUID de conjunto de contadores como entrada y devuelve un bloque con los nombres y los identificadores de las instancias actualmente activas del `PERF_INSTANCE_HEADER` contraconjunto especificado.

### <a name="queries"></a>Consultas

Para recopilar datos de rendimiento, debe crear un identificador de consulta, agregarle consultas y recopilar los datos de las consultas.

Un identificador de consulta puede tener muchas consultas asociadas. Al llamar a **PerfQueryCounterData** para un identificador de consulta, PerfLib ejecutará todas las consultas del identificador y recopilará todos los resultados.

Cada consulta especifica un GUID de conjunto de contadores, un filtro de nombre de instancia, un filtro de identificador de instancia opcional y un filtro de identificador de contador opcional.

- Se requiere el GUID del conjunto de contadores. Indica el GUID del contraconjunto del que la consulta recopilará datos. Esto es similar a la `FROM` cláusula de una SQL consulta.
- Se requiere el filtro de nombre de instancia. Indica un patrón de caracteres comodín que el nombre de instancia debe coincidir para que la instancia se incluya en la consulta, indicando `*` "cualquier carácter" e `?` indicando "un carácter". Para los conjuntos de contadores de instancia única, **debe** establecerse en una cadena de longitud cero `""` . Para los conjuntos de contadores de instancias **múltiples,** debe establecerse en una cadena no vacía (use `"*"` para aceptar todos los nombres de instancia). Esto es similar a una `WHERE InstanceName LIKE NameFilter` cláusula de una SQL consulta.
- El filtro de identificador de instancia es opcional. Si está presente (es decir, si se establece en un valor distinto de ), indica que la consulta solo debe recopilar instancias donde el identificador de instancia coincide con `0xFFFFFFFF` el identificador especificado. Si no está presente (es decir, si se establece en ), indica que la consulta `0xFFFFFFFF` debe aceptar todos los iD de instancia. Esto es similar a una `WHERE InstanceId == IdFilter` cláusula de una SQL consulta.
- El filtro de identificador de contador es opcional. Si está presente (es decir, si se establece en un valor distinto de ), indica que la consulta debe recopilar un único contador, similar a una cláusula de una `PERF_WILDCARD_COUNTER` `SELECT CounterName` SQL consulta. Si no está presente (es decir, si se establece en ), indica que la consulta debe recopilar todos los contadores disponibles, de forma similar a una cláusula de una `PERF_WILDCARD_COUNTER` `SELECT *` SQL consulta.

Use **PerfAddCounters para** agregar consultas a un identificador de consulta. Use **PerfDeleteCounters para** quitar consultas de un identificador de consulta.

Después de cambiar las consultas de un identificador de consulta, use **PerfQueryCounterInfo para** obtener los índices de consulta. Los índices indican el orden en el que **PerfQueryCounterData** devolverá los resultados de la consulta (los resultados no siempre coincidirán con el orden en que se agregaron las consultas).

Una vez que el identificador de consulta esté listo, use **PerfQueryCounterData** para recopilar los datos. Normalmente, recopilará los datos periódicamente (una vez por segundo o una vez por minuto) y los procesará según sea necesario.

> [!NOTE]
> Los contadores de rendimiento no están diseñados para recopilarse más de una vez por segundo.

**PerfQueryCounterData** devolverá un bloque , que consta de un encabezado de datos con marcas de tiempo seguidas de una secuencia de bloques, cada uno de los cuales contiene los `PERF_DATA_HEADER` resultados `PERF_COUNTER_HEADER` de una consulta.

puede contener varios tipos diferentes de datos, como indica `PERF_COUNTER_HEADER` el valor del campo `dwType` :

- `PERF_ERROR_RETURN` - PerfLib no puede obtener datos de contador válidos del proveedor.
- `PERF_SINGLE_COUNTER` - La consulta era para un único contador de un conjunto de contadores de instancia única. Los resultados contienen solo el valor de contador solicitado.
- `PERF_MULTIPLE_COUNTERS` - La consulta era para varios contadores de un conjunto de contadores de instancia única. El resultado contiene los valores de contador junto con información para hacer coincidir cada valor con el contador correspondiente (es decir, los encabezados de columna).
- `PERF_MULTIPLE_INSTANCES` - La consulta era para un único contador de un conjunto de contadores de varias instancias. Los resultados contienen la información de instancia (es decir, encabezados de fila) y un valor de contador por instancia.
- `PERF_COUNTERSET` - La consulta era para varios contadores de un conjunto de contadores de varias instancias. Los resultados contienen la información de instancia (es decir, encabezados de fila), los valores de contador de cada instancia e información para hacer coincidir cada valor con el contador correspondiente (es decir, encabezados de columna).

Los valores devueltos **por PerfQueryCounterData** son `UINT32` o valores sin `UINT64` procesar. Normalmente, requieren algún procesamiento para generar los valores con formato esperados. El procesamiento necesario depende del tipo del contador. Muchos tipos de contador requieren información adicional para el procesamiento completo, como una marca de tiempo o un valor de un contador "base" en el mismo ejemplo.

Algunos tipos de contadores son contadores "delta" que solo son significativos cuando se comparan con los datos de un ejemplo anterior. Por ejemplo, un contador de tipo tiene un valor con formato que se espera que muestre una tasa (el número de veces que se produjo una cosa determinada por segundo durante el intervalo de muestra), pero el valor sin procesar real es solo un recuento (el número de veces que ha ocurrido una cosa determinada `PERF_SAMPLE_COUNTER` en total). Para generar el valor "rate" con formato, debe aplicar la fórmula correspondiente al tipo de contador. La fórmula para es : restar el valor de la muestra actual del valor de la muestra anterior (lo que proporciona el número de veces que se produjo el evento durante el intervalo de muestra) y, a continuación, dividir el resultado por el número de segundos del intervalo de muestra (obtenido restando la marca de tiempo de la muestra actual de la marca de tiempo de la muestra anterior y dividiendo por frecuencia para convertir el intervalo de tiempo en `PERF_SAMPLE_COUNTER` `(N1 - N0) / ((T1 - T0) / F)` segundos).

Consulte [Cálculo de valores de contador para](calculating-counter-values.md) obtener más información sobre la computación de valores con formato a partir de valores sin procesar.

## <a name="sample"></a>Muestra

El código siguiente implementa un consumidor que usa las funciones Consumidor de PerfLib V2 para leer la información de rendimiento de la CPU desde el contraconjunto "Información del procesador".

El consumidor se organiza de la siguiente manera:

- La `CpuPerfCounters` clase implementa la lógica para consumir datos de rendimiento. Encapsula un identificador de consulta y un búfer de datos en el que se registran los resultados de la consulta.
- La `CpuPerfTimestamp` estructura almacena la información de marca de tiempo de un ejemplo. Cada vez que se recopilan datos, el autor de la llamada recibe un único `CpuPerfTimestamp` .
- La estructura almacena la información de rendimiento (nombre de instancia `CpuPerfData` y valores de rendimiento sin procesar) de una CPU. Cada vez que se recopilan datos, el autor de la llamada recibe una matriz `CpuPerfData` de (una por CPU).

En este ejemplo se usan valores de GUID y de identificador de contador codificados de forma hard-coded porque está optimizado para un conjunto de contadores específico (información del procesador) que no cambiará los valores GUID o ID. Una clase más genérica que lee datos de rendimiento de conjuntos de contadores arbitrarios tendría que usar **PerfQueryCounterSetRegistrationInfo** para buscar la asignación entre los valores de contador y los de contador en tiempo de ejecución.

Un programa `CpuPerfCountersConsumer.cpp` simple muestra cómo usar los valores de la clase `CpuPerfCounters` .

### <a name="cpuperfcountersh"></a>CpuPerfCounters.h

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

### <a name="cpuperfcounterscpp"></a>CpuPerfCounters.cpp

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

### <a name="cpuperfcountersconsumercpp"></a>CpuPerfCountersConsumer.cpp

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
