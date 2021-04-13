---
description: Obtiene la declaración de vértice.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo:: GetDeclaration (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362412"
---
# <a name="id3dxskininfogetdeclaration-method"></a>ID3DXSkinInfo:: GetDeclaration (método)

Obtiene la declaración de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Declaración* \[ de in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla. El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md). La matriz de elementos de vértice finaliza con la macro [**D3DDECL \_ End**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

La matriz de elementos incluye la macro [**D3DDECL \_ End**](d3ddecl-end.md) , que finaliza la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
