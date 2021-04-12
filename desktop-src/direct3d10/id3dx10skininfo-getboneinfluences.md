---
description: Obtiene una lista de vértices a los que afecta un hueso determinado y una lista de la cantidad de influencia que tiene el hueso en cada vértice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo:: GetBoneInfluences (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280514"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>ID3DX10SkinInfo:: GetBoneInfluences (método)

Obtiene una lista de vértices a los que afecta un hueso determinado y una lista de la cantidad de influencia que tiene el hueso en cada vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BoneIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice que especifica un hueso existente. Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Desplazamiento desde la parte superior de la lista de vértices influidos por el hueso. Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Recuento* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de índices y pesos que se van a recuperar. Debe estar comprendido entre 0 y el valor devuelto por ID3DX10SkinInfo:: GetBoneInfluenceCount.

</dd> <dt>

*pDestIndices* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Una lista de índices en el búfer de vértices, cada uno de los cuales representa un vértice influido por el hueso. Estos valores corresponden a los valores de pDestWeights, de modo que pDestIndices \[ i se \] corresponda con pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ in, out\]
</dt> <dd>

Tipo: **float \***

Una lista de la cantidad de influencia que tiene el hueso en cada vértice. Estos valores corresponden a los valores de pDestIndices, de modo que pDestWeights \[ i se \] corresponda con pDestIndices \[ i \] . f

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG o e \_ OUTOFMEMORY.

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

 

 
