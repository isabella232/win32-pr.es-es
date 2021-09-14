---
description: Cambiar qué influencia tienen los vértices.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: Método ID3DX10SkinInfo::RemapPxs (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965059"
---
# <a name="id3dx10skininforemapbones-method"></a>Método ID3DX10SkinInfo::RemapPxs

Cambiar qué influencia tienen los vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewBoneCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nuevo número de esqueletos.

</dd> <dt>

*pIqueRemap* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de índices de pórdices, que describen el remapping. Por ejemplo, por ejemplo, say SkinInfo contiene algunos fragmentos, como que se asigna a v0, a pero1 a v1 y a la matriz con 2,1,0, y se especifica array con 2,1,0 para pDimensionRemap. Esto hará que cause que cause que se asignen a v2, a pero1 a v1 y a la versión 2 a v0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY o E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
