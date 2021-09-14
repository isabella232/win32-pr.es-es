---
title: CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT (D3dx12.h)
description: Clase auxiliar para crear un subobjeto que define las propiedades generales de un objeto de estado.
keywords:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT clase
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 952bf1cd1b2833a4e4a2bf0a91892fbb1d6f797c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966855"
---
# <a name="cd3dx12_state_object_config_subobject-class"></a>CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT clase

Clase auxiliar para crear un subobjeto que define las propiedades generales de un objeto de estado.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
{
public:
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetFlags(D3D12_STATE_OBJECT_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_STATE_OBJECT_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**.

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto.

`SetFlags(D3D12_STATE_OBJECT_FLAGS)`

Función para especificar los requisitos del objeto de estado a través [de un D3D12_STATE_OBJECT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_flags) objeto .

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una [constante D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator const D3D12_STATE_OBJECT_CONFIG&`

Operador de conversión que devuelve una referencia a una [constante D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) objeto que describe el objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
