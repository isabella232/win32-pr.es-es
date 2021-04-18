---
description: Establece un valor de influencia de un hueso en un solo vértice.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'ID3DXSkinInfo:: SetBoneVertexInfluence (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707720"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a>ID3DXSkinInfo:: SetBoneVertexInfluence (método)

Establece un valor de influencia de un hueso en un solo vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
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

*peso* \[ de de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de mezcla de la influencia del hueso especificada.

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

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
