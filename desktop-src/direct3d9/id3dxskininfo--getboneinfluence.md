---
description: Obtiene los vértices y pesos que un hueso influye.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'ID3DXSkinInfo:: GetBoneInfluence (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717545"
---
# <a name="id3dxskininfogetboneinfluence-method"></a>ID3DXSkinInfo:: GetBoneInfluence (método)

Obtiene los vértices y pesos que un hueso influye.

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

*Hueso* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número del hueso.

</dd> <dt>

*vértices* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Obtiene la matriz de vértices influida en un hueso.

</dd> <dt>

*pesos* \[ in, out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Obtiene la matriz de pesos influida por un hueso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Use [**ID3DXSkinInfo:: GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) para averiguar el número de vértices que influyen en el hueso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
