---
description: Obtiene la matriz de desplazamiento del hueso.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo:: GetBoneOffsetMatrix (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362418"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>ID3DXSkinInfo:: GetBoneOffsetMatrix (método)

Obtiene la matriz de desplazamiento del hueso.

## <a name="syntax"></a>Sintaxis


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hueso* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número del hueso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Devuelve un puntero a la matriz de desplazamiento del hueso. No libere este puntero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
