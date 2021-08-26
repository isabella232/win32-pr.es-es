---
title: Función RasAdminGetUserAccountServer (Rassapi.h)
description: La función RasAdminGetUserAccountServer recupera el nombre del servidor que tiene la base de datos de la cuenta de usuario. Use el nombre de servidor devuelto en las funciones RasAdminUserGetInfo y RasAdminUserSetInfo para obtener o establecer información sobre un usuario especificado.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer función RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2ac4052ad4638c3e0e2483adb68857f4c2b670322434107d93100b6a177855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028545"
---
# <a name="rasadmingetuseraccountserver-function"></a>Función RasAdminGetUserAccountServer

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminGetPDCServer.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)\]

La **función RasAdminGetUserAccountServer** recupera el nombre del servidor que tiene la base de datos de la cuenta de usuario. Use el nombre de servidor devuelto en las funciones [**RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obtener o establecer información sobre un usuario especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszDomain* \[ En\]
</dt> <dd>

Puntero a una **cadena** Unicode terminada en NULL que especifica el nombre del dominio al que pertenece el servidor RAS. Este parámetro es **NULL para** las aplicaciones de administración ras que se ejecutan en estaciones de trabajo o servidores que no son miembros de un dominio. Si este parámetro es **NULL,** el *parámetro lpszServer* debe ser distinto de **NULL.**

</dd> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Puntero a una **cadena** Unicode terminada en NULL que especifica el nombre del servidor RAS. Especifique el nombre con caracteres iniciales \\ \\ "", con el formato: \\ \\ *nombreServidor*. Este parámetro puede ser **NULL si** el *parámetro lpszDomain* no es **NULL.**

</dd> <dt>

*lpszUserAccountServer* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe **una** cadena Unicode terminada en NULL que especifica el nombre de un controlador de dominio que tiene la base de datos de la cuenta de usuario. El búfer debe ser lo suficientemente grande como para contener el nombre del servidor (LAN +1). La función prefida el nombre del servidor devuelto con caracteres \\ \\ iniciales "", con el formato: \\ \\ *nombreServidor*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser el código de error siguiente.



| Value                                                                                                    | Significado                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl> | Tanto *lpszDomain* como *lpszServer* son **NULL.**<br/> |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

La **función RasAdminGetUserAccountServer** obtiene el nombre del servidor con la base de datos de cuentas de usuario. Esta función requiere el nombre del servidor RAS o el nombre del dominio en el que reside el servidor RAS.

El *parámetro lpszDomain* debe especificar un nombre de dominio válido. Este parámetro es **NULL para** las aplicaciones de administración ras que se ejecutan en servidores que no son miembros de un dominio (por ejemplo, el servidor está en su propio grupo de trabajo). En este caso, el *parámetro lpszServer* debe especificar el nombre del servidor. Para obtener el nombre del servidor, llame a [**la función GetComputerName.**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) Asegúrese de antefir el nombre del servidor con los caracteres \\ \\ "".

Si el nombre de servidor especificado por *lpszServer* es un servidor independiente (es decir, el servidor o la estación de trabajo no es miembro de un dominio), el propio nombre de servidor se devuelve en el búfer *lpszUserAccountServer.*

A continuación, use el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios de la base de datos de cuentas de usuario.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

