---
description: Finaliza las operaciones de escritura de la lista especificada.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Función SdbEndWriteListTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9367b3c807cf152ab0c7aeb35a0b6d0e93ea03bbd10ea0dacb327030e21553c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076029"
---
# <a name="sdbendwritelisttag-function"></a>Función SdbEndWriteListTag

Finaliza las operaciones de escritura de la lista especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ in, out\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tiList* \[ En\]
</dt> <dd>

TAGID [**de**](tagid.md) la lista

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="remarks"></a>Comentarios

Llame a esta función después de escribir todas las entradas de lista; marcará el final de la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




