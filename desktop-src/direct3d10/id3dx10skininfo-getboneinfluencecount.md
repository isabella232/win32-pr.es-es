---
description: Obtiene el número de vértices que influye en un dado.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: Método ID3DX10SkinInfo::GetIonalInfluenceCount (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965071"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a>Método ID3DX10SkinInfo::GetIonalInfluenceCount

Obtiene el número de vértices que influye en un dado.

## <a name="syntax"></a>Sintaxis


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IndexIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un fragmento existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.

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

 

 
