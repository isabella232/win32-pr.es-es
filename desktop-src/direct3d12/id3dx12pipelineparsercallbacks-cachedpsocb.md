---
title: Método ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto PSO (objeto de estado de canalización) almacenada en caché de un objeto que implementa esta interfaz.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Método CachedPSOCb
- Método CachedPSOCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707980"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>ID3DX12PipelineParserCallbacks:: CachedPSOCb (método)

Llama a la devolución de llamada del subobjeto PSO (objeto de estado de canalización) almacenada en caché de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CachedPSO* \[ CLI\]
</dt> <dd>

Tipo: **const [**D3D12 \_ Estado de \_ la \_ canalización en caché**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Detalles del subobjeto PSO (objeto de estado de canalización) almacenado en caché analizado desde una secuencia de estado de canalización.

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

[**D3D12 \_ Estado de \_ canalización en caché \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





