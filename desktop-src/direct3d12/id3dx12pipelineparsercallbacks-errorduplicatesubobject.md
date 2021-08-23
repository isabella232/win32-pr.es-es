---
title: Método ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12.h)
description: Llama a la devolución de llamada de error del subobjeto duplicado de un objeto que implementa esta interfaz.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Método ErrorDuplicateSubobject
- Método ErrorDuplicateSubobject, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método ErrorDuplicateSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33724b1fdfec4951ce2efb31d4916ce210dc2b73858a5ef250c14a8744646bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045473"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>Método ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject

Llama a la devolución de llamada de error del subobjeto duplicado de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DuplicateType* 
</dt> <dd>

Tipo: TIPO DE SUBOBJETO DE ESTADO DE CANALIZACIÓN **[ **D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

Tipo de subobjeto duplicado.

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

[**TIPO DE SUBOBJETO DE ESTADO \_ \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

