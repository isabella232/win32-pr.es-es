---
description: Obtiene la matriz de desplazamiento de desplazamiento de desplazamiento de desplazamiento.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: Método ID3DXSkinInfo::GetOffsetMatrix (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d10586fc9d4008ebd22b7edf2fa955628ffa0ab703ef70ed06cb2f2cb1fd8d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492305"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>Método ID3DXSkinInfo::GetOffsetMatrix

Obtiene la matriz de desplazamiento de desplazamiento de desplazamiento de desplazamiento.

## <a name="syntax"></a>Sintaxis


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Desótola* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de pándalo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Devuelve un puntero a la matriz de desplazamiento de desplazamiento. No libera este puntero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetIonalOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumIonals**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
