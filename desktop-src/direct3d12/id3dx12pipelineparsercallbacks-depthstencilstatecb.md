---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12.h)
description: Llama a la devolución de llamada de subobjeto de estado de galería de símbolos de profundidad de un objeto que implementa esta interfaz.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
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
ms.openlocfilehash: a1086156fcaa6b8736c049c93bacc5dfd1f5e915ba8a7006b3c71e654ba65f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894585"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12.h)

Llama a la devolución de llamada de subobjeto de estado de galería de símbolos de profundidad de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DepthStencilState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





