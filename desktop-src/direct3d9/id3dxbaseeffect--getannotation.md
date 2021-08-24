---
description: Obtiene el identificador de una anotación.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: Método ID3DXBaseEffect::GetAnnotation (D3DX9Effect.h)
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
ms.openlocfilehash: c35deeb04e7cf21be429976c102fdf7c3126b1691b3f63725fc994ef79f7ad42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279015"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>Método ID3DXBaseEffect::GetAnnotation

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

*hObject* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de una técnica, paso o parámetro de nivel superior. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de anotación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve el identificador de la anotación especificada o **NULL** si el índice no era válido. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="remarks"></a>Comentarios

Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro. Vea [Identificadores (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
