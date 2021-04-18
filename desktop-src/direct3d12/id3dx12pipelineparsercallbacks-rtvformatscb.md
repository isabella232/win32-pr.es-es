---
title: Método ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Método RTVFormatsCb
- Método RTVFormatsCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718334"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>ID3DX12PipelineParserCallbacks:: RTVFormatsCb (método)

Llama a la devolución de llamada de subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RTVFormats* \[ CLI\]
</dt> <dd>

Type: **const [**D3D12 \_ RT \_ format \_ array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Detalles del subobjeto de matriz de formato de destino de representación analizado desde una secuencia de estado de canalización.

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

[**\_Matriz de \_ formato D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





