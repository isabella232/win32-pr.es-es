---
title: CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT (D3dx12.h)
description: Clase auxiliar para crear un subobjeto de estado de asociación de subobjeto a exportaciones.
keywords:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT clase
topic_type:
- apiref
api_name:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 23a0bfe1afff461e5d6b8ba69bedd6ade9069904
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568429"
---
# <a name="cd3dx12_subobject_to_exports_association_subobject-class"></a>CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT clase

Clase auxiliar para crear un subobjeto de estado de asociación de subobjeto a exportaciones.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
{
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT() noexcept;
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT& SubobjectToAssociate) noexcept;
    void AddExport(LPCWSTR Export);
    template<size_t N> void AddExports(LPCWSTR(&Exports)[N]);
    void AddExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**.

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto .

`SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT&)`

Función para establecer el subobjeto que se asociará en forma de [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) pasado como parámetro .

`AddExport(LPCWSTR)`

Agrega una exportación para asociar.

`AddExports(LPCWSTR(&)[N]);`

Agrega una matriz de exportaciones para asociar. El parámetro *de plantilla N* especifica el número de elementos de la matriz.

`AddExports(const LPCWSTR*, UINT)`

Define una matriz de *N exportaciones* que se asociará.

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una [constante D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION&`

Operador de conversión que devuelve una referencia a una [constante D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ns-d3d12-d3d12_subobject_to_exports_association) objeto que describe el objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
