---
title: CD3DX12_PIPELINE_STATE_STREAM2 estructura (D3dx12.h)
description: Estructura auxiliar para crear y trabajar con estados de canalización de proceso y gráficos a través de una interfaz combinada.
keywords:
- CD3DX12_PIPELINE_STATE_STREAM2 estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812336"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>CD3DX12_PIPELINE_STATE_STREAM2 estructura

Estructura auxiliar para crear y trabajar con estados de canalización de proceso y gráficos a través de una interfaz combinada. Vea [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) y [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

**CD3DX12_PIPELINE_STATE_STREAM2** admite OS Build 19041+ (donde hay una canalización de sombreador de malla).

## <a name="syntax"></a>Sintaxis

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>Miembros

`CD3DX12_PIPELINE_STATE_STREAM2`

Constructor predeterminado. Crea una nueva instancia sin inicializar de un **CD3DX12_PIPELINE_STATE_STREAM2**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_PIPELINE_STATE_STREAM2** inicializado con el contenido de una [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) estructura.

A continuación, deberá establecer sombreadores de malla y de amplificación manualmente, ya que no tienen representación en **D3D12_GRAPHICS_PIPELINE_STATE_DESC**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_PIPELINE_STATE_STREAM2** inicializado con el contenido de una [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) estructura.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_PIPELINE_STATE_STREAM2** inicializado con el contenido de una [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) estructura.

`Flags`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

Marcas (por ejemplo, para indicar que el estado de la canalización debe compilarse con información adicional para ayudar a la depuración).

`NodeMask`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

Describe la máscara de nodo de estado de canalización, que se usa para identificar los nodos (adaptadores físicos del dispositivo) a los que se aplica el PSO en escenarios de varios adaptadores. cada bit de la máscara corresponde a un único nodo. Para escenarios de adaptador único, use 0.

`pRootSignature`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

Describe la firma raíz.

`InputLayout`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

Describe el formato de búfer de entrada para la fase de ensamblador de entrada.

`IBStripCutValue`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

Describe el valor de índice especial del búfer de entrada que indica un corte (discontinuidad) al usar la topología de franja de triángulo.

`PrimitiveTopologyType`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

Describe la topología primitiva y su orden.

`VS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

Describe el sombreador de vértices.

`GS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

Describe el sombreador de geometría.

`StreamOutput`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

Describe el búfer de salida de streaming.

`HS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

Describe el sombreador de casco.

`DS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

Describe el sombreador de dominio.

`PS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

Describe el sombreador de píxeles.

`AS`

Tipo: **CD3DX12_PIPELINE_STATE_STREAM_AS**

Describe el sombreador de amplificación.

`MS`

Tipo: **CD3DX12_PIPELINE_STATE_STREAM_MS**

Describe el sombreador de malla.

`CS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

Describe el sombreador de proceso.

`BlendState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

Describe el estado de mezcla.

`DepthStencilState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

Describe el estado de la galería de símbolos de profundidad.

`DSVFormat`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

Describe el formato de galería de símbolos de profundidad.

`RasterizerState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

Describe el estado del rasterizador.

`RTVFormats`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

Describe los formatos de destino de representación.

`SampleDesc`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

Describe el recuento de muestras y la calidad.

`SampleMask`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

Describe la máscara de ejemplo utilizada con el estado de mezcla.

`CachedPSO`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

Describe un PSO almacenado en caché.

`ViewInstancingDesc`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

Describe una configuración de creación de instancias de vista.

`GraphicsDescV0`

Devuelve [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc).

devuelve el contenido del objeto **CD3DX12_PIPELINE_STATE_STREAM2** como una **estructura D3D12_GRAPHICS_PIPELINE_STATE_DESC** estructura por valor. **D3D12_GRAPHICS_PIPELINE_STATE_DESC** no incluye el miembro *CS,* por lo que el valor se pierde en la conversión.

`ComputeDescV0`

Devuelve [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

devuelve el contenido del objeto **CD3DX12_PIPELINE_STATE_STREAM2** como una **estructura D3D12_COMPUTE_PIPELINE_STATE_DESC** estructura por valor. **D3D12_COMPUTE_PIPELINE_STATE_DESC** no incluye los miembros *InputLayout*, *IBStripCutValue*, *PrimitiveTopologyType*, *VS*, *GS*, *StreamOutput*, *HS*, *DS*, *PS*, *BlendState*, *DepthStencilState*, *DSVFormat*, *RasterizerState*, *NumRootSignature*, *RTVFormats,* *SampleDesc* y *SampleMask,* por lo que esos valores se pierden en la conversión.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
