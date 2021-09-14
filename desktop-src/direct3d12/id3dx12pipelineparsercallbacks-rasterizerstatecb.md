---
title: Método ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12.h)
description: Llama a la devolución de llamada del subobjeto de descripción del estado del rasterizador de un objeto que implementa esta interfaz.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Método RasterizerStateCb
- Método RasterizerStateCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966783"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>Método ID3DX12PipelineParserCallbacks::RasterizerStateCb

Llama a la devolución de llamada del subobjeto de descripción del estado del rasterizador de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RasterizerState* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Detalles del subobjeto de descripción del estado del rasterizador que se analiza desde una secuencia de estado de canalización.

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

[**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





