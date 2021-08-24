---
description: Obtenga una lista de vértices que influye en un ángulo determinado y una lista de la cantidad de influencia que tiene el pórtico en cada vértice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: Método ID3DX10SkinInfo::GetIonalInfluences (D3DX10.h)
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
ms.openlocfilehash: 38d6901abd871a2b65f4d6816ad4d4b7a0d2effb5ccbd3f4ccee20bc0b8d5ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752915"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>Método ID3DX10SkinInfo::GetIonalInfluences

Obtenga una lista de vértices que influye en un ángulo determinado y una lista de la cantidad de influencia que tiene el pórtico en cada vértice.

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

*Index deindex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un pórmico existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Desplazamiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Desplazamiento desde la parte superior de la lista de vértices influenciados. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetIonalInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de índices y pesos que se recuperarán. Debe estar entre 0 y el valor devuelto por ID3DX10SkinInfo::GetIonalInfluenceCount.

</dd> <dt>

*pDestIndices* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Lista de índices en el búfer de vértices, cada uno de los que representan un vértice influenciado por el pórdice. Estos valores corresponden a los valores de pDestWeights, de modo que pDestIndices i corresponde a \[ \] pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ in, out\]
</dt> <dd>

Tipo: **\* float**

Lista de la cantidad de influencia que tiene el póreo en cada vértice. Estos valores corresponden a los valores de pDestIndices, de modo que pDestWeights i corresponde a \[ \] pDestIndices \[ i \] .f

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser: E \_ INVALIDARG o E \_ OUTOFMEMORY.

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

 

 
