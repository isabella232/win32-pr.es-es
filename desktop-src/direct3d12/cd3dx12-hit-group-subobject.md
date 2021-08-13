---
title: CD3DX12_HIT_GROUP_SUBOBJECT (D3dx12.h)
description: Clase auxiliar para crear un subobjeto de estado del grupo de impacto.
keywords:
- CD3DX12_HIT_GROUP_SUBOBJECT clase
topic_type:
- apiref
api_name:
- CD3DX12_HIT_GROUP_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 68b95f15c41fd46bfaeb58943720d3b657a3208d9a0276e9ab65fe7bd6087c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037388"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>CD3DX12_HIT_GROUP_SUBOBJECT clase

Clase auxiliar para crear un subobjeto de estado del grupo de impacto.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_HIT_GROUP_SUBOBJECT
{
    CD3DX12_HIT_GROUP_SUBOBJECT() noexcept;
    CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetHitGroupExport(LPCWSTR exportName);
    void SetHitGroupType(D3D12_HIT_GROUP_TYPE Type) noexcept;
    void SetAnyHitShaderImport(LPCWSTR importName);
    void SetClosestHitShaderImport(LPCWSTR importName);
    void SetIntersectionShaderImport(LPCWSTR importName);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator const D3D12_HIT_GROUP_DESC& () const noexcept { return m_Desc; }
};
```

## <a name="members"></a>Miembros

`CD3DX12_HIT_GROUP_SUBOBJECT`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_HIT_GROUP_SUBOBJECT**.

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_HIT_GROUP_SUBOBJECT** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto .

`SetHitGroupExport(LPCWSTR)`

Función para establecer el nombre del grupo de impacto.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Función para establecer un valor de la [enumeración D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) especifica el tipo del grupo de posicionamiento.

`SetAnyHitShaderImport(LPCWSTR)`

Función para establecer opcionalmente el nombre del sombreador de cualquier hit asociado al grupo de impactos.

`SetClosestHitShaderImport(LPCWSTR)`

Función para establecer opcionalmente el nombre del sombreador de número más cercano asociado al grupo de impactos.

`SetIntersectionShaderImport(LPCWSTR)`

Función para establecer opcionalmente el nombre del nombre opcional del sombreador de intersección asociado al grupo de impacto.

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una [constante D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator const D3D12_HIT_GROUP_DESC&`

Operador de conversión que devuelve una referencia a una [constante D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) objeto que describe el objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
