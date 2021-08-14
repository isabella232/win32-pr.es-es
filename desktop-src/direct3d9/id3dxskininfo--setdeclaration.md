---
description: Establece la declaración de vértice.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: Método ID3DXSkinInfo::SetDeclaration (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7189abac9041e1abad67ea60558f5ec33714ae47d50225d362ad3bc09e6d1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985265"
---
# <a name="id3dxskininfosetdeclaration-method"></a>Método ID3DXSkinInfo::SetDeclaration

Establece la declaración de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeclaration* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntero a una matriz [**de elementos D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetDeclaration**](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




