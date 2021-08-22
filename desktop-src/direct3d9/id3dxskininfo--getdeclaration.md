---
description: 'Método ID3DXSkinInfo::GetDeclaration: obtiene la declaración de vértice.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: Método ID3DXSkinInfo::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 8188094801ed3a9cef4be3c441d6afb5032e86178da50d837017c0836a702c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800955"
---
# <a name="id3dxskininfogetdeclaration-method"></a>Método ID3DXSkinInfo::GetDeclaration

Obtiene la declaración de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Declaración* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz [**de elementos D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describen el formato de vértice de los vértices de la malla. El límite superior de esta matriz declarator es [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md). La matriz de elementos de vértice termina con la macro [**\_ END de D3DDECL.**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

La matriz de elementos incluye la macro [**\_ END de D3DDECL,**](d3ddecl-end.md) que finaliza la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
