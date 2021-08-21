---
description: Crea una nueva base de datos de correcciones de compatibilidad (shim).
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Función SdbCreateDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161566"
---
# <a name="sdbcreatedatabase-function"></a>Función SdbCreateDatabase

Crea una nueva base de datos de correcciones de compatibilidad (shim).

## <a name="syntax"></a>Sintaxis


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszPath* \[ En\]
</dt> <dd>

Ruta de acceso donde se debe guardar la base de datos. Este parámetro no puede ser **NULL.**

</dd> <dt>

*eType* \[ En\]
</dt> <dd>

Tipo de ruta de acceso. Vea [**PATH \_ TYPE (TIPO DE**](path-type.md) RUTA DE ACCESO) para obtener una lista de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos shim o **NULL en caso** de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




