---
title: CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION (D3dx12.h)
description: Clase auxiliar para crear un subobjeto de estado de asociación DXIL-subobject-to-exports.
keywords:
- CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION clase
topic_type:
- apiref
api_name:
- CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 84d8ae4ab76845d2e188d4be41e57b7770dfe89c
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813309"
---
# <a name="cd3dx12_dxil_subobject_to_exports_association-class"></a>CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION clase

Clase auxiliar para crear un subobjeto de estado de asociación DXIL-subobject-to-exports.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
{
    CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION() noexcept;
    CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetSubobjectNameToAssociate(LPCWSTR SubobjectToAssociate);
    void AddExport(LPCWSTR Export);
    template<size_t N> void AddExports(LPCWSTR(&Exports)[N]);
    void AddExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION& () const noexcept;
};
```

## <a name="members"></a>Miembros

`CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**.

`CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto.

`SetSubobjectNameToAssociate(LPCWSTR)`

Función para establecer el nombre del subobjeto que se asociará.

`AddExport(LPCWSTR)`

Agrega una exportación que se asociará.

`AddExports(LPCWSTR(&)[N]);`

Agrega una matriz de exportaciones que se asociará. El parámetro *de plantilla N* especifica el número de elementos de la matriz.

`AddExports(const LPCWSTR*, UINT)`

Define una matriz de *N exportaciones* que se asocian.

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una [constante D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION&`

Operador de conversión que devuelve una referencia a una [constante D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) objeto que describe el objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
