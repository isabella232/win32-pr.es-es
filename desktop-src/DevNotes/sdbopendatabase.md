---
description: Abre la base de datos de correcciones de compatibilidad (shim) especificada.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Función SdbOpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: df0081d7373bf67d3df1723be7d5beb272ef7ee4c77c54da8a6985dfe250d7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161201"
---
# <a name="sdbopendatabase-function"></a>Función SdbOpenDatabase

Abre la base de datos de correcciones de compatibilidad (shim) especificada.

## <a name="syntax"></a>Sintaxis


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszPath* \[ En\]
</dt> <dd>

Ruta de acceso de la base de datos. Este parámetro no puede ser **NULL.**

</dd> <dt>

*eType* \[ En\]
</dt> <dd>

Tipo de ruta de acceso. Vea [**PATH \_ TYPE (TIPO DE**](path-type.md) RUTA DE ACCESO) para obtener una lista de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos shim.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




