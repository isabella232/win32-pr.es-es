---
description: Declara un nuevo índice en la base de datos especificada.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex función)
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
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666195"
---
# <a name="sdbdeclareindex-function"></a>SdbDeclareIndex función)

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

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tWhich* \[ de\]
</dt> <dd>

Este parámetro debe ser **una \_ \_ lista de tipo de etiqueta**.

</dd> <dt>

*tKey* \[ de\]
</dt> <dd>

ETIQUETA que especifica el tipo que se va a usar como clave. Este parámetro no puede ser una **\_ \_ lista de tipo de etiqueta**.

</dd> <dt>

*dwEntries* \[ de\]
</dt> <dd>

Número de entradas que se van a asignar en el índice.

</dd> <dt>

*bUniqueKey* \[ de\]
</dt> <dd>

Si este parámetro es **true**, el índice es un índice de clave única.

</dd> <dt>

*piiIndex* \[ enuncia\]
</dt> <dd>

**INDEXID** resultante del índice recién declarado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="remarks"></a>Observaciones

Llame a esta función antes de escribir etiquetas en el nuevo índice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
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

 

 




