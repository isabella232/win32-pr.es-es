---
description: Anula el registro de la base de datos especificada, de modo que ya no está disponible.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496091"
---
# <a name="sdbunregisterdatabase-function"></a>SdbUnregisterDatabase función)

Anula el registro de la base de datos especificada, de modo que ya no está disponible.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguidDB* \[ de\]
</dt> <dd>

GUID de la base de datos. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




