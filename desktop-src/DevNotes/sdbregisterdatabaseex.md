---
description: Registra la base de datos especificada.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx función)
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
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538661"
---
# <a name="sdbregisterdatabaseex-function"></a>SdbRegisterDatabaseEx función)

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

*pszDatabasePath* \[ de\]
</dt> <dd>

Ruta de acceso de la base de datos. Este parámetro no puede ser **null**.

</dd> <dt>

*dwDatabaseType* \[ de\]
</dt> <dd>

El tipo de base de datos. Vea [tipos de base de datos de corrección de compatibilidad](shim-database-types.md) para obtener una lista de valores.

</dd> <dt>

*pTimeStamp* \[ en, opcional\]
</dt> <dd>

Marca de tiempo para la base de datos. Si este parámetro es **null**, se utiliza la hora del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="remarks"></a>Observaciones

Se debe registrar una base de datos antes de poder usar cualquier otra función SDB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




