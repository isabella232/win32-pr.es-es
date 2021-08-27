---
description: Recupera los datos binarios para el TAGID especificado.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Función SdbGetBinaryTagData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5bb2155c7fe2ff1ae2d9784777e39740e5b3224cfc60881fbe0d961ddb422360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058525"
---
# <a name="sdbgetbinarytagdata-function"></a>Función SdbGetBinaryTagData

Recupera los datos binarios para el **TAGID especificado.**

## <a name="syntax"></a>Sintaxis


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un puntero a los datos binarios o **NULL** si **el TAGID** no es válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




