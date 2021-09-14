---
description: Clona un objeto de información de máscara.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: Método ID3DXSkinInfo::Clone (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966627"
---
# <a name="id3dxskininfoclone-method"></a>Método ID3DXSkinInfo::Clone

Clona un objeto de información de máscara.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSkinInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Dirección de un puntero a un [**objeto ID3DXSkinInfo,**](id3dxskininfo.md) que contendrá el objeto clonado si el método se realiza correctamente.

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
</dt> </dl>

 

 




