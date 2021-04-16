---
title: Método ID3DX12PipelineParserCallbacks CSCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto del sombreador de cálculo de un objeto que implementa esta interfaz.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Método CSCb
- Método CSCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método CSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707979"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a>ID3DX12PipelineParserCallbacks:: CSCb (método)

Llama a la devolución de llamada de subobjeto del sombreador de cálculo de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CS* \[ CLI\]
</dt> <dd>

Tipo: **const [**D3D12 \_ código de \_ byte del sombreador**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Detalles del subobjeto del sombreador de cálculo analizado desde una secuencia de estado de canalización.

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

[**\_Código de bytes del sombreador D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





