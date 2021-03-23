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
# <a name="fence-based-resource-management"></a>Administración de recursos Fence-Based

Muestra cómo administrar la duración de los datos de recursos mediante el seguimiento del progreso de la GPU a través de vallas. La memoria se puede reutilizar eficazmente con barreras administrando cuidadosamente la disponibilidad de espacio libre en memoria, como en una implementación de búfer de anillo para un montón de carga.

-   [Escenario de búfer en anillo](#ring-buffer-scenario)
-   [Ejemplo de búfer en anillo](#ring-buffer-sample)
-   [Temas relacionados](#related-topics)

## <a name="ring-buffer-scenario"></a>Escenario de búfer en anillo

A continuación se presenta un ejemplo en el que una aplicación experimenta una demanda poco frecuente de carga de memoria del montón.

Un búfer en anillo es una manera de administrar un montón de carga. El búfer en anillo contiene los datos necesarios para los siguientes fotogramas. La aplicación mantiene un puntero de entrada de datos actual y una cola de desplazamiento de fotogramas para registrar cada fotograma y el desplazamiento de inicio de los datos de recursos para ese marco.

Una aplicación crea un búfer de anillo basado en un búfer para cargar datos en la GPU de cada fotograma. Actualmente se ha representado el marco 2, el búfer en anillo se ajusta en torno a los datos del fotograma 4, todos los datos necesarios para el marco 5 está presente y es necesario subasignar un búfer de constantes grande requerido para el marco 6.

**Figura 1** : la aplicación intenta la subasignación para el búfer de constantes, pero no tiene suficiente memoria libre.

![memoria libre insuficiente en este búfer en anillo](images/ring-buffer-1.png)

**Figura 2** : a través del sondeo de barrera, la aplicación detecta que se ha representado el fotograma 3, la cola de desplazamiento de fotogramas se actualiza y el estado actual del búfer de anillo sigue, sin embargo, la memoria libre todavía no es suficientemente grande para alojar el búfer de constantes.

![no hay memoria suficiente después de representar el fotograma 3](images/ring-buffer-2.png)

**Figura 3** : dada la situación, la CPU se bloquea (a través de barrera en espera) hasta que se representa el marco 4, lo que libera la memoria subasignada para el marco 4.

![la representación del fotograma 4 libera más espacio en el búfer en anillo](images/ring-buffer-3.png)

**Figura 4** : ahora la memoria libre es suficientemente grande para el búfer de constantes y la subasignación se realiza correctamente. la aplicación copia los datos de búfer de constantes grandes en la memoria usada anteriormente por los datos de recursos para los marcos 3 y 4. El puntero de entrada actual se ha actualizado por última vez.

![Ahora hay espacio desde el fotograma 6 en el búfer de anillo.](images/ring-buffer-4.png)

Si una aplicación implementa un búfer en anillo, el búfer en anillo debe ser lo suficientemente grande como para admitir el escenario de peor caso de los tamaños de los datos de recursos.

## <a name="ring-buffer-sample"></a>Ejemplo de búfer en anillo

En el código de ejemplo siguiente se muestra cómo se puede administrar un búfer en anillo y se presta atención a la rutina de subasignación que controla el sondeo de barrera y la espera. Para simplificar, el ejemplo utiliza \_ memoria insuficiente \_ para ocultar los detalles de "no hay suficiente memoria libre en el montón", ya que esa lógica (basada en *m \_ pDataCur* y desplazamientos dentro de *FrameOffsetQueue*) no está estrechamente relacionada con los montones o las barreras. El ejemplo se ha simplificado para sacrificar la velocidad de fotogramas en lugar de la utilización de memoria.

Tenga en cuenta que se espera que la compatibilidad con el búfer de anillo sea un escenario popular; sin embargo, el diseño del montón no impide el uso de otros, como la parametrización y reutilización de la lista de comandos.

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

[Subasignación dentro de búferes](large-buffers.md)
</dt> </dl>

 

 




