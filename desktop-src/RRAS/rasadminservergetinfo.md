---
title: Función RasAdminServerGetInfo (Rassapi.h)
description: La función RasAdminServerGetInfo obtiene la configuración del servidor de un servidor RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo, función RAS
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
ms.openlocfilehash: 1f6f83f7310700e774692d876bda979343da80aa45ea8012bf187e50f0af67bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028455"
---
# <a name="rasadminservergetinfo-function"></a>Función RasAdminServerGetInfo

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminServerGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo)\]

La **función RasAdminServerGetInfo** obtiene la configuración del servidor de un servidor RAS.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en **NULL** que especifica el nombre del Windows NT/Windows 2000 RAS. Si este parámetro es **NULL,** la función devuelve información sobre el equipo local. Especifique el nombre con caracteres iniciales \\ \\ "", con el formato: \\ \\ *nombreServidor*.

</dd> <dt>

*pRasServer0* \[ out\]
</dt> <dd>

Puntero a la [**estructura RAS \_ SERVER \_ 0**](ras-server-0-str.md) que recibe el número de puertos configurados en el servidor, el número de puertos actualmente en uso y el número de versión del servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error. Los códigos de error posibles incluyen los devueltos [**por GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para [**la función CallNamedPipe.**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) No hay ninguna información de error extendida para esta función; no llame a **GetLastError.**

## <a name="remarks"></a>Comentarios

Para enumerar todos los servidores RAS de un dominio, llame a la función [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) y especifique SV \_ TYPE \_ DIALIN para el *parámetro servertype.*

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

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**RAS \_ SERVER \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

