---
description: Obtiene el identificador de una técnica buscando su nombre.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect:: GetTechniqueByName (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718509"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>ID3DXBaseEffect:: GetTechniqueByName (método)

Obtiene el identificador de una técnica buscando su nombre.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre de la técnica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador de la primera técnica que tiene el nombre especificado, o **null** si no se encuentra el nombre. Vea [identificadores (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
