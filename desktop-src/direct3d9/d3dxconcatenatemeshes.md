---
description: Concatena un grupo de mallas en una malla común. Este método puede aplicar opcionalmente una transformación de matriz a cada malla de entrada y sus coordenadas de textura.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Función D3DXConcatenateMeshes (D3DX9Mesh. h)
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
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698305"
---
# <a name="d3dxconcatenatemeshes-function"></a>D3DXConcatenateMeshes función)

Concatena un grupo de mallas en una malla común. Este método puede aplicar opcionalmente una transformación de matriz a cada malla de entrada y sus coordenadas de textura.

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

*ppMeshes* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Matriz de punteros de malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)). El número de elementos de la matriz es NumMeshes.

</dd> <dt>

*NumMeshes* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de mallas de entrada que se van a concatenar.

</dd> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de creación de mallas; se trata de una combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) . Las opciones de creación de malla son equivalentes al parámetro Options que requiere [**D3DXCreateMesh**](d3dxcreatemesh.md).

</dd> <dt>

*pGeomXForms* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz opcional de transformaciones de geometría. El número de elementos de la matriz es NumMeshes; cada elemento es una matriz de transformación (vea [**D3DXMATRIX**](d3dxmatrix.md)). Puede ser **null**.

</dd> <dt>

*pTextureXForms* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz opcional de transformaciones de textura. El número de elementos de la matriz es NumMeshes; cada elemento es una matriz de transformación (vea [**D3DXMATRIX**](d3dxmatrix.md)). Este parámetro puede ser **null**.

</dd> <dt>

*pDecl* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntero opcional a una declaración de vértice (vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)). Este parámetro puede ser **null**.

</dd> <dt>

*pD3DDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a un dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para crear la nueva malla.

</dd> <dt>

*ppMeshOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a la malla creada (vea [**ID3DXMesh**](id3dxmesh.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Si no se proporciona ninguna [declaración de vértice](vertex-declaration.md) como parte del parámetro de creación de malla Options, el método generará una Unión de todas las declaraciones de vértices de las submallas, promoviendo canales y tipos si es necesario. El método creará una tabla de atributos a partir de las tablas de atributos de las mallas de entrada. Para garantizar la creación de una tabla de atributos, llame a [**Optimize**](id3dxmesh--optimize.md) with Flags establecido en D3DXMESHOPT \_ Compact y D3DXMESHOPT \_ ATTRSORT (consulte [**D3DXMESHOPT**](./d3dxmeshopt.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
