---
title: CD3DX12_PIPELINE_STATE_STREAM1 estructura (D3dx12.h)
description: Estructura auxiliar para crear y trabajar con gráficos y estados de canalización de proceso a través de una interfaz combinada. Vea [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) y [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- CD3DX12_PIPELINE_STATE_STREAM1 estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56422aeb9b6f1c0bb87b31960b21068e75bd70d
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520454"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>CD3DX12_PIPELINE_STATE_STREAM1 estructura

Estructura auxiliar para crear y trabajar con gráficos y estados de canalización de proceso a través de una interfaz combinada. Vea [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) y [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12_PIPELINE_STATE_STREAM1 admite el Windows 10 Fall Creators Update nuevas características, como la creación de instancias de vistas.

Consulte [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream2.md) compatibilidad con la compilación 19041+ del sistema operativo (donde hay una canalización de sombreador de malla).

## <a name="syntax"></a>Sintaxis

```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```

## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un CD3DX12_PIPELINE_STATE_STREAM1.

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12_PIPELINE_STATE_STREAM1, inicializado con valores copiados de una **CD3DX12_PIPELINE_STATE_STREAM1** estructura.

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12_PIPELINE_STATE_STREAM1, inicializado con valores copiados de una **CD3DX12_PIPELINE_STATE_STREAM1** estructura.

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

devuelve el contenido del objeto CD3DX12_PIPELINE_STATE_STREAM1 como una estructura D3D12_GRAPHICS_PIPELINE_STATE_DESC estructura por valor. Tenga en D3D12_GRAPHICS_PIPELINE_STATE_DESC no incluye el **miembro CS,** por lo que este valor se pierde en la conversión.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

devuelve el contenido del objeto CD3DX12_PIPELINE_STATE_STREAM1 como estructura D3D12_COMPUTE_PIPELINE_STATE_DESC estructura por valor. Tenga en cuenta que D3D12_COMPUTE_PIPELINE_STATE_DESC no incluye los miembros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats,** **SampleDesc** o **SampleMask,** por lo que estos valores se pierden en el Conversión.

</dd> <dt>

**Marcas**
</dt> <dd>

Describe las marcas de estado de canalización, que controlan características como "depuración de herramientas".

</dd> <dt>

**Máscara de nodos**
</dt> <dd>

Describe la máscara de nodo de estado de canalización, que se usa para identificar los nodos (adaptadores físicos del dispositivo) a los que se aplica el PSO en escenarios de varios adaptadores. cada bit de la máscara corresponde a un único nodo. Para escenarios de adaptador único, establezca este valor en 0.

</dd> <dt>

**pRootSignature**
</dt> <dd>

Describe la firma raíz.

</dd> <dt>

**InputLayout**
</dt> <dd>

Describe el formato de búfer de entrada para la fase de ensamblador de entrada.

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

Describe el valor de índice especial del búfer de entrada que indica un corte (discontinuidad) al usar la topología de franja de triángulo.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Describe la topología primitiva y su orden.

</dd> <dt>

**VS**
</dt> <dd>

Describe el sombreador de vértices.

</dd> <dt>

**GS**
</dt> <dd>

Describe el sombreador de geometría.

</dd> <dt>

**StreamOutput**
</dt> <dd>

Describe el búfer de salida de streaming.

</dd> <dt>

**HS**
</dt> <dd>

Describe el sombreador de casco.

</dd> <dt>

**DS**
</dt> <dd>

Describe el sombreador de dominio.

</dd> <dt>

**PS**
</dt> <dd>

Describe el sombreador de píxeles.

</dd> <dt>

**CS**
</dt> <dd>

Describe el sombreador de proceso.

</dd> <dt>

**BlendState**
</dt> <dd>

Describe el estado de mezcla.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Describe el estado de la galería de símbolos de profundidad.

</dd> <dt>

**DSVFormat**
</dt> <dd>

Describe el formato de galería de símbolos de profundidad.

</dd> <dt>

**RasterizerState**
</dt> <dd>

Describe el estado del rasterizador.

</dd> <dt>

**RTVFormats**
</dt> <dd>

Describe los formatos de destino de representación.

</dd> <dt>

**SampleDesc**
</dt> <dd>

Describe el recuento de muestras y la calidad.

</dd> <dt>

**Máscara de ejemplo**
</dt> <dd>

Describe la máscara de ejemplo utilizada con el estado de mezcla.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Describe un PSO almacenado en caché.

</dd> </dl>

## <a name="remarks"></a>Comentarios

[CD3DX12_PIPELINE_STATE_STREAM](cd3dx12-pipeline-state-stream.md) admite el Windows 10 Fall Creators Update, pero no admite los tipos de subobjetos agregados en Windows 10 Fall Creators Update, como para la creación de instancias de vistas. Para admitir los nuevos tipos de subobjeto, use **CD3DX12_PIPELINE_STATE_STREAM1** en su lugar.

Las variables miembro accesibles de esta estructura son definiciones de tipo de la plantilla [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT,**](./cd3dx12-pipeline-state-stream-subobject.md) que combina los datos de marcador de tipo y subobjeto de subobjeto en un único objeto adecuado para una descripción de secuencia.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [Estructuras auxiliares para D3D12](helper-structures-for-d3d12.md)
* [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md)
* [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
* [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
