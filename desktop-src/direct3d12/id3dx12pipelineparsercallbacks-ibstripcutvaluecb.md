---
title: Método ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto index buffer strip-cut value de un objeto que implementa esta interfaz.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Método IBStripCutValueCb
- Método IBStripCutValueCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdbbe2d66ae38a3bcd04ee84e6db15841d8f74a3b0d311552a51a892445b38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124073"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>Método ID3DX12PipelineParserCallbacks::IBStripCutValueCb

Llama a la devolución de llamada del subobjeto index buffer strip-cut value de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IBStripCutValue* 
</dt> <dd>

Tipo: **[ **D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Detalles del subobjeto index buffer strip-cut value analizada desde una secuencia de estado de canalización.

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

[**VALOR DE CORTE DE FRANJA DE \_ \_ BÚFER DE \_ \_ ÍNDICE \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





