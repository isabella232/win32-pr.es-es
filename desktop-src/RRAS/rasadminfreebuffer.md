---
title: Función RasAdminFreeBuffer (rassapi. h)
description: La función RasAdminFreeBuffer libera la memoria asignada por RAS en nombre del autor de la llamada.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RasAdminFreeBuffer función RAS
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681303"
---
# <a name="rasadminfreebuffer-function"></a>RasAdminFreeBuffer función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]

La función **RasAdminFreeBuffer** libera la memoria asignada por ras en nombre del autor de la llamada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Puntero* \[ de de\]
</dt> <dd>

Puntero al búfer que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.



| Value                                                                                                    | Significado                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl> | El parámetro de *puntero* no es válido.<br/> |



 

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Use la función **RasAdminFreeBuffer** para liberar los búferes asignados por las funciones [**RasAdminPortEnum**](rasadminportenum.md) y [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .

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

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

