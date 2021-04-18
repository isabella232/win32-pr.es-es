---
title: Método ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Llama a la devolución de llamada de error de parámetro de entrada incorrecto de un objeto que implementa esta interfaz.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Método ErrorBadInputParameter
- Método ErrorBadInputParameter, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718350"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a>ID3DX12PipelineParserCallbacks:: ErrorBadInputParameter (método)

Llama a la devolución de llamada de error de parámetro de entrada incorrecto de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ParameterIndex* 
</dt> <dd>

Tipo: **uint**

La posición del parámetro que contiene una entrada incorrecta. El parámetro situado más a la izquierda está en la posición 1, no en la posición 0.

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

 

 





