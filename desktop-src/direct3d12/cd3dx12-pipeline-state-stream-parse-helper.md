---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER estructura (D3dx12. h)
description: Compila un \_ \_ \_ objeto de flujo de estado de canalización CD3DX12 interno a partir de los detalles de subobjeto pasados a las funciones miembro correspondientes. Este struct implementa la interfaz ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698192"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>\_Estructura de \_ la \_ \_ \_ aplicación auxiliar de análisis de flujo de estado de canalización CD3DX12

Compila un \_ \_ \_ objeto de flujo de estado de canalización CD3DX12 interno a partir de los detalles de subobjeto pasados a las funciones miembro correspondientes. Este struct implementa la interfaz [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**PipelineStream**
</dt> <dd>

El estado interno de la [**\_ canalización de CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Su estado actual representa el efecto acumulativo de los métodos de devolución de llamada a los que se ha llamado en este objeto.

</dd> <dt>

**FlagsCb (D3D12 \_ marcas de marcas de estado de canalización \_ \_ )**
</dt> <dd>

Inicializa el miembro **Flags** de **PipelineStream** con el valor del parámetro *Flags* .

</dd> <dt>

**NodeMaskCb (UINT NodeMask)**
</dt> <dd>

Inicializa el miembro **NodeMask** de **PipelineStream** con el valor del parámetro *NodeMask* .

</dd> <dt>

**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Inicializa el miembro **pRootSignature** de **PipelineStream** con el valor del parámetro *pRootSignature* .

</dd> <dt>

**InputLayoutCb (D3D12 de \_ diseño de entrada const \_ \_& InputLayout)**
</dt> <dd>

Inicializa el miembro **InputLayout** de **PipelineStream** con el valor del parámetro *InputLayout* .

</dd> <dt>

**IBStripCutValueCb (D3D12 \_ valor de corte de la \_ franja del búfer de índice \_ \_ \_ IBStripCutValue)**
</dt> <dd>

Inicializa el miembro **IBStripCutValue** de **PipelineStream** con el valor del parámetro *IBStripCutValue* .

</dd> <dt>

**PrimitiveTopologyTypeCb ( \_ tipo de \_ topología primitiva D3D12 \_ PrimitiveTopologyType)**
</dt> <dd>

Inicializa el miembro **PrimitiveTopologyType** de **PipelineStream** con el valor del parámetro *PrimitiveTopologyType* .

</dd> <dt>

**VSCb (D3D12 de \_ código de byte del sombreador const \_& vs)**
</dt> <dd>

Inicializa el miembro de **vs** (sombreador de vértices) de **PipelineStream** con el valor del parámetro de *vs* .

</dd> <dt>

**GSCb (código de \_ bytes del sombreador const D3D12 \_& GS)**
</dt> <dd>

Inicializa el miembro **GS** (sombreador de geometría) de **PipelineStream** con el valor del parámetro *GS* .

</dd> <dt>

**StreamOutputCb (D3D12 de \_ salida de flujo const \_ \_& StreamOutput)**
</dt> <dd>

Inicializa el miembro **StreamOutput** de **PipelineStream** con el valor del parámetro *StreamOutput* .

</dd> <dt>

**HSCb (D3D12 de \_ código de \_ byte del sombreador const& HS)**
</dt> <dd>

Inicializa el miembro **HS** (sombreador de casco) de **PipelineStream** con el valor del parámetro *HS* .

</dd> <dt>

**DSCb (D3D12 de \_ código de \_ byte del sombreador const& DS)**
</dt> <dd>

Inicializa el miembro **DS** (sombreador de dominios) de **PipelineStream** con el valor del parámetro *DS* .

</dd> <dt>

**PSCb (el \_ código de bytes del sombreador const D3D12 \_& PS)**
</dt> <dd>

Inicializa el miembro **PS** (sombreador de píxeles) de **PipelineStream** con el valor del parámetro *PS* .

</dd> <dt>

**CSCb (constante de \_ bytes de sombreador const D3D12 \_& CS)**
</dt> <dd>

Inicializa el miembro **CS** de **PipelineStream** con el valor del parámetro *CS* .

</dd> <dt>

**BlendStateCb (const D3D12 \_ BLEND \_& BlendState)**
</dt> <dd>

Inicializa el miembro **BlendState** de **PipelineStream** con el valor del parámetro *BlendState* .

</dd> <dt>

**DepthStencilStateCb (const D3D12 \_ Depth \_ estarcido \_ DESC& DepthStencilState)**
</dt> <dd>

Inicializa el miembro **DepthStencilState** de **PipelineStream** con el valor del parámetro *DepthStencilState* , una descripción de [**la \_ Galería \_ de \_ símbolos de profundidad D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb (const D3D12 \_ Depth \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Inicializa el miembro **DepthStencilState** de **PipelineStream** con el valor del parámetro *DepthStencilState* , una galería de [**símbolos de \_ profundidad D3D12 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**DSVFormatCb (formato de DXGI \_ DSVFormat)**
</dt> <dd>

Inicializa el miembro **DSVFormat** de **PipelineStream** con el valor del parámetro *DSVFormat* .

</dd> <dt>

**RasterizerStateCb (const D3D12 \_ rasterizador \_ DESC& RasterizerState)**
</dt> <dd>

Inicializa el miembro **RasterizerState** de **PipelineStream** con el valor del parámetro *RasterizerState* .

</dd> <dt>

**RTVFormatsCb (matriz de \_ formato const D3D12 RT \_ \_& RTVFormats)**
</dt> <dd>

Inicializa el miembro **RTVFormats** de **PipelineStream** con el valor del parámetro *RTVFormats* .

</dd> <dt>

**SampleDescCb (ejemplo const de DXGI \_ \_& SampleDesc)**
</dt> <dd>

Inicializa el miembro **SampleDesc** de **PipelineStream** con el valor del parámetro *SampleDesc* .

</dd> <dt>

**SampleMaskCb (UINT SampleMask)**
</dt> <dd>

Inicializa el miembro **SampleMask** de **PipelineStream** con el valor del parámetro *SampleMask* .

</dd> <dt>

**ViewInstancingCb (const D3D12 \_ View \_ INSTANCING \_ DESC& ViewInstancingDesc)**
</dt> <dd>

Inicializa el miembro **ViewInstancingDesc** de **PipelineStream** con el valor del parámetro *ViewInstancingDesc* .

</dd> <dt>

**CachedPSOCb (const D3D12 \_ Estado de \_ canalización en caché \_& CachedPSO)**
</dt> <dd>

Inicializa el miembro **CachedPSO** de **PipelineStream** con el valor del parámetro *CachedPSO* .

</dd> <dt>

**ErrorBadInputParameter (UINT)**
</dt> <dd>

No hace nada.

</dd> <dt>

**ErrorDuplicateSubobject ( \_ tipo de \_ subobjeto de estado de canalización D3D12 \_ \_ )**
</dt> <dd>

No hace nada.

</dd> <dt>

**ErrorUnknownSubobject (UINT)**
</dt> <dd>

No hace nada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se pasa como el segundo parámetro a la función [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , los detalles del objeto [**\_ STREAM1 de \_ estado \_ de canalización CD3DX12**](cd3dx12-pipeline-state-stream1.md) interno se clonan desde la [**DESC de flujo de \_ Estado de canalización \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) pasada como primer parámetro. Este proceso valida la descripción del flujo de origen. Si D3DX12ParsePipelineStream devuelve **S \_ OK**, la descripción de la secuencia de origen y el **\_ Estado de canalización CD3DX12 resultante \_ \_ STREAM1PipelineStream** son válidos; de lo contrario, ambos no son válidos. Los flujos no válidos y otros errores solo se muestran a través del valor devuelto de D3DX12ParsePipelineStream; Esta estructura implementa las devoluciones de llamada de error para no hacer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





