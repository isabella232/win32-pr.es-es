---
title: Contadores de salida de flujo
description: La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104581"
---
# <a name="stream-output-counters"></a><span data-ttu-id="cc6a2-104">Contadores de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="cc6a2-104">Stream Output Counters</span></span>

<span data-ttu-id="cc6a2-105">La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="cc6a2-106">Los contadores de salida de flujo supervisan el progreso.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="cc6a2-107">Diferencias en los contadores de flujo de Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cc6a2-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="cc6a2-108">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="cc6a2-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="cc6a2-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc6a2-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="cc6a2-110">Diferencias en los contadores de flujo de Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cc6a2-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="cc6a2-111">Como parte del proceso de salida de la secuencia, la GPU tiene que conocer la ubicación actual en el búfer en el que está escribiendo.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="cc6a2-112">En Direct3D 11, la memoria para almacenar esta ubicación está asignada por el controlador y la única manera en que las aplicaciones manipulan este valor es a través del método **SOSetTargets** .</span><span class="sxs-lookup"><span data-stu-id="cc6a2-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="cc6a2-113">En Direct3D 12, las aplicaciones asignan memoria para almacenar esta ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="cc6a2-114">No hay ninguna manera especial de manipular este valor y las aplicaciones pueden leer y escribir el valor con la CPU o la GPU.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="cc6a2-115">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="cc6a2-115">BufferFilledSize</span></span>

<span data-ttu-id="cc6a2-116">La aplicación es responsable de la asignación de almacenamiento para una cantidad de 32 bits llamada *BufferFilledSize*.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="cc6a2-117">Contiene el número de bytes de datos en el búfer de salida de flujo.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="cc6a2-118">Este almacenamiento se puede colocar en el mismo recurso, o en otro diferente, que el que contiene los datos de salida de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="cc6a2-119">La GPU tiene acceso a este valor en la fase Stream-Output para determinar dónde se deben anexar los nuevos datos de vértice en el búfer.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="cc6a2-120">Además, la GPU accede a este valor para determinar cuándo se ha producido el desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="cc6a2-121">Consulte la D3D12 de la estructura de [**\_ salida de Stream \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span><span class="sxs-lookup"><span data-stu-id="cc6a2-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="cc6a2-122">El nivel de depuración validará lo siguiente en [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="cc6a2-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="cc6a2-123">*BufferFilledSize* se encuentra en el intervalo implícito por {*OffsetInBytes*, *SizeInBytes*}, si se especifica un recurso que no es NULL.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="cc6a2-124">*BufferFilledSizeOffsetInBytes* es un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="cc6a2-125">*BufferFilledSizeOffsetInBytes* está dentro del intervalo del recurso que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="cc6a2-126">El recurso especificado es un búfer.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="cc6a2-127">El runtime no validará el tipo de montón asociado al búfer de salida de flujo, ya que la salida de flujo se admite en todos los tipos de montón.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="cc6a2-128">Las signaturas de raíz deben especificar si se va a utilizar la salida de flujo mediante las marcas de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .</span><span class="sxs-lookup"><span data-stu-id="cc6a2-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="cc6a2-129">\_La marca de firma raíz de D3D12 \_ \_ \_ permite \_ \_ especificar la salida de secuencia para las signaturas raíz creadas en HLSL, de forma similar a la forma en que se especifican las demás marcas.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="cc6a2-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) producirá un error si el sombreador de geometría contiene el flujo de salida, pero la firma raíz no tiene el \_ indicador de firma raíz D3D12 \_ permitir el marcador de salida de \_ \_ \_ secuencia \_ establecido.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="cc6a2-131">Cuando se usa un recurso como destino de salida de flujo, los recursos usados deben estar en el estado de la \_ transmisión por secuencias de estado de recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc6a2-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="cc6a2-132">Esto se aplica tanto a los datos de vértice como a los *BufferFilledSize* (que pueden estar en el mismo o en recursos independientes).</span><span class="sxs-lookup"><span data-stu-id="cc6a2-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="cc6a2-133">No hay ninguna API especial para establecer desplazamientos de búfer de salida de flujo, ya que las aplicaciones pueden escribir en *BufferFilledSize* directamente con la CPU o la GPU.</span><span class="sxs-lookup"><span data-stu-id="cc6a2-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc6a2-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc6a2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc6a2-135">Contadores y consultas</span><span class="sxs-lookup"><span data-stu-id="cc6a2-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




