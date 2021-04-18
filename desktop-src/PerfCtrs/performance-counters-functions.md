---
description: Utilice las siguientes funciones para consumir y proporcionar datos de rendimiento.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Funciones de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667285"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="8cfe7-103">Funciones de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="8cfe7-103">Performance Counters Functions</span></span>

<span data-ttu-id="8cfe7-104">Utilice las siguientes funciones para consumir y proporcionar datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="8cfe7-105">Funciones de consumidor</span><span class="sxs-lookup"><span data-stu-id="8cfe7-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="8cfe7-106">Funciones del ayudante de datos de rendimiento (PDH)</span><span class="sxs-lookup"><span data-stu-id="8cfe7-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="8cfe7-107">Utilice las funciones de la aplicación auxiliar de datos de rendimiento (PDH) para consumir los datos de rendimiento de los proveedores de datos de rendimiento V1 y V2.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="8cfe7-108">Las aplicaciones de Windows OneCore no pueden usar las funciones de PDH.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="8cfe7-109">Si está escribiendo aplicaciones de Windows OneCore, use [las funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="8cfe7-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="8cfe7-110">*CounterPathCallBack*</span><span class="sxs-lookup"><span data-stu-id="8cfe7-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="8cfe7-111">**PdhAddCounter**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="8cfe7-112">**PdhAddEnglishCounter**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="8cfe7-113">**PdhBindInputDataSource**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="8cfe7-114">**PdhBrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="8cfe7-115">**PdhBrowseCountersH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="8cfe7-116">**PdhCalculateCounterFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="8cfe7-117">**PdhCloseLog**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="8cfe7-118">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="8cfe7-119">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="8cfe7-120">**PdhCollectQueryDataEx**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="8cfe7-121">**PdhCollectQueryDataWithTime**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="8cfe7-122">**PdhComputeCounterStatistics**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="8cfe7-123">**PdhConnectMachine**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="8cfe7-124">**PdhEnumLogSetNames**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="8cfe7-125">**PdhEnumMachines**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="8cfe7-126">**PdhEnumMachinesH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="8cfe7-127">**PdhEnumObjectItems**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="8cfe7-128">**PdhEnumObjectItemsH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="8cfe7-129">**PdhEnumObjects**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="8cfe7-130">**PdhEnumObjectsH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="8cfe7-131">**PdhExpandCounterPath**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="8cfe7-132">**PdhExpandWildCardPath**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="8cfe7-133">**PdhExpandWildCardPathH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="8cfe7-134">**PdhFormatFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="8cfe7-135">**PdhGetCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="8cfe7-136">**PdhGetCounterTimeBase**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="8cfe7-137">**PdhGetDataSourceTimeRange**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="8cfe7-138">**PdhGetDataSourceTimeRangeH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="8cfe7-139">**PdhGetDefaultPerfCounter**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="8cfe7-140">**PdhGetDefaultPerfCounterH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="8cfe7-141">**PdhGetDefaultPerfObject**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="8cfe7-142">**PdhGetDefaultPerfObjectH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="8cfe7-143">**PdhGetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="8cfe7-144">**PdhGetFormattedCounterArray**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="8cfe7-145">**PdhGetFormattedCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="8cfe7-146">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="8cfe7-147">**PdhGetRawCounterArray**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="8cfe7-148">**PdhGetRawCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="8cfe7-149">**PdhIsRealTimeQuery**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="8cfe7-150">**PdhLookupPerfIndexByName**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="8cfe7-151">**PdhLookupPerfNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="8cfe7-152">**PdhMakeCounterPath**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="8cfe7-153">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="8cfe7-154">**PdhOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="8cfe7-155">**PdhOpenQueryH**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="8cfe7-156">**PdhParseCounterPath**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="8cfe7-157">**PdhParseInstanceName**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="8cfe7-158">**PdhReadRawLogRecord**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="8cfe7-159">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="8cfe7-160">**PdhSelectDataSource**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="8cfe7-161">**PdhSetCounterScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="8cfe7-162">**PdhSetDefaultRealTimeDataSource**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="8cfe7-163">**PdhSetQueryTimeRange**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="8cfe7-164">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="8cfe7-165">**PdhUpdateLogFileCatalog**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="8cfe7-166">**PdhValidatePath**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="8cfe7-167">**PdhValidatePathEx**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="8cfe7-168">Funciones de consumidor de PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="8cfe7-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="8cfe7-169">Use las funciones de consumidor de PerfLib v2 para consumir datos de rendimiento de los proveedores de datos de rendimiento V2 si no puede utilizar las funciones de la aplicación auxiliar de datos de rendimiento (PDH).</span><span class="sxs-lookup"><span data-stu-id="8cfe7-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="8cfe7-170">Estas funciones se pueden usar al escribir aplicaciones de OneCore para recopilar los valores V2 o cuando es necesario recopilar los valores de V2 específicos con las dependencias y la sobrecarga mínimas.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="8cfe7-171">Las funciones de consumidor de PerfLib V2 son más difíciles de usar que las funciones de la aplicación auxiliar de datos de rendimiento (PDH) y solo admiten la recopilación de datos de proveedores de V2.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="8cfe7-172">Las funciones PDH deben ser preferibles para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="8cfe7-173">**PerfAddCounters**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="8cfe7-174">**PerfCloseQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="8cfe7-175">**PerfDeleteCounters**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="8cfe7-176">**PerfEnumerateCounterSet**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="8cfe7-177">**PerfEnumerateCounterSetInstances**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="8cfe7-178">**PerfOpenQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="8cfe7-179">**PerfQueryCounterData**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="8cfe7-180">**PerfQueryCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="8cfe7-181">**PerfQueryCounterSetRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="8cfe7-182">Funciones de proveedor</span><span class="sxs-lookup"><span data-stu-id="8cfe7-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="8cfe7-183">Funciones de proveedor de PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="8cfe7-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="8cfe7-184">Los [proveedores de datos de rendimiento V2](providing-counter-data-using-version-2-0.md) usan las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="8cfe7-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="8cfe7-185">*AllocateMemory*</span><span class="sxs-lookup"><span data-stu-id="8cfe7-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="8cfe7-186">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="8cfe7-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="8cfe7-187">**Limpieza**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="8cfe7-188">**Contrainicializar**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="8cfe7-189">*FreeMemory (*</span><span class="sxs-lookup"><span data-stu-id="8cfe7-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="8cfe7-190">**PerfCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="8cfe7-191">**PerfDecrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="8cfe7-192">**PerfDecrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="8cfe7-193">**PerfDeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="8cfe7-194">**PerfIncrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="8cfe7-195">**PerfIncrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="8cfe7-196">**PerfQueryInstance**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="8cfe7-197">**PerfSetCounterSetInfo**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="8cfe7-198">**PerfSetULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="8cfe7-199">**PerfSetULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="8cfe7-200">**PerfSetCounterRefValue**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="8cfe7-201">**PerfStartProvider**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="8cfe7-202">**PerfStartProviderEx**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="8cfe7-203">**PerfStopProvider**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="8cfe7-204">Para instalar y desinstalar proveedores de V2, use las herramientas **LODCTR** y **Unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="8cfe7-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="8cfe7-205">Las funciones **LoadPerfCounterTextStrings** y **UnloadPerfCounterTextStrings** no se pueden usar para instalar y desinstalar proveedores de V2.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="8cfe7-206">Funciones de DLL de rendimiento</span><span class="sxs-lookup"><span data-stu-id="8cfe7-206">Performance DLL functions</span></span>

<span data-ttu-id="8cfe7-207">[V1 los proveedores de datos de rendimiento](providing-counter-data-using-a-performance-dll.md) implementan un archivo DLL que proporciona las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="8cfe7-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="8cfe7-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="8cfe7-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="8cfe7-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="8cfe7-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="8cfe7-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8cfe7-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="8cfe7-211">Debido a problemas de rendimiento y confiabilidad significativos, los proveedores de datos de rendimiento v1 están desusados.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="8cfe7-212">Aunque todavía puede usar un archivo DLL de extensión de rendimiento para proporcionar datos de contador, se recomienda [crear un proveedor V2](providing-counter-data-using-version-2-0.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="8cfe7-213">También se recomienda reemplazar los proveedores de v1 existentes por proveedores de V2.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="8cfe7-214">Los proveedores v1 se pueden instalar y desinstalar mediante las herramientas **LODCTR** y **Unlodctr** , o mediante una llamada a las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="8cfe7-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="8cfe7-215">**LoadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="8cfe7-216">**UnloadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="8cfe7-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
