---
title: Contadores de UAV
description: Puede usar contadores de acceso sin ordenar (UAV) para asociar un contador atómico de 32 bits con un desordenado-Access-View (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104549105"
---
# <a name="uav-counters"></a><span data-ttu-id="d5314-103">Contadores de UAV</span><span class="sxs-lookup"><span data-stu-id="d5314-103">UAV Counters</span></span>
<span data-ttu-id="d5314-104">Puede usar contadores de acceso sin ordenar (UAV) para asociar un contador atómico de 32 bits con un desordenado-Access-View (UAV).</span><span class="sxs-lookup"><span data-stu-id="d5314-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="d5314-105">Diferencias en los contadores de UAV de Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d5314-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="d5314-106">Las aplicaciones de Direct3D 12 y Direct3D 11 usan las mismas funciones de sombreador de lenguaje de sombreado de alto nivel (HLSL) para tener acceso a los contadores de UAV.</span><span class="sxs-lookup"><span data-stu-id="d5314-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="d5314-107">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="d5314-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="d5314-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="d5314-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="d5314-109">**Append**</span><span class="sxs-lookup"><span data-stu-id="d5314-109">**Append**</span></span>
-   <span data-ttu-id="d5314-110">**Consumo**</span><span class="sxs-lookup"><span data-stu-id="d5314-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="d5314-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d5314-111">Direct3D 12</span></span>
<span data-ttu-id="d5314-112">En Direct3D 12, la aplicación asigna los valores de 32 bits, por lo que los valores de 32 bits se pueden leer y escribir en la CPU o la GPU, como cualquier otro recurso de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d5314-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="d5314-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d5314-113">Direct3D 11</span></span>
<span data-ttu-id="d5314-114">Fuera de los sombreadores, con Direct3D 11 debe llamar a los métodos de la API para tener acceso a los contadores (por ejemplo, [ID3D11DeviceContext:: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span><span class="sxs-lookup"><span data-stu-id="d5314-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="d5314-115">Uso de contadores de UAV</span><span class="sxs-lookup"><span data-stu-id="d5314-115">Using UAV counters</span></span>
<span data-ttu-id="d5314-116">La aplicación es responsable de asignar 32 bits de almacenamiento para los contadores de UAV.</span><span class="sxs-lookup"><span data-stu-id="d5314-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="d5314-117">Este almacenamiento se puede asignar en otro recurso como el que contiene los datos accesibles a través de UAV.</span><span class="sxs-lookup"><span data-stu-id="d5314-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="d5314-118">Consulte [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) y [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span><span class="sxs-lookup"><span data-stu-id="d5314-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="d5314-119">Si *pCounterResource* se especifica en la llamada a [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), hay un contador asociado al UAV.</span><span class="sxs-lookup"><span data-stu-id="d5314-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="d5314-120">En este caso:</span><span class="sxs-lookup"><span data-stu-id="d5314-120">In this case:</span></span>

-   <span data-ttu-id="d5314-121">*StructureByteStride* debe ser mayor que cero</span><span class="sxs-lookup"><span data-stu-id="d5314-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="d5314-122">El formato debe tener el \_ formato DXGI \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="d5314-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="d5314-123">No se debe establecer la marca sin formato</span><span class="sxs-lookup"><span data-stu-id="d5314-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="d5314-124">Ambos recursos deben ser búferes</span><span class="sxs-lookup"><span data-stu-id="d5314-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="d5314-125">*CounterOffsetInBytes* debe ser un múltiplo de 4 bytes</span><span class="sxs-lookup"><span data-stu-id="d5314-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="d5314-126">*CounterOffsetInBytes* debe estar en el intervalo del recurso de contador</span><span class="sxs-lookup"><span data-stu-id="d5314-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="d5314-127">*pDesc* no puede ser null</span><span class="sxs-lookup"><span data-stu-id="d5314-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="d5314-128">el *preorigen* no puede ser nulo</span><span class="sxs-lookup"><span data-stu-id="d5314-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="d5314-129">Y tenga en cuenta los siguientes casos de uso:</span><span class="sxs-lookup"><span data-stu-id="d5314-129">And note the following use cases:</span></span>

-   <span data-ttu-id="d5314-130">Si no se especifica *pCounterResource* , *CounterOffsetInBytes* debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="d5314-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="d5314-131">Si se establece la marca sin formato, el formato debe ser DXGI \_ format \_ R32 \_ y el recurso UAV debe ser un búfer.</span><span class="sxs-lookup"><span data-stu-id="d5314-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="d5314-132">Si no se establece *pCounterResource* , *CounterOffsetInBytes* debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="d5314-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="d5314-133">Si no se establece la marca sin formato y *StructureByteStride* = 0, el formato debe ser un formato UAV válido.</span><span class="sxs-lookup"><span data-stu-id="d5314-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="d5314-134">Direct3D 12 quita la distinción entre Append y Counter UAVs (aunque la distinción todavía existe en el código de bytes HLSL).</span><span class="sxs-lookup"><span data-stu-id="d5314-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="d5314-135">El entorno de tiempo de ejecución principal validará estas restricciones dentro de [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="d5314-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="d5314-136">Durante el envío y la distribución, el recurso de contador debe estar en el estado de [**\_ recurso D3D12 \_ \_ \_ acceso no ordenado**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span><span class="sxs-lookup"><span data-stu-id="d5314-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="d5314-137">Además, dentro de una única llamada a Draw/Dispatch, no es válido para una aplicación tener acceso a la misma ubicación de memoria de 32 bits a través de dos contadores de UAV independientes.</span><span class="sxs-lookup"><span data-stu-id="d5314-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="d5314-138">La capa de depuración emitirá errores si se detecta cualquiera de ellos.</span><span class="sxs-lookup"><span data-stu-id="d5314-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="d5314-139">No hay ningún método "SetUnorderedAccessViewCounterValue" o "CopyStructureCount", ya que las aplicaciones solo pueden copiar directamente los datos hacia y desde el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="d5314-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="d5314-140">Se admite la indexación dinámica de UAVs con contadores.</span><span class="sxs-lookup"><span data-stu-id="d5314-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="d5314-141">Si un sombreador intenta obtener acceso al contador de un UAV que no tiene un contador asociado, la capa de depuración emitirá una advertencia y se producirá un error de página de GPU que hará que se quite el dispositivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5314-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="d5314-142">Los contadores de UAV se admiten en todos los tipos de montón (predeterminado, upload, readback).</span><span class="sxs-lookup"><span data-stu-id="d5314-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5314-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5314-143">Related topics</span></span>

* [<span data-ttu-id="d5314-144">Contadores y consultas</span><span class="sxs-lookup"><span data-stu-id="d5314-144">Counters and queries</span></span>](counters-and-queries.md)