---
title: Método ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de diseño de entrada de un objeto que implementa esta interfaz.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Método InputLayoutCb
- Método InputLayoutCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718337"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>ID3DX12PipelineParserCallbacks:: InputLayoutCb (método)

Llama a la devolución de llamada de subobjeto de diseño de entrada de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InputLayout* \[ CLI\]
</dt> <dd>

Tipo: **const [**D3D12 \_ diseño de entrada \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Detalles del subobjeto de diseño de entrada analizado desde una secuencia de estado de canalización.

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

[**\_Descripción del \_ diseño de entrada de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





