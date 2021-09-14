---
description: Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influenciados de un ángulo determinado.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: Método ID3DX10SkinInfo::FindIonalInfluenceIndex (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888764"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a>Método ID3DX10SkinInfo::FindIonalInfluenceIndex

Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influenciados de un ángulo determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IndexIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice que especifica un fragmento existente. Debe estar entre 0 y el valor devuelto por [**ID3DX10SkinInfo::GetNumPxs**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*VertexIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice del vértice en el búfer de vértices.

</dd> <dt>

*pInfluenceIndex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Índice del vértice en la lista de vértices influenciados del ángulo.

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

 

 
