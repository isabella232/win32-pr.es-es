---
title: Uso de barreras de recursos para sincronizar los estados de los recursos en Direct3D 12
description: Para reducir el uso general de LA CPU y habilitar el procesamiento previo y multiproceso de controladores, Direct3D 12 traslada la responsabilidad de la administración del estado por recurso del controlador de gráficos a la aplicación.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f79d5463c2f27560049f785b5cc32fe42ae33927cba7d039b90638f3946531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989435"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Uso de barreras de recursos para sincronizar los estados de los recursos en Direct3D 12

Para reducir el uso general de LA CPU y habilitar el procesamiento previo y multiproceso de controladores, Direct3D 12 traslada la responsabilidad de la administración del estado por recurso del controlador de gráficos a la aplicación. Un ejemplo de estado por recurso es si actualmente se tiene acceso a un recurso de textura como a través de un objeto Shader Vista de recursos o como una vista de destino de representación. En Direct3D 11, los controladores tenían que realizar un seguimiento de este estado en segundo plano. Esto es costoso desde la perspectiva de la CPU y complica significativamente cualquier tipo de diseño multiproceso. En Microsoft Direct3D 12, la mayoría del estado por recurso se administra mediante la aplicación con una sola API, [**ID3D12GraphicsCommandList::ResourceBartero**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

-   [Uso de ResourceBar php API para administrar el estado por recurso](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Estados de recursos](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Estados iniciales de los recursos](#initial-states-for-resources)
    -   [Restricciones de estado de recursos de lectura y escritura](#readwrite-resource-state-restrictions)
    -   [Estados de recursos para presentar búferes de reserva](#resource-states-for-presenting-back-buffers)
    -   [Descarte de recursos](#discarding-resources)
-   [Transiciones de estado implícitas](#implicit-state-transitions)
    -   [Promoción de estado común](#common-state-promotion)
    -   [Decadencia del estado a común](#state-decay-to-common)
    -   [Implicaciones de rendimiento](#performance-implications)
-   [Barreras divididas](#split-barriers)
-   [Escenario de ejemplo de barrera de recursos](#resource-barrier-example-scenario)
-   [Ejemplo común de promoción de estado y decadencia](#common-state-promotion-and-decay-sample)
-   [Ejemplo de barreras divididas](#example-of-split-barriers)
-   [Temas relacionados](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Uso de la API ResourceBar php para administrar el estado por recurso

[**ResourceBar odbc notifica**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) al controlador de gráficos las situaciones en las que el controlador puede necesitar sincronizar varios accesos a la memoria en la que se almacena un recurso. Se llama al método con una o varias estructuras de descripción de barrera de recursos que indican el tipo de barrera de recursos que se declara.

Hay tres tipos de barreras de recursos:

-   **Barrera de transición:** una barrera de transición indica que un conjunto de subrecursos pasa entre distintos usos. Se [**usa una estructura D3D12 \_ RESOURCE TRANSITION \_ \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) para especificar el subrecurso que está en transición, así como los estados *antes* y después del subrecurso. 

    El sistema comprueba que las transiciones de subrecursos de una lista de comandos son coherentes con las transiciones anteriores en la misma lista de comandos. La capa de depuración realiza un seguimiento adicional del estado del subrecurso para encontrar otros errores, pero esta validación es conservadora y no exhaustiva.

    Tenga en cuenta que puede usar la marca D3D12 RESOURCE BARRIER ALL SUBRESOURCES para especificar que todos los \_ subrecursos dentro de un recurso se están \_ \_ \_ transicional.

-   **Barrera de alias:** una barrera de alias indica una transición entre los usos de dos recursos diferentes que tienen asignaciones superpuestas en el mismo montón. Esto se aplica a los recursos reservados y colocados. Se [**usa una estructura D3D12 RESOURCE \_ \_ ALIASING \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) para especificar el recurso *anterior* y el *recurso* posterior.

    Tenga en cuenta que uno o ambos recursos pueden ser NULL, lo que indica que cualquier recurso en mosaico podría provocar alias. Para obtener más información sobre el uso de recursos en mosaico, vea [Recursos en mosaico y](../direct3d11/tiled-resources.md) Recursos en mosaico por [volumen.](volume-tiled-resources.md)

-   Barrera de vista de acceso no ordenado **(UAV):** una barrera UAV indica que todos los accesos UAV, tanto de lectura como de escritura, a un recurso determinado deben completarse entre cualquier acceso UAV futuro, tanto de lectura como de escritura. No es necesario que una aplicación coloque una barrera UAV entre dos llamadas a draw o dispatch que solo se leen desde un UAV. Además, no es necesario colocar una barrera UAV entre dos llamadas a draw o dispatch que escriben en el mismo UAV si la aplicación sabe que es seguro ejecutar el acceso UAV en cualquier orden. Se [**usa una estructura D3D12 RESOURCE \_ \_ UAV \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) para especificar el recurso UAV al que se aplica la barrera. La aplicación puede especificar NULL para el UAV de la barrera, lo que indica que cualquier acceso UAV podría requerir la barrera.

Cuando se llama a [**ResourceBartero**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) con una matriz de descripciones de barrera de recursos, la API se comporta como si se llamara una vez para cada elemento, en el orden en que se proporcionaron.

En un momento dado, un subrecurso se encuentra exactamente en un estado, determinado por el conjunto de marcas [**\_ RESOURCE \_ STATES de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) proporcionadas a [**ResourceBarander**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier). La aplicación debe asegurarse de que los *estados antes* y *después* de las llamadas consecutivas a **ResourceBarlda están de acuerdo.**

> [!TIP]
>
> Las aplicaciones deben procesar por lotes varias transiciones en una llamada API siempre que sea posible.

 

### <a name="resource-states"></a>Estados de recursos

Para obtener la lista completa de estados de recursos entre los que un recurso puede realizar la transición, consulte el tema de referencia de la [**enumeración \_ RESOURCE STATES \_ de D3D12.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)

Para las barreras de recursos divididos, consulte también [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Estados iniciales de los recursos

Los recursos se pueden crear con cualquier estado inicial especificado por el usuario (válido para la descripción del recurso), con las siguientes excepciones:

-   Upload montones deben comenzar en el estado D3D12 RESOURCE STATE GENERIC READ, que es \_ una combinación OR bit a bit \_ \_ \_ de:
    -   VÉRTICE DE ESTADO DE RECURSO D3D12 \_ \_ Y BÚFER \_ \_ \_ \_ CONSTANTE
    -   BÚFER DE ÍNDICE DE ESTADO DE RECURSO D3D12 \_ \_ \_ \_
    -   ORIGEN DE COPIA DEL ESTADO DEL RECURSO D3D12 \_ \_ \_ \_
    -   RECURSO DE SOMBREADOR \_ DE PÍXELES DE ESTADO \_ DE RECURSO \_ \_ \_ \_ D3D12
    -   RECURSO SOMBREADOR DE \_ PÍXELES DE ESTADO DE RECURSO D3D12 \_ \_ \_ \_
    -   ARGUMENTO INDIRECTO DE ESTADO DE RECURSO D3D12 \_ \_ \_ \_
-   Los montones de readback deben iniciarse en el estado D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST.
-   Los búferes de reserva de cadena de intercambio se inician automáticamente en el estado RESOURCE STATE COMMON de D3D12. \_ \_ \_

Antes de que un montón pueda ser el destino de una operación de copia de GPU, normalmente el montón debe pasar primero al estado D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST. Sin embargo, los recursos creados en los montones de carga deben iniciarse en y no pueden cambiar desde el estado DE LECTURA GENÉRICA, ya que solo la \_ CPU realizará la escritura. Por el contrario, los recursos confirmados creados en montones READBACK deben iniciarse en y no pueden cambiar desde el estado COPY \_ DEST.

### <a name="readwrite-resource-state-restrictions"></a>Restricciones de estado de recursos de lectura y escritura

Los bits de uso del estado de recurso que se usan para describir un estado de recurso se dividen en estados de solo lectura y de lectura y escritura. El tema de referencia para [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica el nivel de acceso de lectura y escritura para cada bit de la enumeración.

Como máximo, solo se puede establecer un bit de lectura y escritura para cualquier recurso. Si se establece un bit de escritura, no se puede establecer ningún bit de solo lectura para ese recurso. Si no se establece ningún bit de escritura, se puede establecer cualquier número de bits de lectura.

### <a name="resource-states-for-presenting-back-buffers"></a>Estados de recursos para presentar búferes de reserva

Antes de que se presente un búfer de reserva, debe estar en el estado D3D12 \_ RESOURCE \_ STATE \_ COMMON. Tenga en cuenta que el estado de recurso D3D12 RESOURCE STATE PRESENT es un sinónimo de \_ \_ \_ D3D12 RESOURCE STATE COMMON y ambos tienen \_ un valor de \_ \_ 0. Si se llama a [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (o [**IDXGISwapChain1::P resent1)**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)en un recurso que no está actualmente en este estado, se emite una advertencia de capa de depuración.

### <a name="discarding-resources"></a>Descarte de recursos

Todos los subrecursos de un recurso deben estar en el estado RENDER TARGET o DEPTH WRITE para los destinos de representación y los recursos de galería de símbolos de profundidad, respectivamente, cuando se llama a \_ \_ [**ID3D12GraphicsCommandList::D iscardResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)

## <a name="implicit-state-transitions"></a>Transiciones de estado implícitas

Los recursos solo se pueden "promover" fuera de D3D12 \_ RESOURCE \_ STATE \_ COMMON. Del mismo modo, los recursos solo se "degradarán" a D3D12 \_ RESOURCE \_ STATE \_ COMMON.

### <a name="common-state-promotion"></a>Promoción de estado común

Todos los recursos de búfer, así como las texturas con el conjunto de marcas D3D12 RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS, se promueven implícitamente de \_ \_ \_ \_ \_ D3D12 \_ RESOURCE STATE \_ \_ COMMON \_ al estado pertinente en el primer acceso de GPU, incluida LA LECTURA GENÉRICA para cubrir cualquier escenario de lectura. Se puede acceder a cualquier recurso en el estado COMMON como a través de él en un solo estado con

<dl> 1 Marca WRITE o  
1 o más marcas READ  
</dl>

Los recursos se pueden promover desde el estado COMMON en función de la tabla siguiente:



| Marca de estado                    | Búferes y Simultaneous-Access texturas                             | Texturas de acceso no simultáneo                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| VÉRTICE \_ Y \_ BÚFER \_ CONSTANTE | Sí                                          | No                                   |
| BÚFER DE \_ ÍNDICE                 | Sí                                          | No                                   |
| DESTINO DE \_ REPRESENTACIÓN                | Sí                                          | No                                   |
| ACCESO \_ DESORDENADO             | Sí                                          | No                                   |
| ESCRITURA EN \_ PROFUNDIDAD                  | No<sup>\*</sup>                              | No                                   |
| LECTURA DE \_ PROFUNDIDAD                   | No<sup>\*</sup>                              | No                                   |
| RECURSO QUE \_ NO ES \_ \_ SOMBREADOR DE PÍXELES  | Sí                                          | Sí                                  |
| RECURSO \_ SOMBREADOR DE \_ PÍXELES       | Sí                                          | Sí                                  |
| STREAM \_ OUT                   | Sí                                          | No                                   |
| ARGUMENTO \_ INDIRECTO            | Sí                                          | No                                   |
| COPY \_ DEST                    | Sí                                          | Sí                                  |
| ORIGEN DE \_ COPIA                  | Sí                                          | Sí                                  |
| RESOLVE \_ DEST                 | Sí                                          | No                                   |
| RESOLVER \_ ORIGEN               | Sí                                          | No                                   |
| Predicación                   | Sí                                          | No                                   |



 

<sup>\*</sup>Los recursos de galería de símbolos de profundidad deben ser texturas de acceso no simultáneo y, por tanto, nunca se pueden promover implícitamente.

Cuando se produce este acceso, la promoción actúa como una barrera implícita de recursos. Para los accesos posteriores, se requieren barreras de recursos para cambiar el estado del recurso si es necesario. Tenga en cuenta que la promoción de un estado de lectura promocionado a varios estados de lectura es válida, pero este no es el caso de los estados de escritura.  
Por ejemplo, si un recurso en estado común se promueve a PIXEL SHADER RESOURCE en una llamada a Draw, todavía se puede promover a NON_PIXEL \_ \_ RECURSO SHADER \_ \_ | RECURSO \_ \_ SOMBREADOR DE PÍXELES en otra llamada a Draw. Sin embargo, si se usa en una operación de escritura, como un destino de copia, una barrera de transición de estado de recurso de los estados de lectura promocionados combinados, NON_PIXEL \_ SHADER \_ RESOURCE | RECURSO \_ \_ SOMBREADOR DE PÍXELES, para \_ COPIAR DEST es necesario.  
Del mismo modo, si se promueve de COMMON a COPY DEST, todavía se necesita una barrera para realizar la transición de \_ COPY \_ DEST a RENDER \_ TARGET.

Tenga en cuenta que la promoción de estado común es "gratuita", ya que no es necesario que la GPU realice esperas de sincronización. La promoción representa el hecho de que los recursos en el estado COMMON no deben requerir trabajo adicional de GPU ni seguimiento de controladores para admitir determinados accesos.

### <a name="state-decay-to-common"></a>Decadencia del estado a común

El otro lado de la promoción de estado común es volver a decadencia a D3D12 \_ RESOURCE \_ STATE \_ COMMON. Los recursos que cumplen determinados requisitos se consideran sin estado y vuelven eficazmente al estado común cuando la GPU finaliza la ejecución de una [**operación ExecuteCommandLists.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) La decadencia no se produce entre las listas de comandos ejecutadas juntas en la misma **llamada ExecuteCommandLists.**

Los siguientes recursos se decaerán cuando se complete una operación [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la GPU:

-   Recursos a los que se accede en una cola de copia *o*
-   Recursos de búfer en cualquier tipo de cola *o*
-   Recursos de textura en cualquier tipo de cola que tenga establecida la marca DE RECURSOS D3D12 \_ \_ ALLOW SIMULTANEOUS ACCESS \_ \_ \_ o 
-   Cualquier recurso promovido implícitamente a un estado de solo lectura.

Al igual que la promoción de estado común, la decadencia es libre en el sentido de que no se necesita ninguna sincronización adicional. Combinar la promoción de estado común y la decadencia puede ayudar a eliminar muchas transiciones [**innecesarias de ResourceBarcomposición.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) En algunos casos, esto puede proporcionar mejoras de rendimiento significativas.

Los búferes y Simultaneous-Access recursos se degradarán al estado común, independientemente de si se han pasado explícitamente mediante barreras de recursos o se han promocionado implícitamente.

### <a name="performance-implications"></a>Implicaciones de rendimiento

Al registrar transiciones [**de ResourceBargida**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas en recursos en el estado común, es correcto usar D3D12 RESOURCE STATE COMMON o cualquier estado promocionable como valor BeforeState en la estructura \_ \_ \_ D3D12  RESOURCE TRANSITION \_ \_ \_ BARRIER. Esto permite la administración de estado tradicional que omite la decadencia automática de búferes y texturas de acceso simultáneo. Sin embargo, esto puede no ser deseable, ya que evitar la transición de llamadas **ResourceBartero** con recursos que se sabe que están en el estado común puede mejorar significativamente el rendimiento. Las barreras de recursos pueden ser costosas. Están diseñados para forzar vaciados de caché, cambios de diseño de memoria y otra sincronización que pueden no ser necesarias para los recursos que ya están en el estado común. Una lista de comandos que usa una barrera de recursos de un estado no común a otro estado no común en un recurso actualmente en el estado común puede introducir una gran sobrecarga innecesario.

Además, evite las transiciones explícitas de [**ResourceBar begin**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) a D3D12 RESOURCE STATE COMMON a menos que sea absolutamente necesario (por ejemplo, el siguiente acceso se encuentra en una cola de comandos COPY que requiere que los recursos comiencen en el estado \_ \_ \_ común). Las transiciones excesivas al estado común pueden ralentizar considerablemente el rendimiento de la GPU.

En resumen, intente confiar en la promoción de estado común y la decadencia cada vez que su semántica le permita salir sin emitir [**llamadas ResourceBarcomposición.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

## <a name="split-barriers"></a>Barreras divididas

Una barrera de transición de recursos con la marca D3D12 RESOURCE BARRIER FLAG BEGIN ONLY comienza una barrera de división y se dice que la barrera de transición \_ \_ está \_ \_ \_ pendiente. Mientras la barrera está pendiente, la GPU no puede leer ni escribir el recurso (sub) . La única barrera de transición legal que se puede aplicar a un  (sub)recurso con una barrera pendiente es una con los mismos estados antes y después y la marca D3D12 RESOURCE BARRIER FLAG END ONLY, que completa la transición  \_ \_ \_ \_ \_ pendiente.

Las barreras divididas proporcionan sugerencias a la GPU de que un recurso en el estado *A* se usará a continuación en el *estado B* más adelante. Esto ofrece a la GPU la opción de optimizar la carga de trabajo de transición, lo que posiblemente reduzca o elimine los puestos de ejecución. La emisión de la barrera de solo fin garantiza que todo el trabajo de transición de GPU haya finalizado antes de pasar al siguiente comando.

El uso de barreras divididas puede ayudar a mejorar el rendimiento, especialmente en escenarios de varios motores o en los que los recursos se transiciónn de lectura y escritura dispersamente en una o varias listas de comandos.

## <a name="resource-barrier-example-scenario"></a>Escenario de ejemplo de barrera de recursos

Los fragmentos de código siguientes muestran el uso del [**método ResourceBarproceso**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) en un ejemplo de varios subprocesos.

Crear la vista de galería de símbolos de profundidad y pasarla a un estado que se puede escribir.


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



Crear la vista de búfer de vértices, cambiarla primero de un estado común a un destino y, a continuación, de un destino a un estado legible genérico.


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



Crear la vista de búfer de índice, cambiarla primero de un estado común a un destino y, a continuación, de un destino a un estado legible genérico.


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



Crear texturas y vistas de recursos de sombreador. La textura cambia de un estado común a un destino y, a continuación, de un destino a un recurso de sombreador de píxeles.


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



Inicio de un marco; Esto no solo usa [**ResourceBarbuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para indicar que el búfer de reserva se va a usar como destino de representación, sino que también inicializa el recurso de marco (que llama a **ResourceBarbuffer** en el búfer de la galería de símbolos de profundidad).


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



Finalizando un marco, lo que indica que el búfer de reserva ahora se usa para presentarse.


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



Al inicializar un recurso de marco, al que se llama al comenzar un fotograma, se pasa el búfer de la galería de símbolos de profundidad a que se puede escribir.


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



Las barreras se intercambian a mitad del marco, lo que hace que el mapa de sombras se cambie de fácil de escribir a legible.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Se llama a Finish cuando finaliza un marco, con lo que se pasa el mapa de sombras a un estado común.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Ejemplo común de promoción de estado y decadencia

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

En el ejemplo siguiente se muestra cómo usar una barrera de división para reducir los puestos de canalización. El código siguiente no usa barreras divididas:

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

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: Barreras de recursos y seguimiento de estado](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Sincronización de varios motores](./user-mode-heap-synchronization.md)

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)

[Una mirada dentro de las barreras de estado de recursos D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

