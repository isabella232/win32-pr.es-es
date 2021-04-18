---
title: CD3DX12_PIPELINE_STATE_STREAM1 estructura (D3dx12. h)
description: Una estructura auxiliar para crear y trabajar con los Estados de canalización de gráficos y proceso a través de una interfaz combinada. Consulte D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC and D3D12 \_ Compute \_ Pipeline \_ State \_ desc. | CD3DX12_PIPELINE_STATE_STREAM1 estructura (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM1
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
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717611"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>\_ \_ Estructura STREAM1 de estado de CANALización CD3DX12 \_

Una estructura auxiliar para crear y trabajar con los Estados de canalización de gráficos y proceso a través de una interfaz combinada. Consulte [**D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ Compute \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_El estado de canalización \_ de CD3DX12 \_ STREAM1 admite Windows 10 Fall Creators Update con nuevas características, como la creación de instancias de la vista.

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

**\_Estado de canalización de CD3DX12 \_ \_ STREAM1 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ STREAM1 de estado de canalización CD3DX12 \_ \_ .

</dd> <dt>

**\_Estado de canalización de CD3DX12 \_ \_ STREAM1 (const D3D12 \_ gráfico de estado de \_ canalización \_ \_ DESC& DESC)**
</dt> <dd>

Crea una nueva instancia de un \_ STREAM1 de estado de canalización de CD3DX12 \_ \_ , inicializada con los valores copiados de una estructura de STREAM1 de **\_ \_ estado \_ de canalización de CD3DX12** .

</dd> <dt>

**\_Estado de canalización de CD3DX12 \_ \_ STREAM1 (const D3D12 \_ Estado de canalización de proceso \_ \_ \_ DESC& DESC)**
</dt> <dd>

Crea una nueva instancia de un \_ STREAM1 de estado de canalización de CD3DX12 \_ \_ , inicializada con los valores copiados de una estructura de STREAM1 de **\_ \_ estado \_ de canalización de CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Devuelve el contenido del \_ objeto STREAM1 de estado de la canalización CD3DX12 \_ \_ como una \_ estructura de DESC de estado de canalización de gráficos D3D12 \_ \_ \_ por valor. Tenga en cuenta \_ que \_ \_ \_ la descripción del estado de canalización de gráficos D3D12 no incluye el miembro **CS** , por lo que este valor se pierde en la conversión.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Devuelve el contenido del \_ objeto STREAM1 de estado de la canalización de CD3DX12 \_ \_ como una \_ estructura de DESC de estado de canalización de D3D12 \_ \_ \_ por valor. Tenga en cuenta que \_ \_ la descripción del estado de la canalización de proceso de D3D12 \_ \_ no incluye los miembros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask** , por lo que estos valores se pierden en la conversión.

</dd> <dt>

**Marcas**
</dt> <dd>

Describe las marcas de estado de canalización, que controlan características como "depuración de la herramienta".

</dd> <dt>

**NodeMask**
</dt> <dd>

Describe la máscara de nodo de estado de canalización, que se usa para identificar los nodos (adaptadores físicos del dispositivo) a los que se aplica el PSO en escenarios de varios adaptadores. cada bit de la máscara corresponde a un solo nodo. En escenarios de un solo adaptador, establezca este valor en 0.

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

Describe el valor de índice especial del búfer de entrada que indica un corte (discontinuidad) cuando se usa la topología de franja triangular.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Describe la topología primitiva y su orden.

</dd> <dt>

**VIRTUAL**
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

**!**
</dt> <dd>

Describe el sombreador de casco.

</dd> <dt>

**DS**
</dt> <dd>

Describe el sombreador de dominios.

</dd> <dt>

**PS**
</dt> <dd>

Describe el sombreador de píxeles.

</dd> <dt>

**CS**
</dt> <dd>

Describe el sombreador de cálculo.

</dd> <dt>

**BlendState**
</dt> <dd>

Describe el estado de Blend.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Describe el estado de la galería de símbolos de profundidad.

</dd> <dt>

**DSVFormat**
</dt> <dd>

Describe el formato de la galería de símbolos de profundidad.

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

Describe el recuento y la calidad de ejemplo.

</dd> <dt>

**SampleMask**
</dt> <dd>

Describe la máscara de ejemplo utilizada con el estado de Blend.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Describe un PSO almacenado en caché.

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**CD3DX12 \_ El \_ \_ flujo de estado de la canalización**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) es compatible con Windows 10 Fall Creators Update, pero no admite los tipos de subobjetos agregados en Windows 10 Fall Creators Update, como para la creación de instancias de la vista. Para admitir los nuevos tipos de subobjeto, use el \_ Estado de canalización de CD3DX12 \_ \_ STREAM1 en su lugar.

Las variables de miembro accesibles de esta estructura son todas las definiciones de \_ tipo de la plantilla de subobjeto de flujo de estado de canalización de CD3DX12 \_ \_ \_ , que combina los datos de marcador y tipo de subobjeto en un solo objeto adecuado para una descripción de flujo.

Estas typedefs son:

<dl> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Secuencia de estado de la \_ canalización CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[**\_Descripción de \_ Estado de canalización de gráficos de \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_Descripción de \_ Estado de canalización de proceso de \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





