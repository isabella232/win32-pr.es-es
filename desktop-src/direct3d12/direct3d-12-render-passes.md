---
title: Pases de representación de Direct3D 12
description: La característica de pases de representación ayuda al representador a mejorar la eficacia de GPU al reducir el tráfico de memoria hacia y desde la memoria sin chip. para ello, permite a la aplicación identificar mejor los requisitos de ordenación de la representación de recursos y las dependencias de datos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: 96ed14cecd518a3e03672f2667306ee0a4b8d64999aab01aa72aae04975f0a83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069695"
---
# <a name="direct3d-12-render-passes"></a>Pases de representación de Direct3D 12

La característica de pases de representación es nueva para Windows 10, versión 1809 (10.0; Compilación 17763) y presenta el concepto de paso de representación de Direct3D 12. Un paso de representación consta de un subconjunto de los comandos que se registran en una lista de comandos.

Para declarar dónde comienza y finaliza cada paso de representación, anida los comandos que pertenecen a ese paso dentro de las llamadas a [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) y [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Por lo tanto, cualquier lista de comandos contiene cero, uno o más pases de representación.

## <a name="scenarios"></a>Escenarios

Los pases de representación pueden mejorar el rendimiento del representador si se basa en Tile-Based Representación diferida (TBDR), entre otras técnicas. Más concretamente, la técnica ayuda al representador a mejorar la eficacia de GPU al reducir el tráfico de memoria hacia y desde la memoria sin chip al permitir que la aplicación identifique mejor los requisitos de ordenación de la representación de recursos y las dependencias de datos.

Un controlador de pantalla escrito expresamente para aprovechar la característica de pases de representación proporciona los mejores resultados. Sin embargo, las API de pases de representación se pueden ejecutar incluso en controladores ya existentes (aunque no necesariamente con mejoras de rendimiento).

Estos son los escenarios en los que los pases de representación están diseñados para proporcionar valor.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Permitir que la aplicación evite cargas o almacenes innecesarios de recursos desde y hacia la memoria principal en una arquitectura de Tile-Based de representación diferida (TBDR)

Una de las propuestas de valor de los pases de representación es que proporciona una ubicación central para indicar las dependencias de datos de la aplicación para un conjunto de operaciones de representación. Estas dependencias de datos permiten al controlador de visualización inspeccionar estos datos en tiempo de enlace o barrera, así como emitir instrucciones que minimicen las cargas o almacenes de recursos desde y hacia la memoria principal.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Permita que la arquitectura de TBDR sea oportunistamente persistente en la caché en chip a través de pases de representación (incluso en listas de comandos independientes).

> [!NOTE]
> En concreto, este escenario se limita a los casos en los que se escribe en los mismos destinos de representación en varias listas de comandos.

Un patrón de representación común es que la aplicación se represente en los mismos destinos de representación en varias listas de comandos en serie, aunque los comandos de representación se generen en paralelo. El uso de pases de representación en este escenario permite combinar estas pasadas de tal manera (dado que la aplicación sabe que reanudará la representación en la lista de comandos de ejecución inmediata) que el controlador para mostrar puede evitar un vaciado en la memoria principal en los límites de la lista de comandos.

## <a name="your-applications-responsibilities"></a>Responsabilidades de la aplicación

Incluso con la característica de paso de representación, ni el entorno de ejecución de Direct3D 12 ni el controlador de pantalla asumen la responsabilidad deduciendo oportunidades para volver a ordenar o evitar cargas y almacenes. Para aprovechar correctamente la característica de pases de representación, la aplicación tiene estas responsabilidades.

- Identifique correctamente las dependencias de ordenación y datos para sus operaciones.
- Ordene sus envíos de forma que minimice los vaciados (por lo tanto, minimice el uso de **_PRESERVE** marcas).
- Use correctamente las barreras de recursos y realice un seguimiento del estado de los recursos.
- Evite copias o borraciones innecesarios. Para ayudar a identificarlos, puede usar las advertencias de rendimiento automatizadas de [LAN en Windows herramienta](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Uso de la característica de paso de representación

### <a name="what-is-a-render-pass"></a>¿Qué es un *paso de representación?*

Estos elementos definen un paso de representación.

- Conjunto de enlaces de salida que se fijan mientras dure el paso de representación. Estos enlaces son a una o varias vistas de destino de representación (RTV) o a una vista de galería de símbolos de profundidad (DSV).
- Lista de operaciones de GPU destinadas a ese conjunto de enlaces de salida.
- Metadatos que describen las dependencias de carga y almacenamiento de todos los enlaces de salida de destino del paso de representación.

### <a name="declare-your-output-bindings"></a>Declaración de los enlaces de salida

Al principio de un paso de representación, se declaran enlaces a los destinos de representación o al búfer de profundidad o galería de símbolos. Es opcional enlazar para representar destinos y es opcional enlazar a un búfer de profundidad o galería de símbolos. Pero debe enlazar al menos a uno de los dos y, en el ejemplo de código siguiente, enlazaremos a ambos.

Estos enlaces se declaran en una llamada a [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

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

Establezca el primer campo [](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) de la estructura D3D12_RENDER_PASS_RENDER_TARGET_DESC en el identificador del descriptor de CPU correspondiente a una o varias vistas de destino de representación (RTV). De forma similar, [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) contiene el identificador del descriptor de CPU correspondiente a una vista de galería de símbolos de profundidad (DSV). Esos identificadores de descriptor de CPU son los mismos que se pasarían a [**ID3D12GraphicsCommandList::OMSetRenderTargets.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets) Y, al igual que **con OMSetRenderTargets,** los descriptores de CPU se alinean desde sus respectivos montones (descriptor de CPU) en el momento de la llamada a **BeginRenderPass**. 

Los RTV y DSV no se heredan en en el paso de representación. En su lugar, deben establecerse. Tampoco se propagan los RTV y DSV declarados en **BeginRenderPass** a la lista de comandos. En su lugar, se encuentran en un estado indefinido después del paso de representación.

### <a name="render-passes-and-workloads"></a>Representaciones de pases y cargas de trabajo

No se pueden anidar pases de representación y no se puede tener un paso de representación en más de una lista de comandos (deben comenzar y finalizar mientras se graban en una sola lista de comandos). Las optimizaciones diseñadas para permitir una generación multiproceso eficaz de pases de representación se deba a continuación en la sección [ Render pass Flags](#render-pass-flags)(Marcas de paso de representación).

Una escritura que se realice desde dentro  de un paso de representación no es válida para leer hasta un paso de representación posterior. Esto impide algunos tipos de barreras desde dentro del paso de representación, por ejemplo, la barrera de RENDER_TARGET a SHADER_RESOURCE en el destino de &mdash; representación enlazado actualmente.   Para obtener más información, consulte la sección Representa los pasos y [las barreras de recursos,](#render-passes-and-resource-barriers)a continuación.

La única excepción a la restricción de lectura de escritura que se acaba de mencionar implica las lecturas implícitas que se producen como parte de las pruebas de profundidad y la combinación de destino de representación.
Por lo tanto, estas API no están permitidos dentro de un paso de representación (el entorno de ejecución principal quita la lista de comandos si se llama a cualquiera de ellas durante la grabación).

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

### <a name="render-passes-and-resource-barriers"></a>Representa las barreras de recursos y los pases

No puede leer ni consumir una escritura que se haya producido dentro del mismo paso de representación. Ciertas barreras no se ajustan a  esta restricción, por ejemplo, de **\* D3D12_RESOURCE_STATE_RENDER_TARGET a _SHADER_RESOURCE** en el destino de representación enlazado actualmente (y la capa de depuración producirá un error en ese efecto). Sin embargo, esa misma barrera en  un destino de representación que se escribió fuera del paso de representación actual es compatible, porque las escrituras se completarán antes del inicio del paso de representación actual.
Es posible que se beneficie de conocer ciertas optimizaciones que un controlador de pantalla puede realizar en este sentido. Dada una carga de trabajo compatible, un controlador de pantalla podría mover las barreras detectadas en el paso de representación al principio del paso de representación. Allí, se pueden coalir (y no interferir con ninguna operación de tiling/binning). Se trata de una optimización válida siempre que todas las escrituras finalicen antes de que se inicie el paso de representación actual.

Este es un ejemplo más completo de optimización de controladores, en el que se da por supuesto que tiene un motor de representación que tiene un diseño de enlace de recursos anterior a Direct3D 12 que hace barreras a petición en función de cómo se enlazan los &mdash; recursos.  Al escribir en una vista de acceso no ordenado (UAV) hacia el final de un fotograma (que se consumirá en el fotograma siguiente), es posible que el motor deje el recurso en el estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** al finalizar el fotograma. En el marco siguiente, cuando el motor vaya a enlazar el recurso como una vista de recursos de sombreador (SRV), verá que el recurso no está en el estado correcto y emitirá una barrera de **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** a **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Si esa barrera se produce dentro del paso de representación, el controlador de  pantalla se justifica en el supuesto de que todas las escrituras ya  se han producido fuera de este paso de representación actual y, por tanto, (y aquí es donde entra en juego la optimización), el controlador de pantalla podría mover la barrera hasta el inicio del paso de representación. Una vez más, esto es válido, siempre y cuando el código se ajuste a la restricción de lectura y escritura descrita en esta sección y en la última.


Estos son ejemplos de barreras compatibles.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** para **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** a **\* _SHADER_RESOURCE**.

Y estos son ejemplos de barreras no compatibles.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** a cualquier estado de lectura en RTV o DSV enlazados actualmente.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** a cualquier estado de lectura en RTV o DSV enlazados actualmente.
- Cualquier barrera de alias.
- Barreras de la vista de acceso no ordenado (UAV). 

### <a name="resource-access-declaration"></a>Declaración de acceso a recursos

En **el momento de BeginRenderPass,** además de declarar todos los recursos que sirven como RTV o DSV dentro de ese paso, también debe especificar sus características de acceso inicial y final.  Como puede ver en el [](#declare-your-output-bindings) ejemplo de código de la sección Declaración de los enlaces de salida anterior, lo hace con las estructuras [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) y [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) salida.

Para obtener más información, vea [**las estructuras D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) y [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) y las [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) y [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) enumeraciones.

### <a name="render-pass-flags"></a>Representar marcas de paso

El último parámetro pasado a **BeginRenderPass** es una marca de paso de representación (un valor de la [**enumeración D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) representación).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>Escrituras UAV dentro de un paso de representación

Las escrituras de la vista de acceso desordenado (UAV) se permiten dentro de un paso de representación, pero debe indicar específicamente que va a emitir escrituras UAV dentro del paso de representación especificando **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES**, para que el controlador de pantalla pueda rechazar el tiling si es necesario.

Los accesos UAV deben seguir la restricción de escritura y lectura descrita anteriormente (las escrituras en un paso de representación no son válidas para leer hasta un paso de representación posterior). No se permiten barreras UAV dentro de un paso de representación.

Los enlaces UAV (a través de tablas raíz o descriptores raíz) se heredan en pases de representación y se propagan fuera de los pases de representación.

#### <a name="suspending-passes-and-resuming-passes"></a>Suspender los pases y reanudar los pases

Puede indicar que un paso de representación completo es un paso de suspensión o un paso de reanudación. Un par de suspensión seguido por reanudación debe tener vistas o marcas de acceso idénticas entre las pasadas y puede no tener ninguna operación de GPU intermedia (por ejemplo, draws, dispatches, discards, clears, copies, update-tile-mappings, write-buffer-immediates, consultas, resolución de consultas) entre el paso de representación de suspensión y el paso de representación reanudando.

El caso de uso previsto es la representación multiproceso, donde, por ejemplo, cuatro listas de comandos (cada una con sus propios pases de representación) pueden tener como destino los mismos destinos de representación. Cuando se suspenden o reanudan los pases de representación entre listas de comandos, las listas de comandos se deben ejecutar en la misma llamada a [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Un paso de representación puede reanudarse y suspenderse. En el ejemplo multiproceso que se acaba de dar, las listas de comandos 2 y 3 se reanudarían de 1 y 2, respectivamente. Y al mismo tiempo, 2 y 3 se suspenderían a 3 y 4, respectivamente.

## <a name="query-for-render-passes-feature-support"></a>Compatibilidad con las características de las pruebas de representación

Puede llamar a [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para consultar en qué medida un controlador de dispositivo o el hardware admiten eficazmente los pases de representación.

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

Debido a la lógica de asignación del tiempo de ejecución, la función de los pases de representación siempre. Pero, dependiendo de la compatibilidad con características, no siempre proporcionarán una ventaja. Puede usar código similar al ejemplo de código anterior para determinar si merece la pena emitir comandos como pasos de representación y cuando definitivamente no es una ventaja (es decir, cuando el tiempo de ejecución solo se asigna a la superficie de API existente). Realizar esta comprobación es especialmente importante si usa [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)).

Para obtener una descripción de los tres niveles de compatibilidad, consulte la [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) enumeración.
