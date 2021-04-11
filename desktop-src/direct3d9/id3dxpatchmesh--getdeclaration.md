---
description: Obtiene la declaración de vértice.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh:: GetDeclaration (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362816"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>ID3DXPatchMesh:: GetDeclaration (método)

Obtiene la declaración de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeclaration* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla. La dimensión de esta matriz declaradora es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md). La matriz de elementos de vértice finaliza con la macro [**D3DDECL \_ End**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La matriz de elementos incluye la macro [**D3DDECL \_ End**](d3ddecl-end.md) , que finaliza la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
