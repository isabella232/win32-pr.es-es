---
title: Función RasAdminUserSetInfo (Rassapi.h)
description: La función RasAdminUserSetInfo establece los permisos RAS y el número de teléfono de de vuelta para un usuario especificado.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo, función RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073867"
---
# <a name="rasadminusersetinfo-function"></a>Función RasAdminUserSetInfo

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminUserSetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)\]

La **función RasAdminUserSetInfo** establece los permisos RAS y el número de teléfono de de vuelta para un usuario especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
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

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del usuario para el que se va a establecer la información ras.

</dd> <dt>

*pRasUser0* \[ En\]
</dt> <dd>

Puntero a la [**estructura \_ RAS USER \_ 0**](ras-user-0-str.md) que especifica los nuevos datos RAS para el usuario especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Value                                                                                                           | Descripción                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ DATOS NO \_ VÁLIDOS**</dt> </dl>             | El *búfer pRasUser0* contiene datos no válidos.<br/>                                        |
| <dl> <dt>**ERROR \_ NÚMERO DE \_ DEVOLUCIÓN DE LLAMADA NO \_ VÁLIDO**</dt> </dl> | El número de devolución de llamada especificado en el *búfer pRasUser0* contiene caracteres no válidos.<br/> |
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl>               | Memoria insuficiente para realizar esta función.<br/>                                        |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Al establecer los permisos ras para un usuario, el miembro **bfPrivilege** de la estructura [**\_ USER \_ 0**](ras-user-0-str.md) de RAS debe especificar al menos una de las marcas de dedo de llamada. Por ejemplo, para establecer los privilegios de un usuario para permitir privilegios de acceso telefónico pero sin privilegios de devolución de llamada, establezca **bfPrivilege** en RASPRIV \_ DialinPrivilege \| RASPRIV \_ NoCallback.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/> | Windows 2000 Server<br/>                                                         |
| Encabezado<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| Archivo DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funciones de administración del servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**USUARIO \_ RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

