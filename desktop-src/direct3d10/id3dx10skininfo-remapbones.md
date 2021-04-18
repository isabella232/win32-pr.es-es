---
description: Cambiar los huesos influyen en los vértices.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo:: RemapBones (método) (D3DX10. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718226"
---
# <a name="id3dx10skininforemapbones-method"></a>ID3DX10SkinInfo:: RemapBones (método)

Cambiar los huesos influyen en los vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewBoneCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nuevo número de huesos.

</dd> <dt>

*pBoneRemap* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a una matriz de índices de hueso, que describen la reasignación. Por ejemplo, suponga que SkinInfo contiene algunos huesos, de modo que bone0 se asigna a V0, bone1 a V1 y bone2 a V2, y se especifica array con 2, 1, 0 para pBoneRemap. Esto hará que bone0 se asigne a V2, bone1 a V1 y bone2 a v0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY o e \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
