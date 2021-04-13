---
description: Recupera el factor de mezcla y el vértice afectados por una influencia del hueso especificada.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'ID3DXSkinInfo:: GetBoneVertexInfluence (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362414"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a>ID3DXSkinInfo:: GetBoneVertexInfluence (método)

Recupera el factor de mezcla y el vértice afectados por una influencia del hueso especificada.

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

*boneNum* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice del hueso. Debe estar comprendido entre 0 y el número de huesos.

</dd> <dt>

*influenceNum* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de la matriz de influencia del hueso especificado.

</dd> <dt>

*pWeight* \[ in, out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero al factor de combinación influenciado por influenceNum.

</dd> <dt>

*pVertexNum* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al vértice influido por influenceNum.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
