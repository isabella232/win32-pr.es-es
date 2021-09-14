---
description: Obtiene los vértices y pesos que influye en un pórtico.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: Método ID3DXSkinInfo::GetIonalInfluence (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966611"
---
# <a name="id3dxskininfogetboneinfluence-method"></a>Método ID3DXSkinInfo::GetIonalInfluence

Obtiene los vértices y pesos que influye en un pórtico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Insólote* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de pándalo.

</dd> <dt>

*vértices* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Obtenga la matriz de vértices influenciados por un pórtico.

</dd> <dt>

*pesos* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Obtenga la matriz de pesos influenciada por un póreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Use [**ID3DXSkinInfo::GetNumMutInfluences**](id3dxskininfo--getnumboneinfluences.md) para averiguar cuántos vértices influye el tejido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetIonalInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
