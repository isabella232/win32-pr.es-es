---
title: Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12
description: Para reducir el uso general de la CPU y habilitar el procesamiento previo y multithreading del controlador, Direct3D 12 mueve la responsabilidad de la administración de Estados por recurso del controlador de gráficos a la aplicación.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549173"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12

Para reducir el uso general de la CPU y habilitar el procesamiento previo y multithreading del controlador, Direct3D 12 mueve la responsabilidad de la administración de Estados por recurso del controlador de gráficos a la aplicación. Un ejemplo de estado por recurso es si se está accediendo actualmente a un recurso de textura a través de un sombreador Vista de recursos o como una vista de destino de representación. En Direct3D 11, los controladores eran necesarios para realizar el seguimiento de este estado en segundo plano. Esto resulta caro desde la perspectiva de la CPU y complica significativamente cualquier tipo de diseño multiproceso. En Microsoft Direct3D 12, la mayoría de los Estados por recurso se administra mediante la aplicación con una sola API, [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

-   [Uso de la API de ResourceBarrier para administrar el estado de cada recurso](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Estados de los recursos](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Estados iniciales de los recursos](#initial-states-for-resources)
    -   [Restricciones de estado de recursos de lectura/escritura](#readwrite-resource-state-restrictions)
    -   [Estados de los recursos para la presentación de búferes de reserva](#resource-states-for-presenting-back-buffers)
    -   [Descartar recursos](#discarding-resources)
-   [Transiciones de estado IMPLÍCITAS](#implicit-state-transitions)
    -   [Promoción de Estado común](#common-state-promotion)
    -   [Caída del estado a común](#state-decay-to-common)
    -   [Implicaciones de rendimiento](#performance-implications)
-   [Barreras divididas](#split-barriers)
-   [Escenario de ejemplo de barrera de recursos](#resource-barrier-example-scenario)
-   [Ejemplo de promoción de Estado común y decadencia](#common-state-promotion-and-decay-sample)
-   [Ejemplo de barreras divididas](#example-of-split-barriers)
-   [Temas relacionados](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Uso de la API de ResourceBarrier para administrar el estado de cada recurso

[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica al controlador de gráficos las situaciones en las que el controlador puede necesitar sincronizar varios accesos a la memoria en la que se almacena un recurso. Se llama al método con una o más estructuras de descripción de barrera de recursos que indican el tipo de barrera de recursos que se declara.

Existen tres tipos de barreras de recursos:

-   **Barrera de transición** : una barrera de transición indica que un conjunto de Subrecursos realiza una transición entre distintos usos. Una estructura de [**barrera de \_ transición de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) se usa para especificar el subrecurso que está cambiando, así como los Estados *antes* y *después* del subrecurso.

    El sistema comprueba que las transiciones de subrecurso en una lista de comandos son coherentes con las transiciones anteriores en la misma lista de comandos. El nivel de depuración realiza un seguimiento adicional del estado de los Subrecursos para buscar otros errores, pero esta validación es conservadora y no es exhaustiva.

    Tenga en cuenta que puede usar la \_ marca de la barrera de recursos D3D12 \_ \_ todos los \_ Subrecursos para especificar que se están realizando las transiciones de todos los Subrecursos de un recurso.

-   **Barrera de alias** : una barrera de alias indica una transición entre los usos de dos recursos diferentes que tienen asignaciones que se superponen en el mismo montón. Esto se aplica a los recursos reservados y colocados. Se utiliza una estructura de [**barrera de \_ alias de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) para especificar el recurso *Before* y el recurso *After* .

    Tenga en cuenta que uno o ambos recursos pueden ser NULL, lo que indica que cualquier recurso en mosaico podría provocar el alias. Para obtener más información sobre el uso de recursos en mosaico [, vea recursos en mosaico y](../direct3d11/tiled-resources.md) recursos en mosaico de [volumen](volume-tiled-resources.md).

-   **Barrera de vista de acceso desordenado (UAV)** : una barrera UAV indica que todos los accesos de UAV, tanto de lectura como de escritura, a un recurso determinado deben completarse entre cualquier acceso de UAV futuro, tanto de lectura como de escritura. No es necesario que una aplicación ponga una barrera UAV entre dos llamadas a Draw o Dispatch que solo se leen de un UAV. Además, no es necesario poner una barrera UAV entre dos llamadas a Draw o Dispatch que escriben en el mismo UAV si la aplicación sabe que es seguro ejecutar el acceso UAV en cualquier orden. Se utiliza una estructura de [**\_ barrera de \_ UAV \_ de recursos D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) para especificar el recurso UAV al que se aplica la barrera. La aplicación puede especificar NULL para el UAV de la barrera, lo que indica que cualquier acceso a UAV podría requerir la barrera.

Cuando se llama a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) con una matriz de descripciones de barrera de recursos, la API se comporta como si se hubiese llamado una vez para cada elemento, en el orden en el que se proporcionaron.

En un momento dado, un subrecurso está en exactamente un estado, determinado por el conjunto de marcas de [**\_ \_ Estados de recursos de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) proporcionadas a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier). La aplicación debe asegurarse de que los Estados *antes* y *después* de las llamadas consecutivas a **ResourceBarrier** coinciden.

> [!TIP]
>
> Las aplicaciones deben procesar por lotes varias transiciones en una llamada API siempre que sea posible.

 

### <a name="resource-states"></a>Estados de los recursos

Para obtener una lista completa de los Estados de los recursos entre los que un recurso puede realizar una transición, vea el tema de referencia de la enumeración de [**\_ \_ Estados de recursos de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

En el caso de las barreras de recursos divididos, consulte también las [**marcas de barrera de recursos de D3D12 \_ \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Estados iniciales de los recursos

Los recursos se pueden crear con cualquier estado inicial especificado por el usuario (válido para la descripción del recurso), con las siguientes excepciones:

-   Los montones de carga deben comenzar en el estado de recurso de D3D12 de \_ \_ \_ \_ lectura Generic Read que es una combinación OR bit a bit de:
    -   D3D12 \_ \_ de estado \_ \_ de recurso \_ y \_ búfer de constantes
    -   \_Búfer de \_ Índice de estado de recurso de D3D12 \_ \_
    -   \_Origen de \_ copia de estado de recurso de D3D12 \_ \_
    -   \_Recurso de \_ \_ \_ \_ sombreador de estado de recursos sin píxeles de \_ D3D12
    -   \_Recurso de \_ \_ \_ sombreador de píxeles de estado \_ de recursos de D3D12
    -   D3D12 \_ \_ \_ argumento indirecto de estado de recurso \_
-   Los montones de Readback deben comenzar en el estado de destino de la copia de estado de recursos de D3D12 \_ \_ \_ \_ .
-   Los búferes de intercambio de cadena se inician automáticamente en el \_ \_ Estado común de los recursos de D3D12 \_ .

Antes de que un montón pueda ser el destino de una operación de copia de GPU, normalmente primero se debe pasar el montón al \_ Estado de destino de copia de estado de recurso D3D12 \_ \_ \_ . Sin embargo, los recursos creados en montones de carga deben comenzar en y no pueden cambiar desde el \_ Estado de lectura genérico, ya que solo la CPU va a escribir. Por el contrario, los recursos confirmados creados en montones de READBACK deben comenzar en y no pueden cambiar desde el estado de destino de la copia \_ .

### <a name="readwrite-resource-state-restrictions"></a>Restricciones de estado de recursos de lectura/escritura

Los bits de uso de estado de recursos que se usan para describir un estado de recurso se dividen en Estados de solo lectura y de lectura y escritura. El tema de referencia para [**los \_ \_ Estados**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) de los recursos de D3D12 indica el nivel de acceso de lectura y escritura para cada bit de la enumeración.

Como máximo, solo se puede establecer un bit de lectura/escritura para cualquier recurso. Si se establece un bit de escritura, no se puede establecer ningún bit de solo lectura para ese recurso. Si no se establece ningún bit de escritura, se puede establecer cualquier número de bits de lectura.

### <a name="resource-states-for-presenting-back-buffers"></a>Estados de los recursos para la presentación de búferes de reserva

Antes de que se presente un búfer de reserva, debe estar en \_ el \_ Estado común de los recursos de D3D12 \_ . Tenga en cuenta que el estado del recurso D3D12 de estado del recurso \_ \_ \_ es un sinónimo del \_ Estado del recurso D3D12 \_ \_ común y ambos tienen un valor de 0. Si se llama a [**IDXGISwapChain::P reenviar**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (o [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) en un recurso que actualmente no está en este estado, se emite una advertencia de nivel de depuración.

### <a name="discarding-resources"></a>Descartar recursos

Todos los Subrecursos de un recurso deben estar en el \_ Estado de destino de representación, o \_ Estado de escritura de profundidad, para los destinos de representación y los recursos de la galería de símbolos de profundidad, cuando se llama a [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) .

## <a name="implicit-state-transitions"></a>Transiciones de estado IMPLÍCITAS

Los recursos solo se pueden "promover" fuera del estado de los recursos de D3D12 \_ \_ \_ común. Del mismo modo, los recursos solo determinarán el estado de los recursos de D3D12 \_ \_ \_ común.

### <a name="common-state-promotion"></a>Promoción de Estado común

Todos los recursos de búfer y las texturas con la \_ marca de recurso D3D12 \_ \_ permiten que el \_ \_ conjunto de marcadores de acceso simultáneos se promuevan implícitamente del \_ Estado de los recursos de D3D12 \_ \_ común al estado relevante en el primer acceso de la GPU, incluida la \_ lectura genérica para cubrir cualquier escenario de lectura. Se puede tener acceso a cualquier recurso del Estado común tal y como se encontraba en un solo Estado con

<dl> 1 marca de escritura, o  
1 o más marcas de lectura  
</dl>

Los recursos se pueden promocionar desde el Estado común en función de la tabla siguiente:



| Marca de estado                    | Estado promocionable                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | **Búferes y texturas de Simultaneous-Access** | **Texturas de acceso no simultáneo** |
| \_búfer de vértices y \_ constantes \_ | Sí                                          | No                                   |
| búfer de índice \_                 | Sí                                          | No                                   |
| destino de representación \_                | Sí                                          | No                                   |
| acceso desordenado \_             | Sí                                          | No                                   |
| escritura de profundidad \_                  | No<sup>\*</sup>                              | No                                   |
| lectura de profundidad \_                   | No<sup>\*</sup>                              | No                                   |
| \_recurso de \_ sombreador sin píxeles \_  | Sí                                          | Sí                                  |
| \_recurso de sombreador de píxeles \_       | Sí                                          | Sí                                  |
| transmisión \_ por secuencias                   | Sí                                          | No                                   |
| argumento indirecto \_            | Sí                                          | No                                   |
| COPIAR \_ dest                    | Sí                                          | Sí                                  |
| COPIAR \_ origen                  | Sí                                          | Sí                                  |
| RESOLVER \_ dest                 | Sí                                          | No                                   |
| RESOLVER \_ origen               | Sí                                          | No                                   |
| PREDICATION                   | Sí                                          | No                                   |



 

<sup>\*</sup>Los recursos de la galería de símbolos de profundidad deben ser texturas de acceso no simultáneo y, por tanto, nunca se pueden promocionar implícitamente.

Cuando se produce este acceso, la promoción actúa como una barrera de recursos implícita. En el caso de los accesos posteriores, se requerirán barreras de recursos para cambiar el estado del recurso si es necesario. Tenga en cuenta que la promoción de un estado de lectura promocionado a varios Estados de lectura es válida, pero no es el caso de los Estados de escritura.  
Por ejemplo, si un recurso del Estado común se promueve al recurso de \_ sombreador \_ de píxeles en una llamada a Draw, todavía se puede promover a NON_PIXEL \_ recurso de sombreador \_ | \_ \_ Recurso de sombreador de píxeles en otra llamada a Draw. Sin embargo, si se usa en una operación de escritura, como un destino de copia, una barrera de transición de estado de recursos de los Estados de lectura promovidos combinados, aquí NON_PIXEL \_ recurso de sombreador \_ | \_Recurso de sombreador de píxeles \_ , \_ se necesita copiar el destino.  
Del mismo modo, si se promovió de común a COPY \_ dest, todavía se requiere una barrera para realizar la transición de la copia de \_ destino al destino de representación \_ .

Tenga en cuenta que la promoción de Estado común es "gratis", ya que no es necesario que la GPU realice ninguna espera de sincronización. La promoción representa el hecho de que los recursos del Estado común no deben requerir ningún trabajo de GPU adicional ni seguimiento de controladores para admitir determinados accesos.

### <a name="state-decay-to-common"></a>Caída del estado a común

El volteo de la promoción de Estado común es la decadencia en el estado del recurso de D3D12 \_ \_ \_ común. Los recursos que cumplen determinados requisitos se consideran sin estado y, de hecho, vuelven al Estado común cuando la GPU finaliza la ejecución de una operación de [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) . No se produce la caída entre las listas de comandos que se ejecutan juntas en la misma llamada **ExecuteCommandLists** .

Los siguientes recursos determinarán cuando se complete una operación [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la GPU:

-   Recursos a los que se tiene acceso en una cola de copia, *o*
-   Recursos de búfer en cualquier tipo de cola, *o*
-   Los recursos de textura en cualquier tipo de cola que tienen la \_ marca de recurso D3D12 permiten el marcador de \_ \_ \_ \_ acceso simultáneo establecido, *o bien*
-   Cualquier recurso promovido implícitamente a un estado de solo lectura.

Al igual que la promoción de Estado común, la caída es gratuita porque no se necesita ninguna sincronización adicional. La combinación de la promoción de Estado común y la caída puede ayudar a eliminar muchas transiciones de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) innecesarias. En algunos casos, esto puede proporcionar mejoras significativas en el rendimiento.

Los búferes y los recursos de Simultaneous-Access se determinarán en el Estado común, independientemente de si se han transferido explícitamente mediante barreras de recursos o se han promocionado implícitamente.

### <a name="performance-implications"></a>Implicaciones de rendimiento

Al grabar transiciones de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas en los recursos en el Estado común, es correcto usar el \_ Estado de recurso D3D12 \_ \_ común o cualquier estado promocionable como valor *BeforeState* en la estructura de la barrera de transición de recursos de D3D12 \_ \_ \_ . Esto permite la administración de estado tradicional que omite la caída automática de los búferes y las texturas de acceso simultáneo. Sin embargo, esto puede no ser conveniente, ya que evitar las llamadas de transición **ResourceBarrier** con los recursos que se sabe que están en el Estado común puede mejorar significativamente el rendimiento. Las barreras de recursos pueden ser costosas. Están diseñados para forzar vaciados de caché, cambios de diseño de memoria y otra sincronización que puede que no sean necesarios para los recursos que ya están en el Estado común. Una lista de comandos que usa una barrera de recursos de un estado no común a otro Estado no común en un recurso que se encuentra actualmente en estado común puede introducir una sobrecarga innecesaria.

Además, evite las transiciones de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas al \_ Estado de los recursos de D3D12 \_ \_ común a menos que sea absolutamente necesario (por ejemplo, el siguiente acceso se encuentra en una cola de comandos de copia que requiere que los recursos comiencen en el Estado común). Las transiciones excesivas al Estado común pueden reducir drásticamente el rendimiento de la GPU.

En Resumen, intente basarse en la promoción de Estado común y en la decadencia siempre que su semántica le permita salir sin emitir llamadas a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .

## <a name="split-barriers"></a>Barreras divididas

Una barrera de transición de recursos con la marca de la barrera de recurso de D3D12 \_ \_ \_ \_ \_ solo comienza una barrera de división y se dice que la barrera de transición está pendiente. Mientras la barrera está pendiente, la GPU no puede leer ni escribir el recurso (sub). La única barrera de transición válida que se puede aplicar a un recurso (sub) con una barrera pendiente es la misma con los mismos Estados *antes* y *después* y la marca de fin de la marca de barrera de los recursos de D3D12 \_ , la \_ \_ \_ \_ barrera que completa la transición pendiente.

Las barreras divididas proporcionan sugerencias a la GPU de que un recurso en *el estado a* se usará a continuación en el estado *B* posteriormente. Esto proporciona a la GPU la opción de optimizar la carga de trabajo de transición, lo que podría reducir o eliminar las paradas de ejecución. La emisión de la barrera solo final garantiza que todo el trabajo de transición de la GPU finalice antes de pasar al siguiente comando.

El uso de barreras divididas puede ayudar a mejorar el rendimiento, especialmente en escenarios con varios motores o en los que los recursos se transfieran de forma dispersa en una o varias listas de comandos.

## <a name="resource-barrier-example-scenario"></a>Escenario de ejemplo de barrera de recursos

En los fragmentos de código siguientes se muestra el uso del método [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) en un ejemplo de subprocesamiento múltiple.

Crear la vista de galería de símbolos de profundidad, en la que se realiza la transición a un estado grabable.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Crear la vista de búfer de vértices y cambiarla primero de un Estado común a un destino y, a continuación, de un destino a un estado legible genérico.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Crear la vista del búfer de índice, cambiando primero de un Estado común a un destino y, a continuación, de un destino a un estado legible genérico.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Creación de texturas y vistas de recursos de sombreador. La textura se cambia de un Estado común a un destino y, a continuación, de un destino a un recurso de sombreador de píxeles.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Inicio de un fotograma; Esto no solo usa [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para indicar que el búfer de reserva se va a usar como destino de representación, sino que también inicializa el recurso de marco (que llama a **ResourceBarrier** en el búfer de estarcido de profundidad).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Finalización de un fotograma, que indica que el búfer de reserva ahora se usa para presentar.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



Al inicializar un recurso de marco, llamado al iniciar un fotograma, se pasa el búfer de estarcido de profundidad a grabable.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



Las barreras se intercambian de trama intermedia y se realiza la transición de la asignación de instantáneas de escritura a legible.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Se llama a Finish cuando finaliza un fotograma, pasando el mapa de instantáneas a un Estado común.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Ejemplo de promoción de Estado común y decadencia

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Ejemplo de barreras divididas

En el ejemplo siguiente se muestra cómo usar una barrera dividida para reducir las paradas de canalización. El código que sigue no utiliza barreras divididas:

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

En el código siguiente se usan barreras divididas:

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Temas relacionados

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: barreras de recursos y seguimiento de estado](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Sincronización de varios motores](./user-mode-heap-synchronization.md)

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)

[Una mirada dentro de las barreras de estado de los recursos de D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

