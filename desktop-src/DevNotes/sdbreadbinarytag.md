---
Description: Recupera los datos binarios para el TAGID especificado.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: Función SdbReadBinaryTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 92d63182273c96707bb155071164a6b6838378615f603d8ef6d332d6c65be460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911575"
---
# <a name="sdbreadbinarytag-function"></a>Función SdbReadBinaryTag

Recupera los datos binarios para el **TAGID especificado.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tiWhich* \[ En\]
</dt> <dd>

TAGID **que** corresponde a los datos que se recuperarán.

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Búfer que recibe los datos binarios. Este parámetro no puede ser **NULL.**

</dd> <dt>

*dwBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer *pBuffer,* en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




