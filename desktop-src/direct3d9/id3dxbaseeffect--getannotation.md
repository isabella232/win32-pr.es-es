---
description: Obtiene el identificador de una anotación.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect:: GetAnnotation (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718520"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>ID3DXBaseEffect:: GetAnnotation (método)

Obtiene el identificador de una anotación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hObject* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de una técnica, un paso o un parámetro de nivel superior. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*Índice* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de anotación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador de la anotación especificada o **null** si el índice no era válido. Vea [identificadores (Direct3D 9)](handles.md).

## <a name="remarks"></a>Observaciones

Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro. Vea [identificadores (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
