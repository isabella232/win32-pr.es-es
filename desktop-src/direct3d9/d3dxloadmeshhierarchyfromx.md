---
description: 'Función D3DXLoadMeshHierarchyFromX: carga la primera jerarquía de fotogramas desde un archivo .x.'
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Función D3DXLoadMeshHierarchyFromX (D3dx9anim.h)
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
ms.openlocfilehash: 81a087156de61f7997b5d755eb45c0c7e7736fd2345c219b22e8b642ea44e9dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460375"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>Función D3DXLoadMeshHierarchyFromX

Carga la primera jerarquía de fotogramas desde un archivo .x.

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

*Nombre de archivo* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*MeshOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la [**enumeración D3DXMESH**](./d3dxmesh.md) que especifican opciones de creación para la malla.

</dd> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el objeto de dispositivo asociado a la malla.

</dd> <dt>

*pAlloc* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Puntero a una [**interfaz ID3DXAllocateHierarchy.**](id3dxallocatehierarchy.md)

</dd> <dt>

*pUserDataLoader* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interfaz proporcionada por la aplicación que permite cargar datos de usuario. Vea [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHierarchy* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Devuelve un puntero a la jerarquía de fotogramas cargada. Vea [**D3DXFRAME.**](d3dxframe.md)

</dd> <dt>

*ppAnimController* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Devuelve un puntero al controlador de animación correspondiente a la animación en el archivo .x. Esto se crea con pistas y eventos predeterminados. Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXLoadMeshHierarchyFromXW. De lo contrario, la llamada de función se resuelve en D3DXLoadMeshHierarchyFromXA.

Todas las mallas del archivo se contraerán en una malla de salida. Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.

**D3DXLoadMeshHierarchyFromX** carga los datos de animación y la jerarquía de fotogramas desde un archivo .x. Examina el archivo .x y compila una jerarquía de fotogramas y un controlador de animación según el objeto derivado de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)que se le pasa a través de pAlloc. La carga de los datos requiere varios pasos como se muestra a continuación:

1.  Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)e implemente cada método. Esto controla cómo se asignan y liberan los marcos y las mallas.
2.  Derive [**ID3DXLoadUserData,**](id3dxloaduserdata.md)implementando cada método. Si el archivo .x no tiene datos incrustados definidos por el usuario o si no los necesita, puede omitir esta parte.
3.  Cree un objeto de la [**clase ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) y, opcionalmente, de la clase LoadUserData. No es necesario llamar a ningún método de estos objetos usted mismo.
4.  Llame **a D3DXLoadMeshHierarchyFromX** y pase el objeto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) y el objeto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (o **NULL)** para crear la jerarquía de fotogramas y el controlador de animación. Todos los conjuntos de animaciones y fotogramas se registran automáticamente en el controlador de animación.

Durante la carga, se llama de nuevo a [**CreateFrame**](id3dxallocatehierarchy--createframe.md) y [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) en cada fotograma para controlar la carga y asignación del marco. La aplicación define estos métodos para controlar cómo se almacenan los fotogramas. Se llama de nuevo a [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) [**y LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) en cada objeto de malla para controlar la carga y asignación de objetos de malla. Se vuelve a llamar a [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) para cada objeto de nivel superior que los otros métodos no cargan.

Para liberar estos datos, llame a ID3DXAnimationController::Release para liberar los conjuntos de animaciones y [**D3DXFRAMEDestroy,**](d3dxframedestroy.md)pasando el nodo raíz de la jerarquía de fotogramas y un objeto de la clase [**derivada ID3DXAllocateHierarchy.**](id3dxallocatehierarchy.md) [**Se llamará**](id3dxallocatehierarchy--destroyframe.md) a [**DestroyFrame y DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) para cada objeto de marco y malla de la jerarquía de fotogramas. La implementación de **DestroyFrame debe** liberar todo lo asignado por [**CreateFrame**](id3dxallocatehierarchy--createframe.md)y, del mismo modo, para los métodos de contenedor de malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
