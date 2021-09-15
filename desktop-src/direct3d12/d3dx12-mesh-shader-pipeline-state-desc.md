---
title: D3DX12_MESH_SHADER_PIPELINE_STATE_DESC estructura (D3dx12.h)
description: Para [los sombreadores mesh/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), puede usar los datos de [effectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), con **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, para proporcionar todo el estado.
keywords:
- D3DX12_MESH_SHADER_PIPELINE_STATE_DESC estructura
topic_type:
- apiref
api_name:
- D3DX12_MESH_SHADER_PIPELINE_STATE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/02/2021
ms.openlocfilehash: 99ffe747a6cd916f82e3d2ae52f9fa368203da91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570884"
---
# <a name="d3dx12_mesh_shader_pipeline_state_desc-structure"></a>D3DX12_MESH_SHADER_PIPELINE_STATE_DESC estructura

Para [los sombreadores mesh/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), puede usar los datos de [effectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), con **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, para proporcionar todo el estado.

Consulte también [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream1.md).

Para obtener un ejemplo de código, vea [Sombreadores de malla](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription#mesh-shaders).

## <a name="syntax"></a>Sintaxis

```cpp
struct D3DX12_MESH_SHADER_PIPELINE_STATE_DESC
{
    ID3D12RootSignature* pRootSignature;
    D3D12_SHADER_BYTECODE         AS;
    D3D12_SHADER_BYTECODE         MS;
    D3D12_SHADER_BYTECODE         PS;
    D3D12_BLEND_DESC              BlendState;
    UINT                          SampleMask;
    D3D12_RASTERIZER_DESC         RasterizerState;
    D3D12_DEPTH_STENCIL_DESC      DepthStencilState;
    D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType;
    UINT                          NumRenderTargets;
    DXGI_FORMAT                   RTVFormats[D3D12_SIMULTANEOUS_RENDER_TARGET_COUNT];
    DXGI_FORMAT                   DSVFormat;
    DXGI_SAMPLE_DESC              SampleDesc;
    UINT                          NodeMask;
    D3D12_CACHED_PIPELINE_STATE   CachedPSO;
    D3D12_PIPELINE_STATE_FLAGS    Flags;
};
```

## <a name="members"></a>Members

`pRootSignature`

Tipo: **[ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Objeto de firma raíz que define qué recursos están enlazados a la canalización.

`AS`

Tipo: **[D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Contiene los datos que representan el programa de sombreador de amplificación.

`MS`

Tipo: **[D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Contiene los datos que representan el programa de sombreador de malla.

`PS`

Tipo: **[D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Contiene los datos que representan el programa de sombreador de píxeles.

`BlendState`

Tipo: **[D3D12_BLEND_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Describe el estado de mezcla.

`SampleMask`

Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**

Máscara de ejemplo para el estado de mezcla.

`RasterizerState`

Tipo: **[D3D12_RASTERIZER_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Describe el estado del rasterizador.

`DepthStencilState`

Tipo: **[D3D12_DEPTH_STENCIL_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Describe el estado de la galería de símbolos de profundidad.

`PrimitiveTopologyType`

Tipo: **[D3D12_PRIMITIVE_TOPOLOGY_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Describe el tipo y el orden de los datos primitivos.

`NumRenderTargets`

Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**

Número de formatos de destino de representación en *el miembro RTVFormats.*

`RTVFormats`

Tipo: **[DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Matriz de valores para los formatos de destino de representación.

`DSVFormat`

Tipo: **[DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Valor para el formato de galería de símbolos de profundidad.

`SampleDesc`

Tipo: **[DXGI_SAMPLE_DESC](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Especifica parámetros multimuestreo.

`CachedPSO`

Tipo: **[D3D12_CACHED_PIPELINE_STATE](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Objeto de estado de canalización almacenado en caché. *pCachedBlob y* *CachedBlobSizeInBytes* se pueden establecer en NULL y 0, respectivamente.

`Flags`

Tipo: **[D3D12_PIPELINE_STATE_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Constante de enumeración de marcas (por ejemplo, para indicar que el estado de la canalización debe compilarse con información adicional para ayudar a la depuración).

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream1.md)
* [sombreadores mesh/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)
* [EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription)
