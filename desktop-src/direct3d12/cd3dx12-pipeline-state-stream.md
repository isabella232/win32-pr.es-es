---
title: CD3DX12_PIPELINE_STATE_STREAM estructura (D3dx12.h)
description: Estructura auxiliar para crear y trabajar con gráficos y estados de canalización de proceso a través de una interfaz combinada. Consulte D3D12 \_ GRAPHICS \_ PIPELINE STATE \_ \_ DESC y D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC. | CD3DX12_PIPELINE_STATE_STREAM estructura (D3dx12.h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733987"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>Estructura CD3DX12 \_ PIPELINE \_ STATE \_ STREAM

Estructura auxiliar para crear y trabajar con gráficos y estados de canalización de proceso a través de una interfaz combinada. Vea [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) y [**D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12 PIPELINE STATE STREAM admite Windows 10 Creators Update y versiones más recientes, pero no admite nuevas características de la actualización \_ fall creators, como la creación de instancias \_ \_ de vistas. Para admitir las características de la actualización Fall Creators, use [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1 en**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) su lugar.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM(const D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC& Desc)**
</dt> <dd>

Crea una nueva instancia de UNA SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con valores copiados de una estructura \_ \_ \_ **CD3DX12 \_ PIPELINE \_ STATE \_ STREAM.**

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM(const D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC& Desc)**
</dt> <dd>

Crea una nueva instancia de UNA SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con valores copiados de una estructura \_ \_ \_ **CD3DX12 \_ PIPELINE \_ STATE \_ STREAM.**

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

devuelve el contenido del objeto PIPELINE STATE STREAM de CD3DX12 como una estructura DESC DEL ESTADO DE CANALIZACIÓN DE \_ \_ \_ GRÁFICOS D3D12 \_ \_ por \_ \_ valor. Tenga en cuenta que D3D12 GRAPHICS PIPELINE STATE DESC no incluye el \_ \_ miembro \_ \_ **CS,** por lo que este valor se pierde en la conversión.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

devuelve el contenido del objeto PIPELINE STATE STREAM CD3DX12 como una estructura \_ \_ \_ \_ \_ DESC COMPUTE PIPELINE STATE \_ DESC de D3D12 \_ por valor. Tenga en cuenta que D3D12 COMPUTE PIPELINE STATE DESC no incluye los miembros \_ \_ \_ \_ **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature,** **RTVFormats,** **SampleDesc** o **SampleMask,** por lo que estos valores se pierden en la conversión.

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

**Vs**
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

**Hs**
</dt> <dd>

Describe el sombreador de casco.

</dd> <dt>

**DS**
</dt> <dd>

Describe el sombreador de dominio.

</dd> <dt>

**Ps**
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

CD3DX12 PIPELINE STATE STREAM admite Windows 10 Creators Update y versiones más recientes, pero no admite los tipos de subobjetos agregados en Windows 10 \_ \_ Fall Creators Update, como para la creación de instancias de \_ vistas. Para admitir los tipos de subobjetos agregados en la actualización fall creators, use [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1 en**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) su lugar.

Las variables miembro accesibles de esta estructura son definiciones de tipos de la plantilla DE SUBOBJETO PIPELINE STATE STREAM de CD3DX12, que combina los datos de marcador de tipo y subobjeto de subobjeto en un único objeto adecuado para una descripción de \_ \_ \_ \_ secuencia.

Estas definiciones de tipo son:

<dl> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





