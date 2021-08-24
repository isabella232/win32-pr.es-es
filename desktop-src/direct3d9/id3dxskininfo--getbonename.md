---
description: Obtiene el nombre del pie, del índice de la columna.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: Método ID3DXSkinInfo::GetNameName (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa56b175d9047935b9f92829823ba2608536ddabb90cb0ad674b86b73cc17475
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674735"
---
# <a name="id3dxskininfogetbonename-method"></a>Método ID3DXSkinInfo::GetNameName

Obtiene el nombre del pie, del índice de la columna.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Insólote* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de pándalo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Devuelve el nombre del pánseo. No libera esta cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetNameName**](id3dxskininfo--setbonename.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNumPxs**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
