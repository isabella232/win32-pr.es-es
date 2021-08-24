---
description: Establece la influencia mínima de los influjos. Se omiten los valores de influencia inferiores a este.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: Método ID3DXSkinInfo::SetMinIonalInfluence (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: abe9f1d7f9c54b9c3086160b974e2bc7dc659eb6dae3ff647f059627ff3ef145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747485"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a>Método ID3DXSkinInfo::SetMinIonalInfluence

Establece la influencia mínima de los influjos. Se omiten los valores de influencia inferiores a este.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MinInfl* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor de influencia mínimo. Se omiten los valores de influencia inferiores a este.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetMinIonalInfluence**](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
