---
title: Método ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto depth stencil state (D3D12 \_ DEPTH \_ STENCIL DESC1) de un objeto que \_ implementa esta interfaz.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Método DepthStencilState1Cb
- Método DepthStencilState1Cb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966807"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a>Método ID3DX12PipelineParserCallbacks::D epthStencilState1Cb

Llama a la devolución de llamada del subobjeto depth [**stencil DESC1 (D3D12 \_ DEPTH \_ STENCIL \_ DESC1)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DepthStencilState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**

Detalles del subobjeto de estado de galería de símbolos de profundidad que se analiza desde una secuencia de estado de canalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No devuelve nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





