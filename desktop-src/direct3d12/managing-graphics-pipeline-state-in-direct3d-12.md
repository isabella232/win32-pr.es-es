---
title: Administración del estado de la canalización de gráficos en Direct3D 12
description: En este tema se describe cómo se establece el estado de canalización de gráficos en Direct3D 12.
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- estado de canalización
- objeto de estado de canalización
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567993"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>Administración del estado de la canalización de gráficos en Direct3D 12

En este tema se describe cómo se establece el estado de canalización de gráficos en Direct3D 12.

## <a name="pipeline-state-overview"></a>Información general sobre el estado de canalización

Cuando se envía geometría a la unidad de procesamiento gráfico (GPU) que se va a dibujar, hay una amplia gama de configuraciones de hardware que determinan cómo se interpretan y representan los datos de entrada. En conjunto, estos valores se denominan estado de canalización de gráficos e incluyen valores comunes, como el estado del rasterizador, el estado de mezcla y el estado de la galería de símbolos de profundidad, así como el tipo de topología primitiva de la geometría enviada y los sombreadores que se usarán para la representación. En Microsoft Direct3D 12, la mayoría del estado de canalización de gráficos se establece mediante objetos de estado de canalización (PSO). Una aplicación puede crear un número ilimitado de estos objetos, representados por la interfaz [**ID3D12PipelineState,**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) normalmente en tiempo de inicialización. A continuación, en tiempo de representación, las listas de comandos pueden cambiar rápidamente varias configuraciones del estado de canalización mediante una llamada a [**ID3D12GraphicsCommandList::SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) en una lista o agrupación de comandos directos para establecer el PSO activo.

En Direct3D 11, el estado de canalización de gráficos se agrupaba en objetos de estado grandes y general, como [**ID3D11BlendState,**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) que se podían crear y establecer en tiempo de representación en el contexto inmediato con métodos como [**ID3D11DeviceContext::OMSetBlendState.**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate) La idea detrás de esto era que la GPU podía obtener eficiencias estableciendo la configuración relacionada, como la configuración de estado de mezcla, a la vez. Sin embargo, con el hardware gráfico actual, hay dependencias entre las distintas unidades de hardware. Por ejemplo, el estado de mezcla de hardware podría tener dependencias en el estado de trama, así como en el estado de mezcla. Los PSO de Direct3D 12 se diseñaron para permitir que la GPU procese previamente todas las configuraciones dependientes en cada estado de canalización, normalmente durante la inicialización, para que el cambio entre estados en tiempo de representación sea lo más eficaz posible.

Tenga en cuenta que aunque la mayor parte de la configuración de estado de canalización se establece mediante PSO, hay algunas configuraciones de estado que se establecen por separado mediante las API proporcionadas por [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist). Esta configuración y las API asociadas se detalló a continuación. Además, hay diferencias en la forma en que hereda el estado de canalización de gráficos y se conserva de listas de comandos y agrupaciones directas. En este tema se proporcionan detalles sobre ambos a continuación.

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>Estados de canalización de gráficos establecidos con objetos de estado de canalización

La manera más fácil de ver todos los distintos estados de canalización que se pueden establecer mediante un objeto de estado de canalización es consultar el tema de referencia de [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) que se pasa a [**ID3D12Device::CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) al inicializar el objeto. Un resumen rápido de los estados que se pueden establecer incluye:

-   Código de bytes para todos los sombreadores, incluidos los sombreadores de vértice, píxel, dominio, casco y geometría.
-   Formato de vértice de entrada.
-   Tipo de topología primitiva. Tenga en cuenta que el tipo de topología primitiva de ensamblador de entrada (punto, línea, triángulo, revisión) se establece dentro del PSO mediante la [**enumeración D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) La adyacencia primitiva y la ordenación (lista de líneas, franja de líneas, franja de líneas con datos de adyacencia, etc.) se establecen desde una lista de comandos mediante el método [**ID3D12GraphicsCommandList::IASetPrimitiveTopology.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)
-   Estado de mezcla, estado de rasterizador, estado de galería de símbolos de profundidad.
-   La galería de símbolos de profundidad y los formatos de destino de representación, así como el recuento de destinos de representación.
-   Parámetros de muestreo múltiple.
-   Búfer de salida de streaming.
-   Firma raíz. Para obtener más información, vea [Root Signatures](root-signatures.md).

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>Estados de canalización de gráficos establecidos fuera del objeto de estado de canalización

La mayoría de los estados de canalización de gráficos se establecen mediante PSO. Sin embargo, hay un conjunto de parámetros de estado de canalización que se establecen mediante una llamada a métodos de la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) desde una lista de comandos. En la tabla siguiente se muestran los estados que se establecen de esta manera y los métodos correspondientes.

|State|Método|
|-|-|
|Enlaces de recursos|[**IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>Todos **los métodos SetGraphicsRoot...**<br/>Todos **los métodos SetComputeRoot...**<br/>
|Viewports|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**RSSetViewports**</a>|
|Rects de insaseción|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**RSSetScissorRects**</a>|
|Factor blend|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**OMSetBlendFactor**</a>|
|Valor de referencia de la galería de símbolos de profundidad|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**OMSetStencilRef**</a>|
|El orden de topología primitivo de ensamblador de entrada y el tipo de adyacencia|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**IASetPrimitiveTopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>Herencia de estado de canalización de gráficos

Dado que las listas de comandos directos suelen estar diseñadas para un uso a la vez y las agrupaciones están diseñadas para usarse varias veces al mismo tiempo, hay distintas reglas sobre cómo heredan el estado de canalización de gráficos establecido por listas de comandos o agrupaciones anteriores.

Para los estados de canalización de gráficos que se establecen mediante PSO, ninguno de estos estados se hereda mediante listas o agrupaciones de comandos directos. El estado inicial de canalización de gráficos para listas de comandos directos y agrupaciones se establece en el momento de la creación con el parámetro [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) en [**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist). Si no se especifica ningún PSO en la llamada, se usa un estado inicial predeterminado. Puede cambiar el PSO actual dentro de una lista de comandos llamando a [**ID3D12GraphicsCommandList::SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Las listas de comandos directos tampoco heredan el estado establecido con métodos de lista de comandos como [**RSSetViewports.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) Para obtener más información sobre los valores iniciales predeterminados para los estados que no son PSO, [**vea ID3D12GraphicsCommandList::ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate).

Los paquetes heredan todo el estado de canalización de gráficos que no se establece con PSO, excepto el tipo de topología primitiva. La topología primitiva siempre se establece en [**D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE \_ UNDEFINED**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) cuando una agrupación comienza a ejecutarse. Cualquier estado que se establece dentro de una agrupación (el propio PSO, el estado no basado en PSO y los enlaces de recursos) afecta al estado de su lista de comandos directos primaria. Por ejemplo, si se llama a [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) desde dentro de una agrupación, las ventanillas especificadas seguirán estando establecidas en la lista de comandos directos primarios para las llamadas posteriores a la llamada [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) que establecen las ventanillas.

Los enlaces de recursos que se establecen dentro de una lista de comandos o agrupación se conservan. Por lo tanto, los enlaces de recursos modificados en una lista de comandos directos todavía se establecerán en la ejecución posterior del paquete secundario. Y los enlaces de recursos modificados desde dentro de una agrupación se seguirán configurando para las llamadas posteriores dentro de la lista de comandos directos principal.

Para obtener más información sobre los enlaces, consulte la sección **Semántica de agrupación** [de Using a Root Signature](using-a-root-signature.md).

## <a name="related-topics"></a>Temas relacionados

* [Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)