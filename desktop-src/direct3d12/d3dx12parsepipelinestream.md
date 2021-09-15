---
title: Función D3DX12ParsePipelineStream (D3dx12.h)
description: Analiza la descripción de una secuencia de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- Función D3DX12ParsePipelineStream
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570881"
---
# <a name="d3dx12parsepipelinestream-function"></a>Función D3DX12ParsePipelineStream

Analiza la descripción de una secuencia de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Desc* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ PIPELINE STATE STREAM \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Descripción de la secuencia de estado de canalización que se analizará.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Estructura que especifica las devoluciones de llamada a las que se llamará para cada tipo de subobjeto y las devoluciones de llamada adicionales que se llamarán en caso de error de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método devuelve un error HRESULT correcto (S **\_ OK** o **E \_ INVALIDARG** si se encuentra un tipo de subobjeto desconocido, si la descripción de la secuencia está vacía, es null o contiene subobjetos duplicados (incluidos los subobjetos derivados) o si *pCallbacks* es NULL. En cada caso en que se devuelve E INVALIDARG, primero se llama \_ a una devolución de llamada correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





