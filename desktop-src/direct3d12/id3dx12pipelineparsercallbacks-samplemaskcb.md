---
title: Método ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Llama a la devoluciones de llamada de subobjeto de la máscara de ejemplo de un objeto que implementa esta interfaz.
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
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717577"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>ID3DX12PipelineParserCallbacks:: SampleMaskCb (método)

Llama a la devoluciones de llamada de subobjeto de la máscara de ejemplo de un objeto que implementa esta interfaz.

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

Tipo: **uint**

Detalles del subobjeto de máscara de ejemplo analizado desde una secuencia de estado de canalización.

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
</dt> </dl>

 

 





