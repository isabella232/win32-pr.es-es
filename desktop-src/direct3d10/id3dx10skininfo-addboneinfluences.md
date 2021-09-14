---
description: Habilite un tejido existente para influir en un grupo de vértices y definir cuánta influencia tiene el pórtico en cada vértice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: Método ID3DX10SkinInfo::AddIonalInfluences (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888809"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>Método ID3DX10SkinInfo::AddIonalInfluences

Habilite un tejido existente para influir en un grupo de vértices y definir cuánta influencia tiene el pórtico en cada vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IndexIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un fragmento existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices que se agregarán a la influencia del tejido.

</dd> <dt>

*pIndices* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de índices de vértices. Cada miembro de esta matriz tiene un miembro correspondiente en pWeights, de modo que pIndices i corresponde a \[ \] pWeights \[ i \] . El valor correspondiente de pWeights i determina cuánta influencia tendráIndexIndex en el vértice indexado por \[ \] pIndices \[ i \] . El tamaño de la matriz pIndices debe ser igual o mayor que InfluenceCount.

</dd> <dt>

*pWeights* \[ En\]
</dt> <dd>

Tipo: **\* float**

Puntero a una matriz de pesos de pesos de peso. Cada miembro de esta matriz tiene un miembro correspondiente en pIndices, de modo que pWeights i corresponde a \[ \] pIndices \[ i \] . Cada valor de pWeights está entre 0 y 1 y define la cantidad de influencia que tiene el grosor sobre cada vértice. El tamaño de pWeights debe ser igual o mayor que InfluenceCount.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG o E \_ OUTOFMEMORY.

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

 

 
