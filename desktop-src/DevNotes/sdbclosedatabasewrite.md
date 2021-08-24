---
description: Cierra la base de datos especificada.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Función SdbCloseDatabaseWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0ef1c02731f2875fbdfc910243ed80faa28b6ab029314ea43ef281355a08487a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161586"
---
# <a name="sdbclosedatabasewrite-function"></a>Función SdbCloseDatabaseWrite

Cierra la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ in, out\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función llama a [**SdbCloseDatabase**](sdbclosedatabase.md); por lo tanto, estas dos funciones son equivalentes.

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

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> </dl>

 

 




