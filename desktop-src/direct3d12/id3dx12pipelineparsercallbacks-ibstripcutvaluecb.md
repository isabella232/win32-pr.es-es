---
title: Método ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de valor de corte de franja del búfer de índice de un objeto que implementa esta interfaz.
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
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718340"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>ID3DX12PipelineParserCallbacks:: IBStripCutValueCb (método)

Llama a la devolución de llamada de subobjeto de valor de corte de franja del búfer de índice de un objeto que implementa esta interfaz.

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

Tipo: **[ **\_ valor de \_ \_ corte de \_ \_ franja de búfer de índice de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Detalles del subobjeto de valor de corte de franja del búfer de índice analizado desde una secuencia de estado de canalización.

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

[**D3D12 \_ \_ valor de \_ corte de franja de búfer de \_ Índice \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





