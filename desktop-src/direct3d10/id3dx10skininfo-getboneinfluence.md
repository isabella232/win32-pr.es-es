---
description: Obtiene la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'ID3DX10SkinInfo:: GetBoneInfluence (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718360"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>ID3DX10SkinInfo:: GetBoneInfluence (método)

Obtiene la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BoneIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice que especifica un hueso existente. Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de la lista de vértices del hueso a la que influye.

</dd> <dt>

*pWeight* \[ de\]
</dt> <dd>

Tipo: **float \***

La cantidad de influencia, entre 0 y 1, que tiene el hueso en el vértice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser E \_ INVALIDARG.

## <a name="remarks"></a>Observaciones

Use ID3DX10SkinInfo:: GetBoneInfluenceCount para averiguar el número de vértices que influyen en el hueso.

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

 

 
