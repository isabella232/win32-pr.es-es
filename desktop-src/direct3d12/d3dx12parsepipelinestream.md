---
title: Función D3DX12ParsePipelineStream (D3dx12.h)
description: Analiza una descripción de flujo de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.
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
ms.openlocfilehash: cbdd472d118a5ec9d49c5f105ee6b8e8ef2e3ea540f6f1954bad17273e9e030f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608565"
---
# <a name="d3dx12parsepipelinestream-function"></a>Función D3DX12ParsePipelineStream

Analiza una descripción de flujo de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.

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

Estructura que especifica las devoluciones de llamada a las que se debe llamar para cada tipo de subobjeto y las devoluciones de llamada adicionales que se llamarán en caso de error de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método devuelve un error HRESULT correcto (S **\_ OK** o **E \_ INVALIDARG** si se encuentra un tipo de subobjeto desconocido, si la descripción de la secuencia está vacía, null o contiene subobjetos duplicados (incluidos los subobjetos derivados) o si *pCallbacks* es NULL. En cada caso en que se devuelve E \_ INVALIDARG, se llama primero a una devolución de llamada correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





