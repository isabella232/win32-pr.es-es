---
description: Declara un nuevo índice en la base de datos especificada.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Función SdbDeclareIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: b428699641d5a18bad8a1869f59ab1bb5402e7b667526070c3dc0575e435fc38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666594"
---
# <a name="sdbdeclareindex-function"></a>Función SdbDeclareIndex

Declara un nuevo índice en la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tWhich* \[ En\]
</dt> <dd>

Este parámetro debe ser **TAG \_ TYPE \_ LIST.**

</dd> <dt>

*tKey* \[ En\]
</dt> <dd>

Etiqueta que especifica el tipo que se va a usar como clave. Este parámetro no puede ser **TAG \_ TYPE \_ LIST.**

</dd> <dt>

*dwEntries* \[ En\]
</dt> <dd>

Número de entradas que se asignarán en el índice.

</dd> <dt>

*bUniqueKey* \[ En\]
</dt> <dd>

Si este parámetro es **TRUE**, el índice es un índice de clave única.

</dd> <dt>

*piiIndex* \[ out\]
</dt> <dd>

IndexID **resultante** del índice recién declarado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="remarks"></a>Observaciones

Llame a esta función antes de escribir etiquetas en el nuevo índice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INDEXID**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




