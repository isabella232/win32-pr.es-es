---
title: Método ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto de descripción de ejemplo de un objeto que implementa esta interfaz.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Método SampleDescCb
- Método SampleDescCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966795"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>Método ID3DX12PipelineParserCallbacks::SampleDescCb

Llama a la devolución de llamada del subobjeto de descripción de ejemplo de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SampleDesc* \[ Ref\]
</dt> <dd>

Tipo: **const [**DXGI \_ SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**

Detalles del subobjeto de descripción de ejemplo que se analiza desde una secuencia de estado de canalización.

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
</dt> <dt>

[**\_ \_ DESC DESC DE EJEMPLO DE DXGI**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

