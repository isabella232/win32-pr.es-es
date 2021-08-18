---
description: Validar una técnica.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: Método ID3DXEffect::ValidateTechnique (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4ba3f6422c373c63a9b147ded8f288f642dcd880805cbd1d8b638b3f0e7f8f8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951705"
---
# <a name="id3dxeffectvalidatetechnique-method"></a>Método ID3DXEffect::ValidateTechnique

Validar una técnica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hTechnique* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ CONFLICTINGRENDERSTATE, D3DERR \_ CONFLICTINGTEXTUREFILTER, \_ D3DERR DEVICELOST, D3DERR \_ DRIVERINTERNALERROR, D3DERR \_ TOOMANYOPERATIONS, D3DERR \_ UNSUPPORTEDALPHAARG, D3DERR \_ UNSUPPORTEDALPHAOPERATION, D3DERR \_ UNSUPPORTEDCOLORARG, D3DERR \_ UNSUPPORTEDCOLOROPERATION, D3DERR \_ UNSUPPORTEDFACTORVALUE, D3DERR \_ UNSUPPORTEDTEXTUREFILTER y D3DERR \_ WRONGTEXTUREFORMAT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetTechnique**](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




