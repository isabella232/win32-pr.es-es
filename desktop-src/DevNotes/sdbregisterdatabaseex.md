---
description: Registra la base de datos especificada.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Función SdbRegisterDatabaseEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 512e180549c246a5504bc14675d61082c68904aa767d98deca5111d9a275dc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984105"
---
# <a name="sdbregisterdatabaseex-function"></a>Función SdbRegisterDatabaseEx

Registra la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDatabasePath* \[ En\]
</dt> <dd>

Ruta de acceso de la base de datos. Este parámetro no puede ser **NULL.**

</dd> <dt>

*dwDatabaseType* \[ En\]
</dt> <dd>

El tipo de base de datos. Vea [Shim Database Types (Tipos de base de](shim-database-types.md) datos shim) para obtener una lista de valores.

</dd> <dt>

*pTimeStamp* \[ en, opcional\]
</dt> <dd>

Marca de tiempo de la base de datos. Si este parámetro es **NULL,** se usa la hora del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="remarks"></a>Comentarios

Se debe registrar una base de datos para poder usar cualquier otra función de SDB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




