---
title: CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT (D3dx12.h)
description: Clase auxiliar para crear un suboject de estado de firma raíz local.
keywords:
- CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT clase
topic_type:
- apiref
api_name:
- CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 85aee6a1697bdbcf01a741437da076f705731947
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813063"
---
# <a name="cd3dx12_local_root_signature_subobject-class"></a>CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT clase

Clase auxiliar para crear un suboject de estado de firma raíz local.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT
{
    CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT() noexcept;
    CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetRootSignature(ID3D12RootSignature* pRootSig) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator ID3D12RootSignature* () const noexcept { return D3DX12_COM_PTR_GET(m_pRootSig); }
};
```

## <a name="members"></a>Miembros

`CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**.

`CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto .

`SetRootSignature(ID3D12RootSignature*)`

Función para establecer la firma raíz en forma del puntero a [un ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) pasado como parámetro.

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una [constante D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator ID3D12RootSignature*`

Operador de conversión que devuelve la firma raíz en forma de puntero a [id3D12RootSignature.](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
