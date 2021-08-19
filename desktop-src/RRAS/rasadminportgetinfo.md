---
title: Función RasAdminPortGetInfo (Rassapi.h)
description: La función RasAdminPortGetInfo recupera información sobre un puerto especificado en un servidor especificado.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo, función RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e633b663e9c4b35810585a2ac738c79ae2d39be06d7b91be0df75fd0455a5213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028515"
---
# <a name="rasadminportgetinfo-function"></a>Función RasAdminPortGetInfo

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminPortGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)\]

La **función RasAdminPortGetInfo** recupera información sobre un puerto especificado en un servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del servidor RAS. Especifique el nombre con caracteres iniciales \\ \\ "", con el formato: \\ \\ *nombreServidor*.

</dd> <dt>

*lpszPort* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del puerto en el servidor.

</dd> <dt>

*pRasPort1* \[ out\]
</dt> <dd>

Puntero a la [**estructura \_ RAS PORT \_ 1**](ras-port-1-str.md) que la función rellena con información sobre el estado del puerto.

</dd> <dt>

*pRasStats* \[ out\]
</dt> <dd>

Puntero a la [**estructura \_ RAS PORT \_ STATISTICS**](ras-port-statistics-str.md) que la función rellena con estadísticas sobre el puerto.

</dd> <dt>

*ppRasParams* \[ out\]
</dt> <dd>

Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras [**\_ DE PARÁMETROS RAS.**](ras-parameters-str.md) Cada estructura contiene el nombre de una clave específica del medio, como MAXCONNECTBPS, y su valor asociado. Cuando la aplicación termine con esta memoria, desconéctela mediante una llamada a la [**función RasAdminFreeBuffer.**](rasadminfreebuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Value                                                                                                     | Significado                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ DEV \_ NOT \_ EXIST**</dt> </dl>     | El puerto especificado no es válido.<br/>                                        |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl> | Memoria insuficiente para asignar un búfer para la *matriz ppRasParams.*<br/> |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

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

[**PARÁMETROS \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**PUERTO \_ \_ RAS 1**](ras-port-1-str.md)
</dt> <dt>

[**ESTADÍSTICAS \_ DE \_ PUERTO RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

