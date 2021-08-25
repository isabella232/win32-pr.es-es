---
description: Concatena un grupo de mallas en una malla común. Opcionalmente, este método puede aplicar una transformación de matriz a cada malla de entrada y sus coordenadas de textura.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Función D3DXConcatenateMeshes (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21801c2f4b8ef8dd2a34c9788b402128da4ce4fed33c3c38a08e61c35a847e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857395"
---
# <a name="d3dxconcatenatemeshes-function"></a>Función D3DXConcatenateMeshes

Concatena un grupo de mallas en una malla común. Opcionalmente, este método puede aplicar una transformación de matriz a cada malla de entrada y sus coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMeshes* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Matriz de punteros de malla de entrada [**(vea ID3DXMesh).**](id3dxmesh.md) El número de elementos de la matriz es NumMeshes.

</dd> <dt>

*NumMeshes* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de mallas de entrada que se concatenarán.

</dd> <dt>

*Opciones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de creación de mallas; se trata de una combinación de una o varias [**marcas D3DXMESH.**](./d3dxmesh.md) Las opciones de creación de malla son equivalentes al parámetro options requerido por [**D3DXCreateMesh.**](d3dxcreatemesh.md)

</dd> <dt>

*pGeomXForms* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz opcional de transformaciones de geometría. El número de elementos de la matriz es NumMeshes; cada elemento es una matriz de transformación [**(vea D3DXMATRIX**](d3dxmatrix.md)). Puede ser **NULL.**

</dd> <dt>

*pTextureXForms* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz opcional de transformaciones de textura. El número de elementos de la matriz es NumMeshes; cada elemento es una matriz de transformación [**(vea D3DXMATRIX**](d3dxmatrix.md)). Este parámetro puede ser **NULL.**

</dd> <dt>

*pDecl* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntero opcional a una declaración de vértice [**(vea D3DVERTEXELEMENT9).**](d3dvertexelement9.md) Este parámetro puede ser **NULL.**

</dd> <dt>

*pD3DDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a un [**dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para crear la nueva malla.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a la malla creada (vea [**ID3DXMesh).**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de estos: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Si [no](vertex-declaration.md) se especifica ninguna declaración de vértice como parte del parámetro de creación de malla Options, el método generará una unión de todas las declaraciones de vértices de las submeshes, promocionando canales y tipos si es necesario. El método creará una tabla de atributos a partir de tablas de atributos de las mallas de entrada. Para garantizar la creación de una tabla de atributos, llame a [**Optimizar**](id3dxmesh--optimize.md) con marcas establecidas en D3DXMESHOPT COMPACT y \_ D3DXMESHOPT \_ ATTRSORT (vea [**D3DXMESHOPT).**](./d3dxmeshopt.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
