---
description: Carga la primera jerarquía de fotogramas desde un archivo. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Función D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003767"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>D3DXLoadMeshHierarchyFromX función)

Carga la primera jerarquía de fotogramas desde un archivo. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*MeshOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.

</dd> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.

</dd> <dt>

*pAlloc* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Puntero a una interfaz [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*pUserDataLoader* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interfaz proporcionada por la aplicación que permite cargar datos de usuario. Vea [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHierarchy* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Devuelve un puntero a la jerarquía de Marcos cargada. Vea [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Devuelve un puntero al controlador de animación correspondiente a la animación en el archivo. x. Se crea con pistas y eventos predeterminados. Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXLoadMeshHierarchyFromXW. De lo contrario, la llamada de función se resuelve como D3DXLoadMeshHierarchyFromXA.

Todas las mallas del archivo se contraen en una malla de salida. Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.

**D3DXLoadMeshHierarchyFromX** carga los datos de animación y la jerarquía de Marcos desde un archivo. x. Examina el archivo. x y crea una jerarquía de Marcos y un controlador de animación según el objeto derivado de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)que se le pasa a través de pAlloc. La carga de los datos requiere varios pasos de la siguiente manera:

1.  Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementando cada método. Controla cómo se asignan y liberan los fotogramas y las mallas.
2.  Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementando cada método. Si el archivo. x no tiene datos incrustados definidos por el usuario, o si no lo necesita, puede omitir esta parte.
3.  Cree un objeto de la clase [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) y, opcionalmente, de la clase LoadUserData. No es necesario llamar a los métodos de estos objetos.
4.  Llame a **D3DXLoadMeshHierarchyFromX**, pasando el objeto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) y el objeto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (o **null**) para crear la jerarquía de fotogramas y el controlador de animación. Todos los marcos y conjuntos de animaciones se registran automáticamente en el controlador de animación.

Durante la carga, se vuelve a llamar a [**CreateFrame**](id3dxallocatehierarchy--createframe.md) y [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) en cada fotograma para controlar la carga y la asignación del marco. La aplicación define estos métodos para controlar cómo se almacenan los marcos. Se vuelve a llamar a [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) y [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) en cada objeto Mesh para controlar la carga y la asignación de objetos Mesh. Se vuelve a llamar a [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) para cada objeto de nivel superior que no se carga mediante otros métodos.

Para liberar estos datos, llame a ID3DXAnimationController:: release para liberar los conjuntos de animaciones y [**D3DXFRAMEDestroy**](d3dxframedestroy.md), pasando el nodo raíz de la jerarquía de Marcos y un objeto de la clase [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) derivada. Se llamará a [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) y [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) para cada fotograma y objeto de malla en la jerarquía de fotogramas. La implementación de **DestroyFrame** debe liberar todo lo asignado por [**CreateFrame**](id3dxallocatehierarchy--createframe.md)y, igualmente, para los métodos de contenedor de malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
