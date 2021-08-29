---
description: Establece el nombre del país.
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: Método ID3DXSkinInfo::SetCoreName (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dad83b21286a82c33b696374741937b017615912ed01d38b56dafd9af2f8d153
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095705"
---
# <a name="id3dxskininfosetbonename-method"></a>Método ID3DXSkinInfo::SetNameName

Establece el nombre del país.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Desótola* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de ándes

</dd> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del nombre del susto

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)devuelve los nombres de los apellidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNameName**](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 
