---
title: Función RasAdminPortEnum (rassapi. h)
description: La función RasAdminPortEnum enumera todos los puertos en el servidor RAS especificado. Para cada puerto del servidor, la función devuelve la estructura del \_ Puerto ras \_ 0 que contiene información sobre el puerto.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum función RAS
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
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649804"
---
# <a name="rasadminportenum-function"></a>RasAdminPortEnum función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]

La función **RasAdminPortEnum** enumera todos los puertos en el servidor RAS especificado. Para cada puerto del servidor, la función devuelve la estructura [**del \_ Puerto ras \_ 0**](ras-port-0-str.md) que contiene información sobre el puerto.

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

*lpszServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS. Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.

</dd> <dt>

*ppRasPort0* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un puntero a un búfer que contiene una matriz de estructuras del [**\_ Puerto \_ 0 de Ras**](ras-port-0-str.md) . Cuando la aplicación haya finalizado con la memoria, libere mediante una llamada a la función [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> <dt>

*pcEntriesRead* \[ enuncia\]
</dt> <dd>

Puntero a una variable de 16 bits que recibe el número total de estructuras de [**\_ Puerto ras \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) devueltas en la matriz *ppRasPort0* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.



| Value                                                                                             | Significado                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | No se pudo enumerar ningún puerto. Esto puede deberse a que todos los puertos configurados en el servidor se están usando actualmente para el marcado.<br/> |



 

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
</dt> <dt>

[**\_Puerto ras \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

