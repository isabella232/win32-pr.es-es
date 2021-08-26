---
description: Establezca la cantidad de influencia que tiene un póreo determinado sobre un vértice determinado.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: Método ID3DX10SkinInfo::SetIonalInfluence (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1bf2f2a6ec92a1e4551bdc22d43bd143c9da5c8114c44619c073a838de52c606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069965"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a>Método ID3DX10SkinInfo::SetIonalInfluence

Establezca la cantidad de influencia que tiene un póreo determinado sobre un vértice determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index deindex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un pórmico existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de la lista de vértices que influye en el tejido.

</dd> <dt>

*Peso* \[ En\]
</dt> <dd>

Tipo: **float**

La cantidad de influencia, entre 0 y 1, que tiene el tejido sobre el vértice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
