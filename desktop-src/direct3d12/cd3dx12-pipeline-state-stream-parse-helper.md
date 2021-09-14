---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER estructura (D3dx12.h)
description: Compila un objeto CD3DX12 PIPELINE STATE STREAM interno a partir de los detalles del subobjeto pasados \_ a las funciones miembro \_ \_ correspondientes. Esta estructura implementa la interfaz ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969859"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>Estructura DEL ASISTENTE DE ANÁLISIS DE \_ FLUJOS DE ESTADO DE \_ \_ CANALIZACIÓN \_ \_ CD3DX12

Compila un objeto CD3DX12 PIPELINE STATE STREAM interno a partir de los detalles del subobjeto pasados \_ a las funciones miembro \_ \_ correspondientes. Esta estructura implementa la interfaz [**ID3DX12PipelineParserCallbacks.**](id3dx12pipelineparsercallbacks.md)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a>Members

<dl> <dt>

**PipelineStream**
</dt> <dd>

EL FLUJO DE ESTADO DE [**CANALIZACIÓN CD3DX12 \_ \_ \_ interno1**](cd3dx12-pipeline-state-stream1.md). Su estado actual representa el efecto acumulativo de los métodos de devolución de llamada a los que se ha llamado en este objeto.

</dd> <dt>

**FlagsCb(D3D12 \_ PIPELINE \_ STATE \_ FLAGS Flags)**
</dt> <dd>

Inicializa el miembro **Flags** de **PipelineStream** con el valor del *parámetro Flags.*

</dd> <dt>

**NodeMaskCb(UINT NodeMask)**
</dt> <dd>

Inicializa el miembro **NodeMask** de **PipelineStream** con el valor del parámetro *Nodemask.*

</dd> <dt>

**RootSignatureCb(ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Inicializa el **miembro pRootSignature** de **PipelineStream** con el valor del *parámetro pRootSignature.*

</dd> <dt>

**InputLayoutCb(const D3D12 \_ INPUT \_ LAYOUT \_ DESC& InputLayout)**
</dt> <dd>

Inicializa el **miembro InputLayout** de **PipelineStream** con el valor del *parámetro InputLayout.*

</dd> <dt>

**IBStripCutValueCb(D3D12 \_ INDEX \_ BUFFER \_ STRIP \_ CUT \_ VALUE IBStripCutValue)**
</dt> <dd>

Inicializa el **miembro IBStripCutValue** de **PipelineStream** mediante el valor del *parámetro IBStripCutValue.*

</dd> <dt>

**PrimitiveTopologyTypeCb(D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE PrimitiveTopologyType)**
</dt> <dd>

Inicializa el **miembro PrimitiveTopologyType** de **PipelineStream** con el valor del *parámetro PrimitiveTopologyType.*

</dd> <dt>

**VSCb(const D3D12 \_ SHADER \_ BYTECODE& VS)**
</dt> <dd>

Inicializa el miembro **vs** (sombreador de vértices) de **PipelineStream** con el valor del parámetro *de VS.*

</dd> <dt>

**GSCb(const D3D12 \_ SHADER \_ BYTECODE& GS)**
</dt> <dd>

Inicializa el miembro **GS** (sombreador de geometría) de **PipelineStream** con el valor del *parámetro GS.*

</dd> <dt>

**StreamOutputCb(const D3D12 \_ STREAM \_ OUTPUT \_ DESC& StreamOutput)**
</dt> <dd>

Inicializa el miembro **StreamOutput** de **PipelineStream** con el valor del *parámetro StreamOutput.*

</dd> <dt>

**HSCb(const D3D12 \_ SHADER \_ BYTECODE& HS)**
</dt> <dd>

Inicializa el miembro **HS** (sombreador de casco) de **PipelineStream** con el valor *del parámetro HS.*

</dd> <dt>

**DSCb(const D3D12 \_ SHADER \_ BYTECODE& DS)**
</dt> <dd>

Inicializa el miembro **DS** (sombreador de dominio) de **PipelineStream** con el valor del *parámetro DS.*

</dd> <dt>

**PSCb(const D3D12 \_ SHADER \_ BYTECODE& PS)**
</dt> <dd>

Inicializa el miembro **PS** (sombreador de píxeles) de **PipelineStream** con el valor del *parámetro PS.*

</dd> <dt>

**CSCb(const D3D12 \_ SHADER \_ BYTECODE& CS)**
</dt> <dd>

Inicializa el miembro **CS** de **PipelineStream** con el valor del *parámetro CS.*

</dd> <dt>

**BlendStateCb(const D3D12 \_ BLEND \_ DESC& BlendState)**
</dt> <dd>

Inicializa el miembro **BlendState** de **PipelineStream** con el valor del *parámetro BlendState.*

</dd> <dt>

**DepthStencilStateCb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& DepthStencilState)**
</dt> <dd>

