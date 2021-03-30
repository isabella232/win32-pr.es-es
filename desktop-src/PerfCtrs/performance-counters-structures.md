---
description: Use las siguientes estructuras al trabajar con datos de rendimiento.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Estructuras de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001963"
---
# <a name="performance-counters-structures"></a><span data-ttu-id="f6c34-103">Estructuras de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f6c34-103">Performance Counters Structures</span></span>

<span data-ttu-id="f6c34-104">Use las siguientes estructuras al trabajar con datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f6c34-104">You use the following structures when working with performance data.</span></span>

<span data-ttu-id="f6c34-105">Para obtener información acerca de las funciones que están disponibles para trabajar con contadores de rendimiento, consulte [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f6c34-105">For information about the functions that are available for working with performance counters, see [Performance Counters Functions](performance-counters-functions.md).</span></span>

## <a name="performance-data-helper-pdh-structures"></a><span data-ttu-id="f6c34-106">Estructuras del ayudante de datos de rendimiento (PDH)</span><span class="sxs-lookup"><span data-stu-id="f6c34-106">Performance Data Helper (PDH) structures</span></span>

<span data-ttu-id="f6c34-107">Los consumidores que usan las funciones del [ayudante de datos de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md) usan las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="f6c34-107">Consumers that use the [Performance Data Helper (PDH)](using-the-pdh-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="f6c34-108">**PDH \_ Browse \_ Dlg \_ config**</span><span class="sxs-lookup"><span data-stu-id="f6c34-108">**PDH\_BROWSE\_DLG\_CONFIG**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [<span data-ttu-id="f6c34-109">**PDH \_ Browse \_ Dlg \_ config \_ H**</span><span class="sxs-lookup"><span data-stu-id="f6c34-109">**PDH\_BROWSE\_DLG\_CONFIG\_H**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [<span data-ttu-id="f6c34-110">**\_información del contador PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-110">**PDH\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [<span data-ttu-id="f6c34-111">**\_elementos de \_ ruta de acceso de contador PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-111">**PDH\_COUNTER\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [<span data-ttu-id="f6c34-112">**\_elementos de \_ ruta de elementos de datos de PDH \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-112">**PDH\_DATA\_ITEM\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [<span data-ttu-id="f6c34-113">**VALOR de de PDH \_ FMT \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-113">**PDH\_FMT\_COUNTERVALUE**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [<span data-ttu-id="f6c34-114">**\_elemento de \_ contravalor de PDH FMT \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-114">**PDH\_FMT\_COUNTERVALUE\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [<span data-ttu-id="f6c34-115">**\_contador sin formato de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-115">**PDH\_RAW\_COUNTER**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [<span data-ttu-id="f6c34-116">**\_elemento de \_ contador sin formato PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-116">**PDH\_RAW\_COUNTER\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [<span data-ttu-id="f6c34-117">**\_registro de \_ registro sin procesar de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-117">**PDH\_RAW\_LOG\_RECORD**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [<span data-ttu-id="f6c34-118">**estadísticas de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-118">**PDH\_STATISTICS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [<span data-ttu-id="f6c34-119">**\_información de hora de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-119">**PDH\_TIME\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a><span data-ttu-id="f6c34-120">Estructuras de consumidor de PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="f6c34-120">PerfLib V2 Consumer structures</span></span>

<span data-ttu-id="f6c34-121">Los consumidores que usan las funciones de [consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) usan las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="f6c34-121">Consumers that use the [PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="f6c34-122">**\_datos de contadores de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-122">**PERF\_COUNTER\_DATA**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [<span data-ttu-id="f6c34-123">**\_encabezado del contador de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-123">**PERF\_COUNTER\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [<span data-ttu-id="f6c34-124">**\_identificador del contador de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-124">**PERF\_COUNTER\_IDENTIFIER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [<span data-ttu-id="f6c34-125">**\_información de \_ registro del contador de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-125">**PERF\_COUNTER\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [<span data-ttu-id="f6c34-126">**\_información de \_ registro de COUNTERSET de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-126">**PERF\_COUNTERSET\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [<span data-ttu-id="f6c34-127">**\_encabezado de datos de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-127">**PERF\_DATA\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [<span data-ttu-id="f6c34-128">**\_encabezado de instancia de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-128">**PERF\_INSTANCE\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [<span data-ttu-id="f6c34-129">**\_contadores de rendimiento múltiple \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-129">**PERF\_MULTI\_COUNTERS**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [<span data-ttu-id="f6c34-130">**\_instancias múltiples de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-130">**PERF\_MULTI\_INSTANCES**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [<span data-ttu-id="f6c34-131">**\_encabezado de \_ búfer de cadena de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-131">**PERF\_STRING\_BUFFER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [<span data-ttu-id="f6c34-132">**\_encabezado de \_ contador de cadena de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-132">**PERF\_STRING\_COUNTER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a><span data-ttu-id="f6c34-133">Estructuras de proveedor de PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="f6c34-133">PerfLib V2 Provider structures</span></span>

<span data-ttu-id="f6c34-134">Los [proveedores de datos de rendimiento V2](providing-counter-data-using-version-2-0.md) usan las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="f6c34-134">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following structures:</span></span>

- [<span data-ttu-id="f6c34-135">**\_identidad del contador de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-135">**PERF\_COUNTER\_IDENTITY**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="f6c34-136">**\_información del contador de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-136">**PERF\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="f6c34-137">**\_información de COUNTERSET de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-137">**PERF\_COUNTERSET\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="f6c34-138">**\_instancia de COUNTERSET de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-138">**PERF\_COUNTERSET\_INSTANCE**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [<span data-ttu-id="f6c34-139">**\_contexto del proveedor de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-139">**PERF\_PROVIDER\_CONTEXT**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a><span data-ttu-id="f6c34-140">Estructuras de DLL de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f6c34-140">Performance DLL structures</span></span>

<span data-ttu-id="f6c34-141">Los [proveedores de archivos dll de extensión de rendimiento](providing-counter-data-using-a-performance-dll.md) y los [consumidores que usan las funciones del registro para consumir datos de contador](using-the-registry-functions-to-consume-counter-data.md) usan las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="f6c34-141">[Performance extension DLL providers](providing-counter-data-using-a-performance-dll.md) and [consumers that use the registry functions to consume counter data](using-the-registry-functions-to-consume-counter-data.md) use the following structures:</span></span>

- [<span data-ttu-id="f6c34-142">**\_bloque de contadores de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-142">**PERF\_COUNTER\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [<span data-ttu-id="f6c34-143">**\_definición del contador de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-143">**PERF\_COUNTER\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [<span data-ttu-id="f6c34-144">**\_bloque de datos de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-144">**PERF\_DATA\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [<span data-ttu-id="f6c34-145">**definición de la instancia de rendimiento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-145">**PERF\_INSTANCE\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [<span data-ttu-id="f6c34-146">**\_tipo de objeto de rendimiento \_**</span><span class="sxs-lookup"><span data-stu-id="f6c34-146">**PERF\_OBJECT\_TYPE**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
