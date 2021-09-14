---
title: CD3DX12_DXIL_LIBRARY_SUBOBJECT (D3dx12.h)
description: Clase auxiliar para crear un subobjeto de estado de biblioteca DXIL.
keywords:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT clase
topic_type:
- apiref
api_name:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 33ec22dd722469ce131bc58d5aca83f0aed4edf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966860"
---
# <a name="cd3dx12_dxil_library_subobject-class"></a>CD3DX12_DXIL_LIBRARY_SUBOBJECT clase

Clase auxiliar para crear un subobjeto de estado de biblioteca DXIL.

Para obtener más información sobre los asistentes de creación de objetos de estado D3DX12, [vea CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_DXIL_LIBRARY_SUBOBJECT
{
    CD3DX12_DXIL_LIBRARY_SUBOBJECT() noexcept;
    CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    void SetDXILLibrary(const D3D12_SHADER_BYTECODE* pCode) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_DXIL_LIBRARY_DESC& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_DXIL_LIBRARY_SUBOBJECT`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_DXIL_LIBRARY_SUBOBJECT**.

`CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_DXIL_LIBRARY_SUBOBJECT** inicializado con el contenido de un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto.

`SetDXILLibrary(const D3D12_SHADER_BYTECODE*)`

Función para establecer la biblioteca DXIL en forma del puntero a un [D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) pasado como parámetro .

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Define un símbolo exportado desde el subobjeto. Toma un [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) como parámetro opcional.

`DefineExports(LPCWSTR(&)[N]);`

Define una matriz de *N* símbolos exportados desde el subobjeto. El parámetro *de plantilla N* especifica el número de elementos de la matriz.

`DefineExports(const LPCWSTR*, UINT)`

Define una matriz de símbolos exportados desde el subobjeto.

`Type`

Recupera el tipo del subobjeto, representado por la [D3D12_STATE_SUBOBJECT_TYPE_DXIL_LIBRARY](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversión que devuelve una referencia a una [**constante D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que describe el objeto de estado.

`operator const D3D12_DXIL_LIBRARY_DESC&`

Operador de conversión que devuelve una referencia a una [**constante D3D12_DXIL_LIBRARY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_library_desc) objeto que describe el objeto de estado.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
