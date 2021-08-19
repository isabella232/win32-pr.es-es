---
title: Método PSCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto sombreador de píxeles de un objeto que implementa esta interfaz.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Método PSCb
- Método PSCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método PSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c15b09598218259d5cdeedfb3453aaf2a4f669242ddb76e676093e81e0dd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894575"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a>Id3DX12PipelineParserCallbacks::P SCb

Llama a la devolución de llamada del subobjeto sombreador de píxeles de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PS* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Detalles del subobjeto de sombreador de píxeles que se analiza desde una secuencia de estado de canalización.

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

[**CÓDIGO DE BYTES DEL SOMBREADOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





