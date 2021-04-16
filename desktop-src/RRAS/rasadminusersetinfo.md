---
title: Función RasAdminUserSetInfo (rassapi. h)
description: La función RasAdminUserSetInfo establece los permisos RAS y el número de teléfono de devolución de llamada para un usuario especificado.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo función RAS
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649815"
---
# <a name="rasadminusersetinfo-function"></a>RasAdminUserSetInfo función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]

La función **RasAdminUserSetInfo** establece los permisos ras y el número de teléfono de devolución de llamada para un usuario especificado.

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

*lpszUserAccountServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del controlador de dominio principal o de reserva que tiene la base de datos de cuentas de usuario. Use la función [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener este nombre de servidor.

</dd> <dt>

*lpszUser* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del usuario para el que se va a establecer información de RAS.

</dd> <dt>

*pRasUser0* \[ de\]
</dt> <dd>

Puntero a la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) que especifica los nuevos datos ras para el usuario especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Value                                                                                                           | Descripción                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR de \_ datos no válidos \_**</dt> </dl>             | El búfer *pRasUser0* contiene datos no válidos.<br/>                                        |
| <dl> <dt>**ERROR \_ de \_ número de devolución de llamada no válido \_**</dt> </dl> | El número de devolución de llamada especificado en el búfer *pRasUser0* contiene caracteres no válidos.<br/> |
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl>               | Memoria insuficiente para realizar esta función.<br/>                                        |



 

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Al establecer los permisos RAS para un usuario, el miembro **bfPrivilege** de la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) debe especificar al menos una de las marcas de devolución de llamada. Por ejemplo, para establecer los privilegios de un usuario para permitir el privilegio de acceso telefónico pero ningún privilegio de devolución de llamada, establezca **bfPrivilege** en RASPRIV \_ DialinPrivilege \| RASPRIV \_ nocallback.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/> | Windows 2000 Server<br/>                                                         |
| Encabezado<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| Archivo DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funciones de administración del servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**Usuario de RAS \_ \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

