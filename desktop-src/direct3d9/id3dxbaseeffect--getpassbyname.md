---
description: Obtiene el identificador de un paso buscando su nombre.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'ID3DXBaseEffect:: GetPassByName (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718513"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>ID3DXBaseEffect:: GetPassByName (método)

Obtiene el identificador de un paso buscando su nombre.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hTechnique* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de la técnica primaria. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre del paso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador del primer paso dentro de la técnica especificada que tiene el nombre especificado, o **null** si no se encuentra el nombre. Vea [identificadores (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
