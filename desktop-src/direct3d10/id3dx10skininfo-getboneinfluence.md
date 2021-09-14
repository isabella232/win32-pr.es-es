---
description: Obtiene la cantidad de influencia que tiene un ángulo determinado sobre un vértice determinado.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: Método ID3DX10SkinInfo::GetIonalInfluence (D3DX10.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965068"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>Método ID3DX10SkinInfo::GetIonalInfluence

Obtiene la cantidad de influencia que tiene un ángulo determinado sobre un vértice determinado.

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

*IndexIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un fragmento existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de la lista de vértices que influye en el tejido.

</dd> <dt>

*pWeight* \[ En\]
</dt> <dd>

Tipo: **\* float**

La cantidad de influencia, entre 0 y 1, que el extremo tiene sobre el vértice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser E \_ INVALIDARG.

## <a name="remarks"></a>Observaciones

Use ID3DX10SkinInfo::GetIonalInfluenceCount para averiguar cuántos vértices influye el influjo de la ingle.

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

 

 
