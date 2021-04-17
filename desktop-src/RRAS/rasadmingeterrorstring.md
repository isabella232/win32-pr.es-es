---
title: Función RasAdminGetErrorString (rassapi. h)
description: La función RasAdminGetErrorString recupera una cadena de mensaje que corresponde a un código de error de RAS devuelto por una de las funciones de administración del servidor RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString función RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653605"
---
# <a name="rasadmingeterrorstring-function"></a>RasAdminGetErrorString función)

\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0. Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003. Las aplicaciones deben usar la función [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]

La función **RasAdminGetErrorString** recupera una cadena de mensaje que corresponde a un código de error de Ras devuelto por una de las funciones de administración del servidor RAS (RasAdmin). Estas cadenas de mensaje se recuperan de la Rasmsg.dll que se instala como parte de RAS.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResourceId* \[ de\]
</dt> <dd>

Especifica un código de error devuelto por una de las funciones de RasAdmin. Este valor debe estar en el intervalo de códigos de error de RASBASE a RASBASEEND. Se definen en Raserror. h.

</dd> <dt>

*lpszString* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe el mensaje de error correspondiente al código de error especificado.

</dd> <dt>

*InBufSize* \[ de\]
</dt> <dd>

Especifica el tamaño, en caracteres, del búfer de *lpszString* . Los mensajes de error suelen ser de 80 caracteres o menos; un tamaño de búfer de 512 caracteres siempre es adecuado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error. Este valor puede ser el último valor de error establecido por las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)o [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) ; o puede ser uno de los siguientes códigos de error.



| Value                                                                                                      | Significado                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>   | Los parámetros *ResourceId* o *lpszString* no son válidos.<br/>      |
| <dl> <dt>**ERROR \_ de \_ búfer insuficiente**</dt> </dl> | El tamaño especificado por el parámetro *InBufSize* es demasiado pequeño.<br/> |



 

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Las funciones RasAdmin pueden devolver códigos de error que no están en el intervalo admitido por la función **RasAdminGetErrorString** . Por ejemplo, las funciones RasAdmin pueden devolver códigos de error que se definen en Lmerr. h y Winerror. h. Antes de llamar a **RasAdminGetErrorString**, compruebe que el código de error está en el intervalo RASBASE a RASBASEEND, tal y como se define en Raserror. h.

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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**Fall**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

