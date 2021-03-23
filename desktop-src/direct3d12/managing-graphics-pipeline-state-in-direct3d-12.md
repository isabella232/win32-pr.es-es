---
title: Administrar el estado de canalización de gráficos en Direct3D 12
description: En este tema se describe cómo se establece el estado de canalización de gráficos en Direct3D 12.
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- Estado de canalización
- objeto de estado de canalización
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549193"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>Administrar el estado de canalización de gráficos en Direct3D 12

En este tema se describe cómo se establece el estado de canalización de gráficos en Direct3D 12.

## <a name="pipeline-state-overview"></a>Información general sobre el estado de canalización

Cuando la geometría se envía a la unidad de procesamiento de gráficos (GPU) que se va a dibujar, hay una amplia gama de opciones de hardware que determinan cómo se interpretan y representan los datos de entrada. Colectivamente, estos valores se denominan el estado de canalización de gráficos e incluyen valores comunes como el estado del rasterizador, el estado de Blend y el estado de la galería de símbolos de profundidad, así como el tipo de topología primitiva de la geometría enviada y los sombreadores que se usarán para la representación. En Microsoft Direct3D 12, la mayoría del estado de canalización de gráficos se establece mediante el uso de objetos de estado de canalización (PSO). Una aplicación puede crear un número ilimitado de estos objetos, representados por la interfaz [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) , normalmente en el momento de la inicialización. Después, en el momento de la representación, las listas de comandos pueden cambiar rápidamente varias configuraciones del estado de la canalización mediante una llamada a [**ID3D12GraphicsCommandList:: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) en una lista de comandos directa o un paquete para establecer el valor de PSO activo.

En Direct3D 11, el estado de canalización de gráficos se incluyó en objetos de estado grandes y generales, como [**ID3D11BlendState**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) , que se podían crear y establecer en tiempo de representación en el contexto inmediato con métodos como [**ID3D11DeviceContext:: OMSetBlendState**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate). La idea de esto es que la GPU podría obtener eficiencias estableciendo la configuración relacionada, como la configuración de estado de Blend, todas a la vez. Sin embargo, con el hardware de gráficos de hoy en día, existen dependencias entre las distintas unidades de hardware. Por ejemplo, el estado de mezcla de hardware puede tener dependencias en el estado de rasterizado, así como en el estado de mezcla. PSO en Direct3D 12 se ha diseñado para permitir que la GPU procese previamente todas las configuraciones dependientes en cada estado de canalización, normalmente durante la inicialización, para que el cambio entre Estados en el tiempo de representación sea lo más eficaz posible.

Tenga en cuenta que, aunque la mayor parte de la configuración de estado de canalización se establece mediante PSO, hay algunas configuraciones de estado que se establecen por separado mediante las API proporcionadas por [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist). Esta configuración y las API asociadas se describen con más detalle a continuación. Además, existen diferencias en la manera en que el estado de canalización de gráficos es heredado por y se conservan de las listas de comandos y agrupaciones directas. En este tema se proporcionan detalles sobre ambas opciones.

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>Estados de canalización de gráficos establecidos con objetos de estado de canalización

La forma más fácil de ver todos los distintos Estados de canalización que se pueden establecer mediante un objeto de estado de canalización es consultar el tema de referencia de la [**\_ Descripción del \_ \_ estado \_ de canalización de gráficos de D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) que se pasa a [**ID3D12Device:: CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) cuando se inicializa el objeto. Un resumen rápido de los Estados que se pueden establecer incluye:

