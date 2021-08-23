---
description: Confirma los índices recién creados en la base de datos especificada.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Función SdbCommitIndexes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1c133b55456dec402e54c3bcd24b7e84c81752d467be5cf7872896deaafdf424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571345"
---
# <a name="sdbcommitindexes-function"></a>Función SdbCommitIndexes

Confirma los índices recién creados en la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbCommitIndexes(
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

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




