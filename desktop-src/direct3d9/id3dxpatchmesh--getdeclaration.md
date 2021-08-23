---
description: 'Método ID3DXPatchMesh::GetDeclaration: obtiene la declaración de vértice.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: Método ID3DXPatchMesh::GetDeclaration (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 120a9f4179819b550502c2c3764d334159b647fd4c8621d3a088516b9a669d56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747855"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>Método ID3DXPatchMesh::GetDeclaration

Obtiene la declaración de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeclaration* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz [**de elementos D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describen el formato de vértice de los vértices de malla. La dimensión de esta matriz declarator es [**MAX \_ FVF \_ DECL \_ SIZE.**](./max-fvf-decl-size.md) La matriz de elementos de vértice termina con la macro [**END D3DDECL. \_**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La matriz de elementos incluye la macro [**\_ END D3DDECL,**](d3ddecl-end.md) que finaliza la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
