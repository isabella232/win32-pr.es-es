---
title: Método ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto mask de ejemplo de un objeto que implementa esta interfaz.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Método SampleMaskCb
- Método SampleMaskCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64acc7e969f52e78250cde9bc4c693ce3eae06ae3edd08e7f18c65dc0ff6fa8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069595"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>Método ID3DX12PipelineParserCallbacks::SampleMaskCb

Llama a la devolución de llamada del subobjeto mask de ejemplo de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SampleMask* 
</dt> <dd>

Tipo: **UINT**

Detalles del subobjeto de máscara de ejemplo que se analiza desde una secuencia de estado de canalización.

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
</dt> </dl>

 

 





