---
title: Función RasAdminPortGetInfo (rassapi. h)
description: La función RasAdminPortGetInfo recupera información acerca de un puerto específico en un servidor especificado.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo función RAS
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
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680703"
---
# <a name="rasadminportgetinfo-function"></a>RasAdminPortGetInfo función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]

La función **RasAdminPortGetInfo** recupera información acerca de un puerto específico en un servidor especificado.

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

*lpszServer* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS. Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el servidor.

</dd> <dt>

*pRasPort1* \[ enuncia\]
</dt> <dd>

Puntero a la estructura del [**Puerto de Ras \_ \_ 1**](ras-port-1-str.md) que la función rellena con información sobre el estado del puerto.

</dd> <dt>

*pRasStats* \[ enuncia\]
</dt> <dd>

Puntero a la estructura de [**\_ \_ estadísticas del puerto ras**](ras-port-statistics-str.md) que la función rellena con estadísticas sobre el puerto.

</dd> <dt>

*ppRasParams* \[ enuncia\]
</dt> <dd>

Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras de [**\_ parámetros de Ras**](ras-parameters-str.md) . Cada estructura contiene el nombre de una clave específica del medio, como MAXCONNECTBPS, y su valor asociado. Cuando la aplicación haya finalizado con esta memoria, libere llamando a la función [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.



| Value                                                                                                     | Significado                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ no existe el desarrollador de errores \_**</dt> </dl>     | El puerto especificado no es válido.<br/>                                        |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl> | Memoria insuficiente para asignar un búfer para la matriz *ppRasParams* .<br/> |



 

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

[**parámetros de RAS \_**](ras-parameters-str.md)
</dt> <dt>

[**\_Puerto ras \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_estadísticas de Puerto ras \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

