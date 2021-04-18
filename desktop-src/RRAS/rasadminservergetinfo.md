---
title: Función RasAdminServerGetInfo (rassapi. h)
description: La función RasAdminServerGetInfo obtiene la configuración de servidor de un servidor RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo función RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680702"
---
# <a name="rasadminservergetinfo-function"></a>RasAdminServerGetInfo función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]

La función **RasAdminServerGetInfo** obtiene la configuración de servidor de un servidor RAS.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en **null** que especifica el nombre del servidor RAS de Windows NT/Windows 2000. Si este parámetro es **null**, la función devuelve información sobre el equipo local. Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.

</dd> <dt>

*pRasServer0* \[ enuncia\]
</dt> <dd>

Puntero a la estructura del [**servidor de Ras \_ \_ 0**](ras-server-0-str.md) que recibe el número de puertos configurados en el servidor, el número de puertos actualmente en uso y el número de versión del servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error. Los códigos de error posibles incluyen los devueltos por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para la función [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) . No hay información de error extendida para esta función; no llame a **GetLastError**.

## <a name="remarks"></a>Observaciones

Para enumerar todos los servidores RAS de un dominio, llame a la función [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) y especifique el \_ tipo VP \_ para el parámetro *ServerType* .

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

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**\_Servidor RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

