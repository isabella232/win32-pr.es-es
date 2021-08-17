---
title: Función RasAdminUserGetInfo (Rassapi.h)
description: La función RasAdminUserGetInfo obtiene los permisos RAS y la información del número de teléfono de devolución de llamada para un usuario especificado.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RasAdminUserGetInfo, función RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4cda41447af832bd4ae04a14c6f8038fee4b61a17ac98c919c0b085261b242d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788704"
---
# <a name="rasadminusergetinfo-function"></a>Función RasAdminUserGetInfo

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminUserGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)\]

La **función RasAdminUserGetInfo obtiene** los permisos RAS y la información del número de teléfono de devolución de llamada para un usuario especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszUserAccountServer* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del controlador de dominio principal o de copia de seguridad que tiene la base de datos de la cuenta de usuario. Use la [**función RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener este nombre de servidor.

</dd> <dt>

*lpszUser* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del usuario para el que se obtiene información de RAS.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Puntero a la [**estructura \_ RAS USER \_ 0**](ras-user-0-str.md) que recibe los datos RAS del usuario especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser el código de error siguiente.



| Value                                                                                            | Significado                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl> | Memoria insuficiente para realizar esta función.<br/> |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| Archivo DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funciones de administración del servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**USUARIO \_ RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

