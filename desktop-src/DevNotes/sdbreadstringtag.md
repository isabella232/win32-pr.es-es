---
Description: Recupera la cadena para el TAGID especificado.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Función SdbReadStringTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8f8652e944328298b7cd3888fa93c41d3551ba913f4acd848f60fa053ed0067e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044945"
---
# <a name="sdbreadstringtag-function"></a>Función SdbReadStringTag

Recupera la cadena para el **TAGID especificado.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
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

TagID **que** corresponde a los datos que se recuperarán.

</dd> <dt>

*pwszBuffer* \[ out\]
</dt> <dd>

Búfer que recibe la cadena. Este parámetro no puede ser **NULL.**

</dd> <dt>

*cchBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer *pwszBuffer,* en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadBinaryTag**](sdbreadbinarytag.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> </dl>

 

 




