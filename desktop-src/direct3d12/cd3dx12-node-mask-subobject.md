---
title: CD3DX12_NODE_MASK_SUBOBJECT (D3dx12.h)
description: Clase auxiliar para crear un subobjeto de estado que identifica los nodos de GPU a los que se aplica el objeto de estado.
keywords:
- CD3DX12_NODE_MASK_SUBOBJECT clase
topic_type:
- apiref
api_name:
- CD3DX12_NODE_MASK_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: bfa1c5ce1facb946b060bf7501c09c6c13cfca13
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812905"
---
# <a name="cd3dx12_node_mask_subobject-class"></a>CD3DX12_NODE_MASK_SUBOBJECT clase

Clase auxiliar para crear un subobjeto de estado que identifica los nodos de GPU a los que se aplica el objeto de estado.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_NODE_MASK_SUBOBJECT
{
    CD3DX12_NODE_MASK_SUBOBJECT() noexcept;
    CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetNodeMask(UINT NodeMask) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_NODE_MASK& () const noexcept;
};
```

## <a name="members"></a>Miembros

`CD3DX12_NODE_MASK_SUBOBJECT`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_NODE_MASK_SUBOBJECT**.

`CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_NODE_MASK_SUBOBJECT** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto .

`SetNodeMask(UINT)`

Función para establecer la máscara de nodo.

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_NODE_MASK](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator const D3D12_NODE_MASK&`

Operador de conversión que devuelve una referencia a una [constante D3D12_NODE_MASK](/windows/win32/api/d3d12/ns-d3d12-d3d12_node_mask) objeto que describe el objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
