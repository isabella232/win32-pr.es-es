---
title: Método ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718336"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>ID3DX12PipelineParserCallbacks::P método rimitiveTopologyTypeCb

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

Tipo: **[ **\_ \_ \_ tipo de topología primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Detalles del subobjeto de tipo de topología primitiva analizado desde una secuencia de estado de canalización.

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

[**\_Tipo de \_ topología primitiva \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





