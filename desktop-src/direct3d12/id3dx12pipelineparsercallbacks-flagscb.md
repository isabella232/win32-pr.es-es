---
title: Método ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto flags de un objeto que implementa esta interfaz.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Método FlagsCb
- Método FlagsCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718345"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>ID3DX12PipelineParserCallbacks:: FlagsCb (método)

Llama a la devolución de llamada del subobjeto flags de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* 
</dt> <dd>

Tipo: **[ **\_ marcas de \_ estado \_ de canalización de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Detalles del subobjeto Flags analizado desde una secuencia de estado de canalización.

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

[**\_Marcas de estado de canalización de D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





