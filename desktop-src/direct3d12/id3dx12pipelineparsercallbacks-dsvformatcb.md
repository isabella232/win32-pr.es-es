---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) (DSV)
description: Llama a la devoluciones de llamada de subobjeto de formato de valor de estarcido de profundidad de un objeto que implementa esta interfaz.
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
ms.openlocfilehash: 7d26c13c70976c67bbe8d5910c4f3573010ff580
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105709282"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)

Llama a la devoluciones de llamada de subobjeto de formato de valor de estarcido de profundidad de un objeto que implementa esta interfaz.

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

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Detalles del subobjeto de formato de valor de estarcido de profundidad analizado desde una secuencia de estado de canalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No devuelve nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces auxiliares de Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**formato de DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

