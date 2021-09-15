---
title: CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING estructura (D3dx12.h)
description: Estructura auxiliar que se usa para encapsular [una CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) estructura. Permite que los sombreadores se representen en varias vistas con una sola llamada a draw; útil para la visión estéreo o la generación de mapas de cubo.
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: b693130bab6d090379d253d07ce4bbaa5c88b150
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569980"
---
# <a name="cd3dx12_pipeline_state_stream_view_instancing-structure"></a>CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING estructura

Estructura auxiliar que se usa para encapsular [una CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) estructura. Permite que los sombreadores se representen en varias vistas con una sola llamada a draw; útil para la visión estéreo o la generación de mapas de cubo.

## <a name="syntax"></a>Sintaxis

```cpp
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_VIEW_INSTANCING_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VIEW_INSTANCING, CD3DX12_DEFAULT> CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING;
```

**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING** es una `typedef` especialización de la [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) plantilla.

## <a name="members"></a>Members

Vea [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) y [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md).

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md)
* [D3D12_PIPELINE_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
