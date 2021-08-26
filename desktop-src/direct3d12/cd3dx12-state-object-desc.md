---
title: CD3DX12_STATE_OBJECT_DESC clase (D3dx12.h)
description: Clase central de los asistentes de creación de objetos de estado D3DX12, que son clases auxiliares para crear objetos de estado a través de un conjunto arbitrario de subobjetos.
keywords:
- CD3DX12_STATE_OBJECT_DESC clase
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813078"
---
# <a name="cd3dx12_state_object_desc-class"></a>CD3DX12_STATE_OBJECT_DESC clase

Clase central de los asistentes de creación de objetos de estado D3DX12, que son clases auxiliares para crear objetos de estado a través de un conjunto arbitrario de subobjetos.

## <a name="syntax"></a>Sintaxis

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>Miembros

`CD3DX12_STATE_OBJECT_DESC`

Constructor predeterminado. Crea una nueva instancia de inicializada de forma predeterminada de un **CD3DX12_STATE_OBJECT_DESC**.

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

Constructor que crea una nueva instancia de un **CD3DX12_STATE_OBJECT_DESC** inicializado con un tipo de subjobject correspondiente al valor del D3D12_STATE_OBJECT_TYPE [**pasado**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) a él.

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

Método que establece el tipo de subjobject en el valor del [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) pasado a él.

`operator const D3D12_STATE_OBJECT_DESC&`

Operador de conversión que devuelve una referencia a una [**constante D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) objeto que describe el objeto de estado.

`operator const D3D12_STATE_OBJECT_DESC*`

Operador de conversión que devuelve un puntero a una [**constante D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) objeto que describe el objeto de estado.

`CreateSubobject`

Plantilla de función que crea un asistente sububject cuya duración pertenece a esta clase.

El parámetro *de plantilla T* especifica el tipo del asistente de subjobject, por ejemplo, [CD3DX12_HIT_GROUP_SUBOBJECT](cd3dx12-hit-group-subobject.md).

## <a name="remarks"></a>Comentarios

Para usar los asistentes de creación de objetos de estado D3DX12, empiece por crear una instancia de un objeto CD3DX12_STATE_OBJECT_DESC y llame **a** su **función CreateSubobject** para crear subobjetos. Cada uno de los asistentes de subobjetos tiene métodos específicos de ese subobjeto para configurar su contenido.

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

Como alternativa, puede crear instancias explícitamente de los asistentes de subobjetos, como a través de variables locales, pasando el objeto de estado desc (que debe apuntar a él) en el constructor auxiliar (o llamar a `mySubobjectHelper.AddToStateObject(Collection1)` ).

En este escenario alternativo, debe mantener activo el subobjeto siempre que el objeto de estado al que está asociado esté activo; de lo contrario, sus referencias de puntero estarán obsoletas.

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vea también

* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
