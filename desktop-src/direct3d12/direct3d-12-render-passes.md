---
title: Fases de representación de Direct3D 12
description: La característica de pasos de representación ayuda al representador a mejorar la eficacia de la GPU al reducir el tráfico de memoria hacia y desde la memoria fuera del chip; para ello, permite a la aplicación identificar mejor los requisitos de orden de representación de recursos y las dependencias de datos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: f776729f17ac0017d713c6f37bc71de7302a7c08
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/26/2020
ms.locfileid: "104549067"
---
# <a name="direct3d-12-render-passes"></a>Fases de representación de Direct3D 12

La característica de pasos de representación es nueva para Windows 10, versión 1809 (10,0; Compilación 17763) e introduce el concepto de una fase de representación de Direct3D 12. Una fase de representación consta de un subconjunto de los comandos que se registran en una lista de comandos.

Para declarar dónde comienza y finaliza cada paso de representación, se anidan los comandos que pertenecen a ese paso dentro de las llamadas a [**ID3D12GraphicsCommandList4:: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) y [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Por lo tanto, cualquier lista de comandos contiene cero, una o más fases de representación.

## <a name="scenarios"></a>Escenarios

Las pasadas de representación pueden mejorar el rendimiento del representador si se basa en Tile-Based representación diferida (TBDR), entre otras técnicas. Más concretamente, la técnica ayuda al representador a mejorar la eficacia de la GPU al reducir el tráfico de memoria hacia y desde la memoria fuera del chip al permitir a la aplicación identificar mejor los requisitos de orden de representación de recursos y las dependencias de datos.

Un controlador de pantalla escrito expresamente para aprovechar la característica de pasos de representación proporciona los mejores resultados. Pero las API de las pasadas de representación pueden ejecutarse incluso en controladores preexistentes (aunque no necesariamente con mejoras de rendimiento).

Estos son los escenarios en los que las fases de representación están diseñadas para proporcionar valor.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Permitir a la aplicación evitar cargas y almacenes innecesarios de recursos de/a la memoria principal en una Tile-Based arquitectura de representación diferida (TBDR)

Una de las propuestas de valor de las fases de representación es que proporciona una ubicación central para indicar las dependencias de datos de la aplicación para un conjunto de operaciones de representación. Estas dependencias de datos permiten al controlador de pantalla inspeccionar estos datos en el momento del enlace o la barrera y emitir instrucciones que minimizan las cargas y almacenes de recursos de/a la memoria principal.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Permita que la arquitectura de TBDR de los recursos persistentes en la memoria caché en chip a través de las fases de representación (incluso en listas de comandos independientes)

> [!NOTE]
> En concreto, este escenario se limita a los casos en los que se escribe en los mismos destinos de representación en varias listas de comandos.

Un patrón de representación común es que la aplicación se represente en los mismos destinos de representación en varias listas de comandos en serie, aunque los comandos de representación se generen en paralelo. El uso de pasos de representación en este escenario permite que estas pasadas se combinen de este modo (dado que la aplicación sabe que se reanudará la representación en la lista de comandos correcta inmediata) que el controlador de pantalla puede evitar un vaciado en la memoria principal en los límites de la lista de comandos.

## <a name="your-applications-responsibilities"></a>Responsabilidades de la aplicación

Incluso con la característica de pasos de representación, ni el motor en tiempo de ejecución de Direct3D 12 ni el controlador de pantalla asumen la responsabilidad de deducir oportunidades de reordenar o evitar cargas y almacenes. Para aprovechar correctamente la característica de pasadas de representación, la aplicación tiene estas responsabilidades.

- Identifique correctamente las dependencias de datos y ordenación para sus operaciones.
- Ordene los envíos de forma que se minimicen los vaciados (por lo tanto, minimice el uso de las marcas de **_PRESERVE** ).
- Usar correctamente las barreras de recursos y realizar un seguimiento del estado de los recursos.
- Evite copias o borraciones innecesarias. Para ayudar a identificarlos, puede hacer uso de las advertencias de rendimiento automatizadas de la [herramienta PIX en Windows](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Usar la característica de paso de representación

### <a name="what-is-a-render-pass"></a>¿Qué es una *fase de representación*?

Estos elementos definen una fase de representación.

- Un conjunto de enlaces de salida que son fijos para la duración de la fase de representación. Estos enlaces son a una o varias vistas de destino de representación (RTVs) o a una vista de galería de símbolos de profundidad (DSV).
- Una lista de las operaciones de GPU que tienen como destino ese conjunto de enlaces de salida.
- Metadatos que describen las dependencias de carga y almacenamiento de todos los enlaces de salida de destino de la fase de representación.

### <a name="declare-your-output-bindings"></a>Declarar los enlaces de salida

Al principio de una fase de representación, se declaran enlaces a los destinos de representación y/o al búfer de profundidad/estarcido. Es opcional enlazar a destinos de representación y es opcional enlazar a un búfer de profundidad/estarcido. Pero debe enlazar al menos a uno de los dos, y en el ejemplo de código siguiente enlazamos a ambos.

Estos enlaces se declaran en una llamada a [**ID3D12GraphicsCommandList4:: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

El primer campo de la estructura de [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) se establece en el identificador del descriptor de la CPU correspondiente a una o varias vistas de destino de representación (RTVs). Del mismo modo, [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) contiene el identificador de descriptor de la CPU correspondiente a una vista de galería de símbolos de profundidad (DSV). Esos identificadores de descriptor de CPU son los mismos que, de otro modo, pasaría a [**ID3D12GraphicsCommandList:: OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets). Y, al igual que con **OMSetRenderTargets**, los descriptores de CPU se *ajustan* desde sus montones de (descriptor de CPU) respectivos en el momento de la llamada a **BeginRenderPass**.

RTVs y DSV no se heredan en la fase de representación. En su lugar, se deben establecer. Ni los RTVs y DSV declarados en **BeginRenderPass** propagados a la lista de comandos. En su lugar, se encuentran en un estado indefinido después de la fase de representación.

### <a name="render-passes-and-workloads"></a>Representación de pasadas y cargas de trabajo

No se pueden anidar las fases de representación y no se puede tener una fase de representación a la vez de más de una lista de comandos (deben comenzar y finalizar mientras se graba en una sola lista de comandos). Las optimizaciones diseñadas para habilitar la generación eficaz multiproceso de las fases de representación se describen en la sección [ indicadores de paso de representación](#render-pass-flags), más abajo.

Una escritura que se realiza desde una fase de representación no es *válida* para que se pueda leer hasta una fase de representación posterior. Esto impide algunos tipos de barreras desde dentro del paso de representación &mdash; , por ejemplo, la barrera de **RENDER_TARGET** a **SHADER_RESOURCE** en el destino de presentación enlazado actualmente. Para obtener más información, vea la sección [fases de representación y barreras de recursos](#render-passes-and-resource-barriers), a continuación.

La única excepción a la restricción de lectura/escritura que se acaba de mencionar implica las lecturas implícitas que se producen como parte de las pruebas de profundidad y de la mezcla de destino de representación.
Por lo tanto, estas API no se permiten en una fase de representación (el tiempo de ejecución principal quita la lista de comandos si se llama a cualquiera de ellas durante la grabación).

- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList::ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList::ClearState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList::D iscardResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Fases de representación y barreras de recursos

No se puede leer, o consumir, una escritura que se produjo dentro de la misma fase de representación. Ciertas barreras no se ajustan a esta restricción, por ejemplo, desde **D3D12_RESOURCE_STATE_RENDER_TARGET** a **\* _SHADER_RESOURCE** en el destino de presentación enlazado actualmente (y la capa de depuración producirá un error en ese efecto). Sin embargo, esa misma barrera en un destino de representación que se escribió *fuera* de la fase de representación actual es compatible, ya que las escrituras se completarán antes del inicio del paso de representación actual.
Es posible que se beneficie de conocer algunas optimizaciones que un controlador de pantalla puede tomar en este sentido. Dada una carga de trabajo compatible, un controlador de pantalla puede trasladar las barreras encontradas en el paso de representación al principio de la fase de representación. Allí, se pueden fusionar mediante combinación (y no interferir con ninguna operación de mosaico o discretización). Se trata de una optimización válida siempre que todas las escrituras hayan finalizado antes de que se inicie la fase de representación actual.

A continuación se muestra un ejemplo de optimización de controladores más completo, en el que se supone que tiene un motor de representación que tiene un diseño de enlace de recursos de estilo anterior a Direct3D que &mdash; realiza barreras *a petición* en función de cómo se enlazan los recursos. Al escribir en una vista de acceso desordenado (UAV) hacia el final de un marco (que se va a consumir en el siguiente fotograma), el motor podría dejar el recurso en el estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** al concluir el marco. En el marco siguiente, cuando el motor vaya a enlazar el recurso como vista de recursos del sombreador (SRV), se descubrirá que el recurso no está en el estado correcto y emitirá una barrera de **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** a **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Si esa barrera se produce dentro de la fase de representación, el controlador de pantalla está justificado en la suposición de que ya se han producido todas las escrituras *fuera* de esta fase de representación actual y, por tanto, (y aquí es donde entra la optimización), el controlador de pantalla podría *pasar* la barrera hasta el inicio de la fase de representación. De nuevo, esto es válido, siempre que el código se ajuste a la restricción de lectura y escritura descrita en esta sección y en el último.


Estos son ejemplos de barreras conformes.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** que se va a **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** que se va a **\* _SHADER_RESOURCE**.

Y estos son ejemplos de barreras no compatibles.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** a cualquier estado de lectura en RTVs/DSV enlazado actualmente.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** a cualquier estado de lectura en RTVs/DSV enlazado actualmente.
- Cualquier barrera de alias.
- Barreras de la vista de acceso desordenado (UAV). 

### <a name="resource-access-declaration"></a>Declaración de acceso a recursos

En el momento de **BeginRenderPass** , así como declarar todos los recursos que sirven como RTVs y/o DSV dentro de ese paso, también debe especificar sus características de *acceso* inicial y final. Como puede ver en el ejemplo de código de la sección [declare Your Output bindings](#declare-your-output-bindings) anterior, lo hace con las estructuras [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) y [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) .

Para obtener más información, vea las estructuras [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) y [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) , y las enumeraciones [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) y [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) .

### <a name="render-pass-flags"></a>Mostrar marcas de paso

El último parámetro pasado a **BeginRenderPass** es una marca de paso de representación (un valor de la enumeración [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) ).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>UAV escribe dentro de una fase de representación

Las escrituras de vista de acceso desordenados (UAV) se permiten dentro de una fase de representación, pero debe indicar específicamente que va a emitir escrituras de UAV dentro de la fase de representación especificando **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES**, de modo que el controlador de pantalla pueda optar por no incluir mosaicos si es necesario.

Los accesos de UAV deben seguir la restricción de lectura y escritura descrita anteriormente (las escrituras en una fase de representación no son válidas para leer hasta un paso de representación subsiguiente). No se permiten barreras UAV en una fase de representación.

Los enlaces de UAV (a través de tablas raíz o descriptores raíz) se heredan en pasadas de representación y se propagan fuera de las fases de representación.

#### <a name="suspending-passes-and-resuming-passes"></a>Suspend-pasa y RESUMING-pasa

Puede indicar una fase de representación completa como un paso de suspensión o un paso de reanudación. Un par de suspensión seguido de reanudación debe tener marcas de acceso o vistas idénticas entre las pasadas. y es posible que no tenga ninguna operación de GPU interactiva (por ejemplo, dibuje, envíe, descarte, borre, copia, copias de actualización-mosaicos, instantáneas del búfer de escritura, consultas, resoluciones de consulta) entre la fase de resuspensión de representación y la fase de representación de reanudación.

El caso de uso previsto es la representación multiproceso, donde, por ejemplo, cuatro listas de comandos (cada una con sus propios pasos de representación) pueden tener como destino los mismos objetivos de representación. Cuando se suspenden o reanudan los pasos de representación en las listas de comandos, las listas de comandos se deben ejecutar en la misma llamada a [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Una fase de representación se puede reanudar y suspender. En el ejemplo con varios subprocesos que se acaba de proporcionar, las listas de comandos 2 y 3 se reanudarían de 1 y 2, respectivamente. Y, al mismo tiempo, 2 y 3 se suspenderían en 3 y 4, respectivamente.

## <a name="query-for-render-passes-feature-support"></a>Consulta para la compatibilidad de las características de las fases de representación

Puede llamar a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para consultar la medida en la que un controlador de dispositivo o el hardware admiten correctamente las fases de representación.

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

Debido a la lógica de asignación del tiempo de ejecución, las pasadas de representación siempre funcionan. Sin embargo, en función de la compatibilidad de las características, no siempre ofrecen una ventaja. Puede usar código similar al del ejemplo de código anterior para determinar si merece la pena su tiempo para emitir comandos como pasadas de representación, y cuando no es una ventaja, es decir, cuando el tiempo de ejecución simplemente se asigna a la superficie de API existente. La realización de esta comprobación es especialmente importante si usa [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)).

Para obtener una descripción de los tres niveles de compatibilidad, vea la enumeración [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) .
