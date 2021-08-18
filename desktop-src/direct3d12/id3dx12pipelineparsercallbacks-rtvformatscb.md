---
title: Método ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.
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
ms.openlocfilehash: d826bd2c2f3c5f1c0783a4be2cba132e4874f5a54776c227590dd87f5365d347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045443"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>Método ID3DX12PipelineParserCallbacks::RTVFormatsCb

Llama a la devolución de llamada del subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RTVFormats* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ RT FORMAT \_ \_ ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Detalles del subobjeto de matriz de formato de destino de representación que se analiza desde una secuencia de estado de canalización.

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

[**MATRIZ DE FORMATO D3D12 \_ RT \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





