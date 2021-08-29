---
description: Escribe un valor QWORD en la base de datos especificada.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: Función SdbWriteQWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: adff37c575604f9d717c3e2253c9cad545a14c32e22c7718c9063384c78a37b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044785"
---
# <a name="sdbwriteqwordtag-function"></a>Función SdbWriteQWORDTag

Escribe un valor **QWORD** en la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
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

Etiqueta de la entrada. Esta ETIQUETA debe ser del tipo **TAG \_ TYPE \_ QWORD**.

</dd> <dt>

*qwData* \[ En\]
</dt> <dd>

Valor.

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

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




