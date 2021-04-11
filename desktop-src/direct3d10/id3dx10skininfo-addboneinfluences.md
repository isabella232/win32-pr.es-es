---
description: Permite que un hueso existente afecte a un grupo de vértices y defina la influencia que tenga el hueso en cada vértice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo:: AddBoneInfluences (método) (D3DX10. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280336"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>ID3DX10SkinInfo:: AddBoneInfluences (método)

Permite que un hueso existente afecte a un grupo de vértices y defina la influencia que tenga el hueso en cada vértice.

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

*BoneIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice que especifica un hueso existente. Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices que se van a agregar a la influencia del hueso.

</dd> <dt>

*pIndices* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a una matriz de índices de vértice. Cada miembro de esta matriz tiene un miembro correspondiente en pWeights, de modo que pIndices \[ i se \] corresponde con pWeights \[ i \] . El valor correspondiente en pWeights \[ \] determinará la cantidad de influencia que BoneIndex tendrá en el vértice indexado por pIndices \[ i \] . El tamaño de la matriz pIndices debe ser igual o mayor que InfluenceCount.

</dd> <dt>

*pWeights* \[ de\]
</dt> <dd>

Tipo: **float \***

Puntero a una matriz de pesos del hueso. Cada miembro de esta matriz tiene un miembro correspondiente en pIndices, de modo que pWeights \[ i se \] corresponde con pIndices \[ i \] . Cada valor de pWeights se encuentra entre 0 y 1, y define la cantidad de influencia que tiene el hueso en cada vértice. El tamaño de pWeights debe ser igual o mayor que InfluenceCount.

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

 

 
