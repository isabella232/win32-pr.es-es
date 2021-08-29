---
description: Use las siguientes funciones para consumir y proporcionar datos de rendimiento.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Funciones de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: b5d93bb23bf6a7b26d9f869e829416aec3d66ac3daa1c8f408e4959b062b187e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624975"
---
# <a name="performance-counters-functions"></a>Funciones de contadores de rendimiento

Use las siguientes funciones para consumir y proporcionar datos de rendimiento.

## <a name="consumer-functions"></a>Funciones de consumidor

### <a name="performance-data-helper-pdh-functions"></a>Funciones del asistente de datos de rendimiento (PDH)

Use las funciones del asistente de datos de rendimiento (PDH) para consumir datos de rendimiento de los proveedores de datos de rendimiento V1 y V2.

> [!Note]
> Windows OneCore aplicaciones no pueden usar las funciones PDH. Si va a escribir aplicaciones Windows OneCore, use las funciones de consumidor [de PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md).

- [*CounterPathCallBack*](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [**PdhBrowseCountersH**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [**PdhCollectQueryDataWithTime**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [**PdhConnectMachine**](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [**PdhEnumLogSetNames**](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [**PdhEnumMachines**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [**PdhEnumMachinesH**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [**PdhEnumObjectItemsH**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [**PdhEnumObjectsH**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [**PdhExpandCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [**PdhExpand HaddCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [**PdhExpand HaddCardPathH**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [**PdhGetCounterInfo**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [**PdhGetDataSourceTimeRangeH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [**PdhGetDefaultPerfCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [**PdhGetDefaultPerfCounterH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [**PdhGetDefaultPerfObject**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [**PdhGetDefaultPerfObjectH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [**PdhGetDllVersion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [**PdhIsRealTimeQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [**PdhLookupPerfIndexByName**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [**PdhLookupPerfNameByIndex**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [**PdhReadRawLogRecord**](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [**PdhSetDefaultRealTimeDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [**PdhUpdateLogFileCatalog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [**PdhValidatePathEx**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a>Funciones de consumidor de PerfLib V2

Use las funciones perfLib V2 Consumer para consumir datos de rendimiento de proveedores de datos de rendimiento V2 si no puede usar las funciones del Asistente de datos de rendimiento (PDH). Estas funciones se pueden usar al escribir OneCore aplicaciones para recopilar conjuntos de contadores V2 o cuando necesite recopilar conjuntos de contadores V2 específicos con dependencias mínimas y sobrecarga.

> [!TIP]
> Las funciones perfLib V2 Consumer son más difíciles de usar que las funciones del asistente de datos de rendimiento (PDH) y solo admiten la recopilación de datos de proveedores V2. Las funciones PDH deben ser preferidas para la mayoría de las aplicaciones.

- [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a>Funciones de proveedor

### <a name="perflib-v2-provider-functions"></a>Funciones del proveedor de PerfLib V2

[Los proveedores de datos de rendimiento V2](providing-counter-data-using-version-2-0.md) usan las siguientes funciones:

- [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [**CounterCleanup**](countercleanup.md)
- [**CounterInitialize**](counterinitialize.md)
- [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [**PerfQueryInstance**](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [**PerfStartProviderEx**](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> Para instalar y desinstalar proveedores V2, use las herramientas **lodctr** **y unlodctr.** Las **funciones LoadPerfCounterTextStrings** y **UnloadPerfCounterTextStrings** no se pueden usar para instalar y desinstalar proveedores V2.

### <a name="performance-dll-functions"></a>Funciones DLL de rendimiento

[Los proveedores de datos de rendimiento V1](providing-counter-data-using-a-performance-dll.md) implementan un archivo DLL que proporciona las siguientes funciones:

- [*ClosePerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [*CollectPerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- [*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

> [!Note]
> Debido a problemas importantes de rendimiento y confiabilidad, los proveedores de datos de rendimiento V1 están en desuso. Aunque todavía puede usar un archivo DLL de extensión de rendimiento para proporcionar datos de contador, se recomienda crear un [proveedor V2](providing-counter-data-using-version-2-0.md) en su lugar. También se recomienda reemplazar los proveedores V1 existentes por proveedores V2.

Los proveedores V1 se pueden instalar y desinstalar mediante las herramientas **lodctr** y **unlodctr** o mediante una llamada a las siguientes funciones:

- [**LoadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
