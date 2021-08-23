---
title: Administración de recursos basada en límites
description: Muestra cómo administrar el intervalo de vida de los datos de recursos mediante el seguimiento del progreso de la GPU a través de barreras. La memoria se puede volver a usar de forma eficaz con barreras que administran cuidadosamente la disponibilidad del espacio libre en la memoria, como en una implementación de búfer en anillo para un montón Upload anillo.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cbfd9231e3013099c8382072049f1ae1478e28f00830e89fb4ecef1b835ce58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728895"
---
# <a name="fence-based-resource-management"></a>Administración de recursos basada en límites

Muestra cómo administrar el intervalo de vida de los datos de recursos mediante el seguimiento del progreso de la GPU a través de barreras. La memoria se puede volver a usar de forma eficaz con barreras que administran cuidadosamente la disponibilidad del espacio libre en la memoria, como en una implementación de búfer en anillo para un montón Upload anillo.

-   [Escenario de búfer en anillo](#ring-buffer-scenario)
-   [Ejemplo de búfer en anillo](#ring-buffer-sample)
-   [Temas relacionados](#related-topics)

## <a name="ring-buffer-scenario"></a>Escenario de búfer en anillo

A continuación se muestra un ejemplo en el que una aplicación experimenta una demanda poco frecuente de memoria del montón de carga.

Un búfer en anillo es una manera de administrar un montón de carga. El búfer en anillo contiene los datos necesarios para los siguientes fotogramas. La aplicación mantiene un puntero de entrada de datos actual y una cola de desplazamiento de marco para registrar cada fotograma y el desplazamiento inicial de los datos de recursos para ese marco.

Una aplicación crea un búfer en anillo basado en un búfer para cargar datos en la GPU para cada fotograma. Actualmente se ha representado el fotograma 2, el búfer en anillo se ajusta alrededor de los datos del fotograma 4, todos los datos necesarios para el fotograma 5 están presentes y es necesario asignar un búfer constante grande necesario para el fotograma 6.

**Figura 1:** la aplicación intenta la subasignación para el búfer constante, pero no encuentra suficiente memoria libre.

![memoria libre insuficiente en este búfer en anillo](images/ring-buffer-1.png)

**Figura 2:** a través del sondeo de barrera, la aplicación detecta que se ha representado el fotograma 3, la cola de desplazamiento del marco se actualiza y el estado actual del búfer en anillo sigue; sin embargo, la memoria libre todavía no es lo suficientemente grande como para alojar el búfer constante.

![memoria insuficiente después de que se haya representado el fotograma 3](images/ring-buffer-2.png)

**Figura 3:** Dada la situación, la CPU se bloquea a sí misma (a través de la espera de barrera) hasta que se ha representado el fotograma 4, lo que libera la memoria subasignada para el fotograma 4.

![el marco de representación 4 libera más del búfer en anillo](images/ring-buffer-3.png)

**Figura 4:** ahora la memoria libre es lo suficientemente grande para el búfer constante y la subatribución se realiza correctamente; La aplicación copia los datos de búfer de constantes grandes en la memoria usada anteriormente por los datos de recursos para los fotogramas 3 y 4. El puntero de entrada actual se actualiza finalmente.

![ahora hay espacio del marco 6 en el búfer en anillo](images/ring-buffer-4.png)

Si una aplicación implementa un búfer en anillo, el búfer en anillo debe ser lo suficientemente grande como para hacer frente al escenario peor de los tamaños de los datos de recursos.

## <a name="ring-buffer-sample"></a>Ejemplo de búfer en anillo

El código de ejemplo siguiente muestra cómo se puede administrar un búfer en anillo, prestando atención a la rutina de subatribución que controla el sondeo y la espera de barreras. Para simplificar, el ejemplo usa MEMORIA INSUFICIENTE para ocultar los detalles de "memoria libre insuficiente que se encuentra en el montón", ya que esa lógica (basada en m pDataCur y los desplazamientos dentro de \_ \_ *FrameOffsetQueue)* *\_* no está estrechamente relacionada con montones o barreras. El ejemplo se simplifica para sacrificar la velocidad de fotogramas en lugar del uso de memoria.

Tenga en cuenta que se espera que la compatibilidad con el búfer en anillo sea un escenario popular. sin embargo, el diseño del montón no impide otro uso, como la parametrización de la lista de comandos y la re-utilización.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Subasignación en los búferes](large-buffers.md)
</dt> </dl>

 

 