Inicializa el **miembro DepthStencilState** de **PipelineStream** con el valor del parámetro *DepthStencilState,* [**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Inicializa el **miembro DepthStencilState** de **PipelineStream** con el valor del parámetro *DepthStencilState,* [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**DSVFormatCb(DXGI \_ FORMAT DSVFormat)**
</dt> <dd>

Inicializa el miembro **DSVFormat** de **PipelineStream** con el valor del *parámetro DSVFormat.*

</dd> <dt>

**RasterizerStateCb(const D3D12 \_ RASTERIZER \_ DESC& RasterizerState)**
</dt> <dd>

Inicializa el miembro **RasterizerState** de **PipelineStream** con el valor del *parámetro RasterizerState.*

</dd> <dt>

**RTVFormatsCb(const D3D12 \_ RT \_ FORMAT \_ ARRAY& RTVFormats)**
</dt> <dd>

Inicializa el **miembro RTVFormats** de **PipelineStream** con el valor del *parámetro RTVFormats.*

</dd> <dt>

**SampleDescCb(const DXGI \_ SAMPLE \_ DESC& SampleDesc)**
</dt> <dd>

Inicializa el **miembro SampleDesc** de **PipelineStream** con el valor del *parámetro SampleDesc.*

</dd> <dt>

**SampleMaskCb(UINT SampleMask)**
</dt> <dd>

Inicializa el miembro **SampleMask** de **PipelineStream** con el valor del *parámetro SampleMask.*

</dd> <dt>

**ViewInstancingCb(const D3D12 \_ VIEW \_ INSTANCING \_ DESC& ViewInstancingDesc)**
</dt> <dd>

Inicializa el **miembro ViewInstancingDesc** de **PipelineStream** con el valor del *parámetro ViewInstancingDesc.*

</dd> <dt>

**CachedPSOCb(const D3D12 \_ CACHED \_ PIPELINE \_ STATE& CachedPSO)**
</dt> <dd>

Inicializa el miembro **CachedPSO** de **PipelineStream** con el valor del *parámetro CachedPSO.*

</dd> <dt>

**ErrorBadInputParameter(UINT)**
</dt> <dd>

No hace nada.

</dd> <dt>

**ErrorDuplicateSubobject(D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE)**
</dt> <dd>

No hace nada.

</dd> <dt>

**ErrorUnknownSubobject(UINT)**
</dt> <dd>

No hace nada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se pasa como segundo parámetro a la función [**D3DX12ParsePipelineStream,**](d3dx12parsepipelinestream.md) los detalles del objeto [**INTERNO CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) se clonan a partir del [**\_ \_ \_ \_ DESC PIPELINE STATE STREAM de D3D12 que**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) se pasa como primer parámetro. Este proceso valida la descripción del flujo de origen. Si D3DX12ParsePipelineStream devuelve **S \_ OK**, la descripción de la secuencia de origen y el **CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1PipelineStream** resultante son válidos; de lo contrario, ambos no son válidos. Los flujos no válidos y otros errores solo se notifican a través del valor devuelto de D3DX12ParsePipelineStream; Esta estructura implementa las devoluciones de llamada de error para no hacer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





