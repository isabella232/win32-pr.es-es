---
description: Obtiene el identificador de una técnica mediante la búsqueda de su nombre.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: Método ID3DXBaseEffect::GetTechniqueByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 446c4625f6eee8c654991a9ed3685125e34d2de97553d328538deea0a7a4e116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121948"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>Método ID3DXBaseEffect::GetTechniqueByName

Obtiene el identificador de una técnica mediante la búsqueda de su nombre.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre de la técnica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador de la primera técnica que tiene el nombre especificado o **NULL** si no se encuentra el nombre. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
