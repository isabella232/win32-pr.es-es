---
description: Recupera una declaración que describe los vértices de la malla.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: Método ID3DXBaseMesh::GetDeclaration (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d66afd8daf6a8cc60fa63dcf38e6bb853c33ca05986d2a37b94eba1250eb01b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026475"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a>Método ID3DXBaseMesh::GetDeclaration

Recupera una declaración que describe los vértices de la malla.

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

Matriz [**de elementos D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describen el formato de vértice de los vértices de malla. El límite superior de esta matriz declarativa es [**MAX \_ FVF \_ DECL \_ SIZE.**](./max-fvf-decl-size.md) La matriz de elementos de vértice termina con la macro [**END D3DDECL. \_**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

La matriz de elementos incluye la macro [**\_ END D3DDECL,**](d3ddecl-end.md) que finaliza la declaración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
