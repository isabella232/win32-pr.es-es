---
description: Crea una nueva etiqueta de lista para las operaciones de escritura.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Función SdbBeginWriteListTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 448b57e73bec0115d4c2ae87be96630cad6542833da66a2de8e02037c264de83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058585"
---
# <a name="sdbbeginwritelisttag-function"></a>Función SdbBeginWriteListTag

Crea una nueva etiqueta de lista para las operaciones de escritura.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tTag* \[ En\]
</dt> <dd>

Etiqueta de la nueva entrada. Este valor debe ser de tipo **TAG \_ TYPE \_ LIST.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el [**TAGID de**](tagid.md) la nueva lista si se ejecuta correctamente o **TAGID \_ NULL** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> <dt>

[**etiqueta**](tag.md)
</dt> <dt>

[Tipos TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




