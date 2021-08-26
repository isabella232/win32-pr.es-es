---
Description: Recupera el valor DWORD para el TAGID especificado.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: Función SdbReadDWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ce168aab7755dcd11f145caf44678a489bca152753ea010edbd7387b3e730f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044955"
---
# <a name="sdbreaddwordtag-function"></a>Función SdbReadDWORDTag

Recupera el **valor DWORD** para el **TAGID especificado.**

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
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

*dwDefault* \[ En\]
</dt> <dd>

Valor predeterminado que se va a devolver en caso de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el valor si se ha ejecutado correctamente o *dwDefault* en caso de error.

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

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




