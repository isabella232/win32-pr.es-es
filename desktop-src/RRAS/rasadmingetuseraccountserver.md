---
title: Función RasAdminGetUserAccountServer (rassapi. h)
description: La función RasAdminGetUserAccountServer recupera el nombre del servidor que tiene la base de datos de cuentas de usuario. Use el nombre de servidor devuelto en las funciones RasAdminUserGetInfo y RasAdminUserSetInfo para obtener o establecer información sobre un usuario especificado.
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
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679552"
---
# <a name="rasadmingetuseraccountserver-function"></a>RasAdminGetUserAccountServer función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]

La función **RasAdminGetUserAccountServer** recupera el nombre del servidor que tiene la base de datos de cuentas de usuario. Use el nombre de servidor devuelto en las funciones [**RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obtener o establecer información sobre un usuario especificado.

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

*lpszDomain* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en **null** que especifica el nombre del dominio al que pertenece el servidor RAS. Este parámetro es **null** para las aplicaciones de administración de ras que se ejecutan en estaciones de trabajo o servidores que no son miembros de un dominio. Si este parámetro es **null**, el parámetro *lpszServer* no debe ser **null**.

</dd> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en **null** que especifica el nombre del servidor RAS. Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*. Este parámetro puede ser **null** si el parámetro *LpszDomain* no es **null**.

</dd> <dt>

*lpszUserAccountServer* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe una cadena Unicode terminada en **null** que especifica el nombre de un controlador de dominio que tiene la base de datos de cuentas de usuario. El búfer debe ser lo suficientemente grande como para contener el nombre del servidor (más o más). La función antepone el nombre del servidor devuelto con los " \\ \\ " caracteres iniciales, con el formato: \\ \\ *ServerName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.



| Value                                                                                                    | Significado                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl> | Tanto *lpszDomain* como *lpszServer* son **null**.<br/> |



 

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

La función **RasAdminGetUserAccountServer** obtiene el nombre del servidor con la base de datos de cuentas de usuario. Esta función requiere el nombre del servidor RAS o el nombre del dominio en el que reside el servidor RAS.

El parámetro *lpszDomain* debe especificar un nombre de dominio válido. Este parámetro es **null** para las aplicaciones de administración de ras que se ejecutan en servidores que no son miembros de un dominio (por ejemplo, el servidor está en su propio grupo de trabajo). En este caso, el parámetro *lpszServer* debe especificar el nombre del servidor. Para obtener el nombre del servidor, llame a la función [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) . Asegúrese de anteponer los caracteres "" al nombre del servidor \\ \\ .

Si el nombre del servidor especificado por *lpszServer* es un servidor independiente (es decir, el servidor o la estación de trabajo no es miembro de un dominio), se devuelve el nombre del servidor en el búfer *lpszUserAccountServer* .

A continuación, utilice el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios en la base de datos de cuentas de usuario.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

