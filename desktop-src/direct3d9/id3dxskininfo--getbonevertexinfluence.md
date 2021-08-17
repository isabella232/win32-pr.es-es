---
description: Recupera el factor de mezcla y el vértice afectados por una influencia de ángulo especificada.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: Método ID3DXSkinInfo::GetIonalVertexInfluence (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8dfeff1f6c3e8fc7030fa33f8a23c89278a9dd2b1e59f043db7723eac7d32801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801151"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a>Método ID3DXSkinInfo::GetIonalVertexInfluence

Recupera el factor de mezcla y el vértice afectados por una influencia de ángulo especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*numnum* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de la estructura. Debe estar entre 0 y el número de tordos.

</dd> <dt>

*influenceNum* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de la matriz de influencia del pórmico especificado.

</dd> <dt>

*pWeight* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al factor de mezcla influenciado por influenceNum.

</dd> <dt>

*pVertexNum* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al vértice influenciado por influenceNum.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetIonalVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindIonalVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetIonalInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
