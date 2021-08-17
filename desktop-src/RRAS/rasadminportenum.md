---
title: Función RasAdminPortEnum (Rassapi.h)
description: La función RasAdminPortEnum enumera todos los puertos del servidor RAS especificado. Para cada puerto del servidor, la función devuelve la estructura RAS \_ PORT \_ 0 que contiene información sobre el puerto.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum, función RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b86cbf78a47a62c8d98799ac18adf987cbe623dc92e703537c54b54bf892a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788877"
---
# <a name="rasadminportenum-function"></a>Función RasAdminPortEnum

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminPortEnum.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)\]

La **función RasAdminPortEnum** enumera todos los puertos del servidor RAS especificado. Para cada puerto del servidor, la función devuelve la [**estructura RAS \_ PORT \_ 0**](ras-port-0-str.md) que contiene información sobre el puerto.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del servidor RAS. Especifique el nombre con caracteres " \\ \\ " " iniciales, con el formato: \\ \\ *servername*.

</dd> <dt>

*ppRasPort0* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un puntero a un búfer que contiene una matriz de estructuras [**\_ RAS PORT \_ 0.**](ras-port-0-str.md) Cuando la aplicación haya terminado con la memoria, desconéctela mediante una llamada a la [**función RasAdminFreeBuffer.**](rasadminfreebuffer.md)

</dd> <dt>

*pcEntriesRead* \[ out\]
</dt> <dd>

Puntero a una variable de 16 bits que recibe el número total de estructuras [**\_ RAS PORT \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) devueltas en la matriz *ppRasPort0.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.



| Value                                                                                             | Significado                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | No se pudo enumerar ningún puerto. Esto podría deberse a que todos los puertos configurados en el servidor se usan actualmente para marcar hacia fuera.<br/> |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**PUERTO \_ \_ RAS 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

