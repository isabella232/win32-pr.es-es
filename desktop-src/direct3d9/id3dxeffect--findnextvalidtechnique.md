---
description: Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect:: FindNextValidTechnique (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424412"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>ID3DXEffect:: FindNextValidTechnique (método)

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

*hTechnique* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de una técnica. Vea [identificadores (Direct3D 9)](handles.md). Especifique **null** para este parámetro para buscar la primera técnica válida.

</dd> <dt>

*pTechnique* \[ enuncia\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

Puntero a un identificador de la técnica siguiente. Se devuelve **null** si se trata de la última técnica. Vea [identificadores (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect::ValidateTechnique**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




