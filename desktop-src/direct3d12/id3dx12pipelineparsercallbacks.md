---
title: Interfaz ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Interfaz que representa una colección de devoluciones de llamada de error y analizador que usa la función auxiliar D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, descrita
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474474"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>Interfaz ID3DX12PipelineParserCallbacks

Interfaz que representa una colección de devoluciones de llamada de error y analizador que usa la función auxiliar [**D3DX12parsePipelineStream.**](d3dx12parsepipelinestream.md)

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX12PipelineParserCallbacks** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Llama a la devolución de llamada del subobjeto blend state description de un objeto que implementa esta interfaz.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Llama a la devolución de llamada del subobjeto PSO (objeto de estado de canalización) almacenado en caché de un objeto que implementa esta interfaz.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Llama a la devolución de llamada del subobjeto del sombreador de proceso de un objeto que implementa esta interfaz.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Llama a la devolución de llamada del subobjeto depth [**stencil DESC1 (D3D12 \_ DEPTH \_ STENCIL \_ DESC1)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)de un objeto que implementa esta interfaz.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Llama a la devolución de llamada del subobjeto depth stencil value format de un objeto que implementa esta interfaz.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Llama a la devolución de llamada de subobjeto de estado de galería de símbolos de profundidad de un objeto que implementa esta interfaz.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Llama a la devolución de llamada del subobjeto del sombreador de dominio de un objeto que implementa esta interfaz.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Llama a la devolución de llamada de error del parámetro de entrada no válido de un objeto que implementa esta interfaz.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Llama a la devolución de llamada de error del subobjeto duplicado de un objeto que implementa esta interfaz.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Llama a la devolución de llamada de error del subobjeto desconocido de un objeto que implementa esta interfaz.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Llama a la devolución de llamada del subobjeto flags de un objeto que implementa esta interfaz.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Llama a la devolución de llamada del subobjeto del sombreador geometry de un objeto que implementa esta interfaz.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Llama a la devolución de llamada del subobjeto del sombreador de casco de un objeto que implementa esta interfaz.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Llama a la devolución de llamada del subobjeto index buffer strip-cut value de un objeto que implementa esta interfaz.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Llama a la devolución de llamada del subobjeto de diseño de entrada de un objeto que implementa esta interfaz.<br/>                                                                            |
| [**Máscara de nodoCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Llama a la devolución de llamada del subobjeto nodemask de un objeto que implementa esta interfaz.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Llama a la devolución de llamada de subobjeto de tipo de topología primitiva de un objeto que implementa esta interfaz.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Llama a la devolución de llamada del subobjeto del sombreador de píxeles de un objeto que implementa esta interfaz.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Llama a la devolución de llamada del subobjeto de descripción de estado del rasterizador de un objeto que implementa esta interfaz.<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Llama a la devolución de llamada del subobjeto de firma raíz de un objeto que implementa esta interfaz.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Llama a la devolución de llamada del subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Llama a la devolución de llamada del subobjeto de descripción de ejemplo de un objeto que implementa esta interfaz.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Llama a la devolución de llamada del subobjeto mask de ejemplo de un objeto que implementa esta interfaz.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Llama a la devolución de llamada del subobjeto de descripción de salida de secuencia de un objeto que implementa esta interfaz.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Llama a la devolución de llamada del subobjeto del sombreador de vértices de un objeto que implementa esta interfaz.<br/>                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





