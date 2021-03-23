---
title: Administración de recursos Fence-Based
description: Muestra cómo administrar la duración de los datos de recursos mediante el seguimiento del progreso de la GPU a través de vallas. La memoria se puede reutilizar eficazmente con barreras administrando cuidadosamente la disponibilidad de espacio libre en memoria, como en una implementación de búfer de anillo para un montón de carga.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104424"
---
# <a name="fence-based-resource-management"></a><span data-ttu-id="0deaf-104">Administración de recursos Fence-Based</span><span class="sxs-lookup"><span data-stu-id="0deaf-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="0deaf-105">Muestra cómo administrar la duración de los datos de recursos mediante el seguimiento del progreso de la GPU a través de vallas.</span><span class="sxs-lookup"><span data-stu-id="0deaf-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="0deaf-106">La memoria se puede reutilizar eficazmente con barreras administrando cuidadosamente la disponibilidad de espacio libre en memoria, como en una implementación de búfer de anillo para un montón de carga.</span><span class="sxs-lookup"><span data-stu-id="0deaf-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="0deaf-107">Escenario de búfer en anillo</span><span class="sxs-lookup"><span data-stu-id="0deaf-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="0deaf-108">Ejemplo de búfer en anillo</span><span class="sxs-lookup"><span data-stu-id="0deaf-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="0deaf-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0deaf-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="0deaf-110">Escenario de búfer en anillo</span><span class="sxs-lookup"><span data-stu-id="0deaf-110">Ring buffer scenario</span></span>

<span data-ttu-id="0deaf-111">A continuación se presenta un ejemplo en el que una aplicación experimenta una demanda poco frecuente de carga de memoria del montón.</span><span class="sxs-lookup"><span data-stu-id="0deaf-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="0deaf-112">Un búfer en anillo es una manera de administrar un montón de carga.</span><span class="sxs-lookup"><span data-stu-id="0deaf-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="0deaf-113">El búfer en anillo contiene los datos necesarios para los siguientes fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0deaf-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="0deaf-114">La aplicación mantiene un puntero de entrada de datos actual y una cola de desplazamiento de fotogramas para registrar cada fotograma y el desplazamiento de inicio de los datos de recursos para ese marco.</span><span class="sxs-lookup"><span data-stu-id="0deaf-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="0deaf-115">Una aplicación crea un búfer de anillo basado en un búfer para cargar datos en la GPU de cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="0deaf-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="0deaf-116">Actualmente se ha representado el marco 2, el búfer en anillo se ajusta en torno a los datos del fotograma 4, todos los datos necesarios para el marco 5 está presente y es necesario subasignar un búfer de constantes grande requerido para el marco 6.</span><span class="sxs-lookup"><span data-stu-id="0deaf-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="0deaf-117">**Figura 1** : la aplicación intenta la subasignación para el búfer de constantes, pero no tiene suficiente memoria libre.</span><span class="sxs-lookup"><span data-stu-id="0deaf-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![memoria libre insuficiente en este búfer en anillo](images/ring-buffer-1.png)

<span data-ttu-id="0deaf-119">**Figura 2** : a través del sondeo de barrera, la aplicación detecta que se ha representado el fotograma 3, la cola de desplazamiento de fotogramas se actualiza y el estado actual del búfer de anillo sigue, sin embargo, la memoria libre todavía no es suficientemente grande para alojar el búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="0deaf-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![no hay memoria suficiente después de representar el fotograma 3](images/ring-buffer-2.png)

<span data-ttu-id="0deaf-121">**Figura 3** : dada la situación, la CPU se bloquea (a través de barrera en espera) hasta que se representa el marco 4, lo que libera la memoria subasignada para el marco 4.</span><span class="sxs-lookup"><span data-stu-id="0deaf-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![la representación del fotograma 4 libera más espacio en el búfer en anillo](images/ring-buffer-3.png)

<span data-ttu-id="0deaf-123">**Figura 4** : ahora la memoria libre es suficientemente grande para el búfer de constantes y la subasignación se realiza correctamente. la aplicación copia los datos de búfer de constantes grandes en la memoria usada anteriormente por los datos de recursos para los marcos 3 y 4.</span><span class="sxs-lookup"><span data-stu-id="0deaf-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="0deaf-124">El puntero de entrada actual se ha actualizado por última vez.</span><span class="sxs-lookup"><span data-stu-id="0deaf-124">The current input pointer is finally updated.</span></span>

![Ahora hay espacio desde el fotograma 6 en el búfer de anillo.](images/ring-buffer-4.png)

<span data-ttu-id="0deaf-126">Si una aplicación implementa un búfer en anillo, el búfer en anillo debe ser lo suficientemente grande como para admitir el escenario de peor caso de los tamaños de los datos de recursos.</span><span class="sxs-lookup"><span data-stu-id="0deaf-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="0deaf-127">Ejemplo de búfer en anillo</span><span class="sxs-lookup"><span data-stu-id="0deaf-127">Ring buffer sample</span></span>

<span data-ttu-id="0deaf-128">En el código de ejemplo siguiente se muestra cómo se puede administrar un búfer en anillo y se presta atención a la rutina de subasignación que controla el sondeo de barrera y la espera.</span><span class="sxs-lookup"><span data-stu-id="0deaf-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="0deaf-129">Para simplificar, el ejemplo utiliza \_ memoria insuficiente \_ para ocultar los detalles de "no hay suficiente memoria libre en el montón", ya que esa lógica (basada en *m \_ pDataCur* y desplazamientos dentro de *FrameOffsetQueue*) no está estrechamente relacionada con los montones o las barreras.</span><span class="sxs-lookup"><span data-stu-id="0deaf-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="0deaf-130">El ejemplo se ha simplificado para sacrificar la velocidad de fotogramas en lugar de la utilización de memoria.</span><span class="sxs-lookup"><span data-stu-id="0deaf-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="0deaf-131">Tenga en cuenta que se espera que la compatibilidad con el búfer de anillo sea un escenario popular; sin embargo, el diseño del montón no impide el uso de otros, como la parametrización y reutilización de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="0deaf-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="0deaf-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0deaf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0deaf-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="0deaf-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="0deaf-134">Subasignación dentro de búferes</span><span class="sxs-lookup"><span data-stu-id="0deaf-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




