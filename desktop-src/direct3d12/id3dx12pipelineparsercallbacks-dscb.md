---
title: Método DSCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto del sombreador de dominio de un objeto que implementa esta interfaz.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Método DSCb
- Método DSCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método DSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c4cee98bf617fb02cb5c543050f51c56a733d56964e2139e5b7357c7a88034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528993"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a>Id3DX12PipelineParserCallbacks::D SCb (método)

Llama a la devolución de llamada del subobjeto del sombreador de dominio de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DS* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Detalles del subobjeto del sombreador de dominio que se analiza desde una secuencia de estado de canalización.

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

[**CÓDIGO DE BYTES DEL SOMBREADOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





