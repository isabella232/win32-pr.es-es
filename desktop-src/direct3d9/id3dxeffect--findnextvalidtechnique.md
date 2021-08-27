---
description: Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: Método ID3DXEffect::FindNextValidTechnique (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f65a08d1f1ec8a1f7710272d2a1c48e936f211b3bcdee8b84652b9a7196f39e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118705"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>Método ID3DXEffect::FindNextValidTechnique

Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hTechnique* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de una técnica. Vea [Identificadores (Direct3D 9).](handles.md) Especifique **NULL** para este parámetro para buscar la primera técnica válida.

</dd> <dt>

*pTechnique* \[ out\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

Puntero a un identificador para la siguiente técnica. **Se** devuelve NULL si esta es la última técnica. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect::ValidateTechnique**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




