---
description: Establece el valor de influencia de un póreo.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: Método ID3DXSkinInfo::SetIonalInfluence (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575217"
---
# <a name="id3dxskininfosetboneinfluence-method"></a>Método ID3DXSkinInfo::SetIonalInfluence

Establece el valor de influencia de un póreo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Insólote* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de pándalo.

</dd> <dt>

*numInfluences* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de influencias.

</dd> <dt>

*vértices* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matriz de vértices influenciados por un pórtico.

</dd> <dt>

*pesos* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Matriz de pesos influenciada por un póreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetIonalInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNumPxInfluences**](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
