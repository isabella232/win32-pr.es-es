---
title: Función RasAdminPortDisconnect (rassapi. h)
description: La función RasAdminPortDisconnect desconecta un puerto que está actualmente en uso.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect función RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680704"
---
# <a name="rasadminportdisconnect-function"></a>RasAdminPortDisconnect función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]

La función **RasAdminPortDisconnect** desconecta un puerto que está actualmente en uso.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS de Windows NT/Windows 2000. Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Value                                                                                               | Significado                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ Puerto no válido**</dt> </dl> | El puerto especificado no es válido.<br/>    |
| <dl> <dt>**NERR \_ UserNotFound**</dt> </dl>   | El puerto no está actualmente en uso.<br/> |



 

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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
</dt> </dl>

 

