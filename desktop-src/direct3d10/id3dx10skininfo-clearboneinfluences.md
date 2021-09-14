---
description: Borrar una lista de vértices que influye.
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: Método ID3DX10SkinInfo::ClearIonalInfluences (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6f161ba400b684b12d6b0a091abb1fa452d476b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888785"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a>Método ID3DX10SkinInfo::ClearIonalInfluences

Borrar una lista de vértices que influye.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ClearBoneInfluences(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index deindex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un pórmico existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

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

 

 
