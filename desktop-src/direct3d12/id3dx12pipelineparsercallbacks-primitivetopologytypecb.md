---
title: Método Id3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12.h)
description: Llama a la devolución de llamada de subobjeto de tipo de topología primitiva de un objeto que implementa esta interfaz.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Método PrimitiveTopologyTypeCb
- Método PrimitiveTopologyTypeCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966792"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>Método ID3DX12PipelineParserCallbacks::P rimitiveTopologyTypeCb

Llama a la devolución de llamada de subobjeto de tipo de topología primitiva de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PrimitiveTopologyType* 
</dt> <dd>

Tipo: **[ **TIPO DE TOPOLOGÍA \_ PRIMITIVA \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Detalles del subobjeto de tipo de topología primitivo que se analiza desde una secuencia de estado de canalización.

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

[**TIPO DE TOPOLOGÍA PRIMITIVA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





