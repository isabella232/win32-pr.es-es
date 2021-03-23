---
title: Temporización (gráficos de Direct3D 12)
description: En esta sección se explica cómo consultar las marcas de tiempo y calibrar los contadores de GPU y de marca de tiempo de la CPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2020
ms.locfileid: "104549185"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="be34c-103">Temporización (gráficos de Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="be34c-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="be34c-104">En esta sección se explica cómo consultar las marcas de tiempo y calibrar los contadores de GPU y de marca de tiempo de la CPU.</span><span class="sxs-lookup"><span data-stu-id="be34c-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="be34c-105">Frecuencia de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="be34c-105">Timestamp frequency</span></span>

<span data-ttu-id="be34c-106">La aplicación puede consultar la frecuencia de la marca de tiempo de la GPU en cada cola de comandos (consulte el método [**ID3D12CommandQueue:: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).</span><span class="sxs-lookup"><span data-stu-id="be34c-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="be34c-107">La frecuencia devuelta se mide en Hz (TICs/seg.).</span><span class="sxs-lookup"><span data-stu-id="be34c-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="be34c-108">Si la cola de comandos especificada no admite marcas de tiempo (vea la tabla en la sección [consultas](queries.md) ), se produce un error en esta API (y se devuelve **E_FAIL**).</span><span class="sxs-lookup"><span data-stu-id="be34c-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="be34c-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) y [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) admiten marcas de tiempo siempre.</span><span class="sxs-lookup"><span data-stu-id="be34c-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="be34c-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) opcionalmente admite marcas de tiempo si el miembro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) es **true**.</span><span class="sxs-lookup"><span data-stu-id="be34c-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="be34c-111">Calibración de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="be34c-111">Timestamp calibration</span></span>

<span data-ttu-id="be34c-112">D3D12 permite a las aplicaciones correlacionar los resultados obtenidos de las consultas de marca de tiempo con los resultados obtenidos de la llamada a `QueryPerformanceCounter` .</span><span class="sxs-lookup"><span data-stu-id="be34c-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="be34c-113">Esta opción está habilitada por la llamada a [**ID3D12CommandQueue:: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span><span class="sxs-lookup"><span data-stu-id="be34c-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="be34c-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) muestrea el contador de marca de tiempo de GPU para una cola de comandos determinada y muestrea el contador de CPU a través `QueryPerformanceCounter` de casi al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="be34c-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="be34c-115">De nuevo, se produce un error en esta API (se devuelve E \_ produce un error) si la cola de comandos especificada no admite marcas de tiempo (vea la tabla en el tema [consultas](queries.md) ).</span><span class="sxs-lookup"><span data-stu-id="be34c-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="be34c-116">Tenga en cuenta que los contadores de marca de tiempo de la GPU y la CPU no están necesariamente relacionados directamente con la velocidad del reloj de estos procesadores, sino que trabajan desde TICs de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="be34c-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="be34c-117">Consultas de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="be34c-117">Timestamp queries</span></span>

<span data-ttu-id="be34c-118">Puede obtener marcas de tiempo como parte de una lista de comandos (en lugar de una llamada del lado de la CPU en una cola de comandos) mediante consultas de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="be34c-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="be34c-119">(Consulte [consultas](queries.md) para obtener más información acerca de las consultas en general).</span><span class="sxs-lookup"><span data-stu-id="be34c-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="be34c-120">Todas las consultas de marca de tiempo usan el tipo [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) para la consulta real.</span><span class="sxs-lookup"><span data-stu-id="be34c-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="be34c-121">Sin embargo, debido a las limitaciones de hardware, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) y [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usar un [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) diferente del que utiliza [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) .</span><span class="sxs-lookup"><span data-stu-id="be34c-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="be34c-122">Las colas directas y de proceso usan [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="be34c-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="be34c-123">Las colas de copia usan [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="be34c-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="be34c-124">Las consultas Copy Queue solo se admiten si el miembro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) es **true**.</span><span class="sxs-lookup"><span data-stu-id="be34c-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="be34c-125">Las consultas de marca de tiempo, una vez resueltas a través de [**ID3D12GraphicsCommandList:: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), son un **UINT64** que representa TICs, tal como lo devuelve [**ID3D12CommandQueue:: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)y, como tal, debe dividirse por la frecuencia de la cola para obtener la longitud en segundos.</span><span class="sxs-lookup"><span data-stu-id="be34c-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be34c-126">Para obtener precisión, use aritmética de punto flotante al calcular los intervalos de segundos o milisegundos de las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="be34c-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="be34c-127">Por ejemplo, use `queriedTicks / (double)Frequency` en lugar de `queriedTicks / Frequency`.</span><span class="sxs-lookup"><span data-stu-id="be34c-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be34c-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be34c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be34c-129">Contadores y consultas</span><span class="sxs-lookup"><span data-stu-id="be34c-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="be34c-130">**ID3D12Device::SetStablePowerState**</span><span class="sxs-lookup"><span data-stu-id="be34c-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="be34c-131">**ID3D12Object:: SetName**</span><span class="sxs-lookup"><span data-stu-id="be34c-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="be34c-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="be34c-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="be34c-133">Medición del rendimiento</span><span class="sxs-lookup"><span data-stu-id="be34c-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>
