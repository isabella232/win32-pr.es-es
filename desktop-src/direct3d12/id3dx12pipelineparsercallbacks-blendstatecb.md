---
title: Método ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto blend state description de un objeto que implementa esta interfaz.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Método BlendStateCb
- Método BlendStateCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método BlendStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966815"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>Método ID3DX12PipelineParserCallbacks::BlendStateCb

Llama a la devolución de llamada del subobjeto blend state description de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BlendState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Detalles del subobjeto blend state description que se analiza desde una secuencia de estado de canalización.

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

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





