---
description: Busca una etiqueta secundaria dentro del elemento primario especificado y devuelve el TAGID del primer elemento secundario.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Función SdbGetFirstChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58e63b3c1c8b3e56c9610ec795c1706fe58990e4611c36886ee4a3061d0816fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075979"
---
# <a name="sdbgetfirstchild-function"></a>Función SdbGetFirstChild

Busca una etiqueta secundaria dentro del elemento primario especificado y devuelve el **TAGID** del primer elemento secundario.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
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

TAGID **del** inicio de la búsqueda. Este parámetro puede ser **TAGID \_ ROOT o** **TAG TYPE \_ \_ LIST.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No **se encuentra el TAGID** del primer elemento secundario o **TAGID \_ NULL.**

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

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 




