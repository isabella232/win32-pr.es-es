---
description: Recupera el índice de la influencia del ángulo que afecta a un solo vértice.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: Método ID3DXSkinInfo::FindCoreVertexInfluenceIndex (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966619"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a>Método ID3DXSkinInfo::FindIonalVertexInfluenceIndex

Recupera el índice de la influencia del ángulo que afecta a un solo vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ynum* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de la estructura. Debe estar entre 0 y el número de esqueletos.

</dd> <dt>

*vertexNum* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice del vértice para el que se va a encontrar la influencia del ángulo. Debe estar entre 0 y el número de vértices de la malla.

</dd> <dt>

*pInfluenceIndex* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al índice de la influencia del ángulo que afecta a vertexNum.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si el ángulo especificado no influye en el vértice especificado, se devuelve S \_ FALSE. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetIonalVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::SetIonalVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::GetIonalInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
