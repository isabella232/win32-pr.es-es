---
description: Busca la siguiente etiqueta secundaria dentro del elemento primario especificado y devuelve el TAGID del siguiente elemento secundario.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Función SdbGetNextChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045323"
---
# <a name="sdbgetnextchild-function"></a>Función SdbGetNextChild

Busca la siguiente etiqueta secundaria dentro del elemento primario especificado y devuelve el **TAGID** del siguiente elemento secundario.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tiParent* \[ En\]
</dt> <dd>

TAGID **del** inicio de búsqueda. Este parámetro puede ser **TAGID \_ ROOT o** **TAG TYPE \_ \_ LIST.**

</dd> <dt>

*tiPrev* \[ En\]
</dt> <dd>

TAGID **del** elemento secundario anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TagID **del** elemento secundario o **TAGID \_ NULL** si no se encuentra ningún elemento secundario.

## <a name="remarks"></a>Comentarios

Antes de llamar a esta función, llame a [**la función SdbGetFirstChild.**](sdbgetfirstchild.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




