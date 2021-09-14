---
title: Método Id3DX12PipelineParserCallbacks NodemaskCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto nodemask de un objeto que implementa esta interfaz.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Método NodemaskCb
- Método NodemaskCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966796"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>Método ID3DX12PipelineParserCallbacks::NodemaskCb

Llama a la devolución de llamada del subobjeto nodemask de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Máscara de nodo* 
</dt> <dd>

Tipo: **UINT**

Detalles del subobjeto nodemask que se analiza desde una secuencia de estado de canalización.

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
</dt> </dl>

 

 





