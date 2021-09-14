---
title: Método Id3DX12PipelineParserCallbacks StreamOutputCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto de descripción de salida de secuencia de un objeto que implementa esta interfaz.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Método StreamOutputCb
- Método StreamOutputCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126971003"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>Método ID3DX12PipelineParserCallbacks::StreamOutputCb

Llama a la devolución de llamada del subobjeto de descripción de salida de secuencia de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StreamOutput* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ STREAM OUTPUT \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Detalles del subobjeto de descripción de salida de la secuencia analizada desde una secuencia de estado de canalización.

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

[**D3D12 \_ STREAM \_ OUTPUT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





