---
title: Función D3DX12ParsePipelineStream (D3dx12. h)
description: Analiza una descripción de flujo de estado de canalización, que llama a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream función)
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721436"
---
# <a name="d3dx12parsepipelinestream-function"></a>D3DX12ParsePipelineStream función)

Analiza una descripción de flujo de estado de canalización, que llama a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DESC* \[ . CLI\]
</dt> <dd>

Tipo: **const [**D3D12 de la secuencia de \_ \_ estado \_ \_ de canalización**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

La descripción del flujo de estado de la canalización que se va a analizar.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Estructura que especifica las devoluciones de llamada que se van a llamar para cada tipo de subobjeto y devoluciones de llamada adicionales que se van a llamar en caso de un error de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método devuelve un error HRESULT Success (**S \_ OK** o **E \_ INVALIDARG** ) si se encuentra un tipo de subobjeto desconocido, si la descripción del flujo está vacía, es null o contiene subobjetos duplicados (incluidos los subobjetos derivados) o si *pCallbacks* es NULL. En cada caso en \_ el que se devuelve E INVALIDARG, primero se llama a una devolución de llamada correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





