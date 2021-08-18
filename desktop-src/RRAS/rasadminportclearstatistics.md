---
title: Función RasAdminPortClearStatistics (Rassapi.h)
description: La función RasAdminPortClearStatistics restablece los contadores que representan las distintas estadísticas notificadas por la función RasAdminPortGetInfo en la estructura \_ RAS PORT \_ STATISTICS. Los contadores se restablecen a cero y comienzan a acumularse.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics, función RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da7d17516e7dd7708821a7c60c2d93db913f25c38471524367ae96494e41f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788992"
---
# <a name="rasadminportclearstatistics-function"></a>Función RasAdminPortClearStatistics

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminPortClearStats.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)\]

La **función RasAdminPortClearStatistics** restablece los contadores que representan las distintas estadísticas notificadas por la función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) en la estructura [**RAS PORT \_ \_ STATISTICS.**](ras-port-statistics-str.md) Los contadores se restablecen a cero y comienzan a acumularse.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del servidor RAS. Especifique el nombre con caracteres " \\ \\ " " iniciales, con el formato: \\ \\ *servername*.

</dd> <dt>

*lpszPort* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del puerto en el servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.



| Value                                                                                                 | Significado                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**ERROR \_ DEV \_ NOT \_ EXIST**</dt> </dl> | El puerto especificado no es válido.<br/> |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

La **función RasAdminPortClearStatistics** borra las estadísticas del servidor, no localmente dentro de la aplicación que realiza la llamada. Esto significa que las estadísticas también se restablecen para cualquier otra aplicación que esté supervisando el puerto especificado.

Si el puerto *lpszPort* forma parte de una conexión de varios vínculos, **RasAdminPortClearStatistics** restablece las estadísticas del puerto especificado, la función también restablece las estadísticas acumulativas para la conexión de varios vínculos. Sin embargo, la función no afecta a las estadísticas individuales de otros puertos que forman parte de la conexión de varios vínculos.

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

[**ESTADÍSTICAS \_ DE \_ PUERTO RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

