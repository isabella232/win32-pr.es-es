---
title: Función RasAdminPortClearStatistics (rassapi. h)
description: La función RasAdminPortClearStatistics restablece los contadores que representan las diversas estadísticas indicadas por la función RasAdminPortGetInfo en la \_ estructura de estadísticas del puerto ras \_ . Los contadores se restablecen a cero y comienzan a acumularse.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics función RAS
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
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649805"
---
# <a name="rasadminportclearstatistics-function"></a>RasAdminPortClearStatistics función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]

La función **RasAdminPortClearStatistics** restablece los contadores que representan las diversas estadísticas indicadas por la función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) en la estructura de [**\_ \_ estadísticas del puerto ras**](ras-port-statistics-str.md) . Los contadores se restablecen a cero y comienzan a acumularse.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS. Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.



| Value                                                                                                 | Significado                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ \_ no existe el desarrollador de errores \_**</dt> </dl> | El puerto especificado no es válido.<br/> |



 

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

La función **RasAdminPortClearStatistics** borra las estadísticas del servidor, no localmente dentro de la aplicación que realiza la llamada. Esto significa que las estadísticas también se restablecen para cualquier otra aplicación que esté supervisando el puerto especificado.

Si el puerto *lpszPort* forma parte de una conexión Multilink, **RasAdminPortClearStatistics** restablece las estadísticas para el puerto especificado, la función también restablece las estadísticas acumuladas de la conexión multivínculo. Sin embargo, la función no afecta a las estadísticas individuales de otros puertos que forman parte de la conexión de multivínculo.

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

[**\_estadísticas de Puerto ras \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

