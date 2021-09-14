---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12.h) (DSV)
description: Llama a la devolución de llamada del subobjeto depth stencil value format de un objeto que implementa esta interfaz.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
keywords:
- Método DepthStencilStateCb
- Método DepthStencilStateCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060797"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a>Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12.h) para el valor de galería de símbolos de profundidad

Llama a la devolución de llamada del subobjeto depth stencil value format de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DepthStencilState* 
</dt> <dd>

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Detalles del subobjeto de formato de valor de galería de símbolos de profundidad que se analiza desde una secuencia de estado de canalización.

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

[**FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

