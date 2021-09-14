---
description: Obtiene el identificador de una función mediante la búsqueda de su nombre.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: Método ID3DXBaseEffect::GetFunctionByName (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964832"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a>Método ID3DXBaseEffect::GetFunctionByName

Obtiene el identificador de una función mediante la búsqueda de su nombre.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre de la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador de la función especificada o **NULL** si no se encontró el nombre. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