-   Código de bytes para todos los sombreadores, incluidos los sombreadores de vértices, de píxeles, de dominios, de casco y de geometría.
-   Formato del vértice de entrada.
-   Tipo de topología primitiva. Tenga en cuenta que el tipo de topología primitiva del ensamblador de entrada (punto, línea, triángulo, revisión) se establece dentro del PSO mediante la enumeración de [**\_ \_ \_ tipo de topología primitiva D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) . La adyacencia y el orden primitivos (lista de líneas, franja de líneas, franja de líneas con datos de adyacencia, etc.) se establecen en una lista de comandos mediante el método [**ID3D12GraphicsCommandList:: IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology) .
-   Estado de Blend, estado de rasterizador, estado de estarcido de profundidad.
-   La galería de símbolos de profundidad y los formatos de destino de representación, así como el número de destinos de representación.
-   Parámetros de muestreo múltiple.
-   Búfer de salida de streaming.
-   La firma raíz. Para obtener más información, consulte [signaturas de raíz](root-signatures.md).

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>Estados de canalización de gráficos establecidos fuera del objeto de estado de canalización

La mayoría de los Estados de canalización de gráficos se establecen mediante PSO. Sin embargo, hay un conjunto de parámetros de estado de canalización que se establecen mediante la llamada a métodos de la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) desde una lista de comandos. En la tabla siguiente se muestran los Estados que se establecen de esta manera y los métodos correspondientes.

|State|Método|
|-|-|
|Enlaces de recursos|[**IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>Todos los métodos **SetGraphicsRoot...**<br/>Todos los métodos **SetComputeRoot...**<br/>
|Ventanillas|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**RSSetViewports**</a>|
|Rectángulos con tijeras|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**RSSetScissorRects**</a>|
|Factor de mezcla|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**OMSetBlendFactor**</a>|
|Valor de referencia de estarcido de profundidad|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**OMSetStencilRef**</a>|
|El orden de topología primitiva del ensamblador de entrada y el tipo de adyacencia|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**IASetPrimitiveTopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>Herencia de estado de canalización de gráficos

Dado que las listas de comandos directas están pensadas generalmente para un uso a la vez y las agrupaciones están diseñadas para usarse varias veces al mismo tiempo, hay diferentes reglas sobre cómo heredan el estado de canalización de gráficos que se estableció en las listas de comandos o agrupaciones anteriores.

En el caso de los Estados de canalización de gráficos que se establecen mediante PSO, ninguno de estos Estados se hereda mediante listas de comandos directas o agrupaciones. El estado inicial de canalización de gráficos para las listas de comandos y agrupaciones directas se establece en el momento de la creación con el parámetro [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) en [**ID3D12Device:: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist). Si no se especifica ningún PSO en la llamada, se usa un estado inicial predeterminado. Puede cambiar el PSO actual en una lista de comandos mediante una llamada a [**ID3D12GraphicsCommandList:: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Las listas de comandos directas tampoco heredan el estado establecido con métodos de lista de comandos como [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports). Para obtener más información sobre los valores iniciales predeterminados para Estados que no son de PSO, vea [**ID3D12GraphicsCommandList:: ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate).

Las agrupaciones heredan todo el estado de canalización de gráficos que no se establece con PSO, excepto el tipo de topología primitiva. La topología primitiva siempre se establece en el [**\_ tipo de \_ topología primitiva D3D12 \_ sin \_ definir**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) cuando se inicia la ejecución de un lote. Cualquier Estado que se establece dentro de una agrupación (el propio PSO, el estado basado en no PSO y los enlaces de recursos) afecta al estado de su lista de comandos directa. Por ejemplo, si se llama a [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) desde una agrupación, las ventanillas especificadas seguirán estando establecidas en la lista de comandos directa primaria para las llamadas posteriores a la llamada [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) que establecen las ventanillas.

Los enlaces de recursos que se establecen en una lista de comandos o un paquete se conservan. Por tanto, los enlaces de recursos modificados en una lista de comandos directa se seguirán definiendo en la ejecución posterior del lote secundario. Los enlaces de recursos y modificados desde dentro de un paquete se seguirán definiendo para las llamadas subsiguientes dentro de la lista de comandos directa primaria.

Para obtener más información sobre los enlaces, consulte la sección sobre la **semántica de agrupación** del [uso de una firma raíz](using-a-root-signature.md).

## <a name="related-topics"></a>Temas relacionados

* [Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)