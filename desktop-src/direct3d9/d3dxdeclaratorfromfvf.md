---
description: Devuelve un declarador de un código de formato de vértice flexible (FVF).
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: Función D3DXDeclaratorFromFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707888"
---
# <a name="d3dxdeclaratorfromfvf-function"></a>D3DXDeclaratorFromFVF función)

Devuelve un declarador de un código de formato de vértice flexible (FVF).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FVF* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de [D3DFVF](d3dfvf.md) que describe el FVF desde el que se va a generar la matriz declaradora devuelta.

</dd> <dt>

*Declaración* \[ de in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla. El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DXERR \_ INVALIDMESH.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
