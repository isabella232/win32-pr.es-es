---
title: Función RasAdminGetErrorString (Rassapi.h)
description: La función RasAdminGetErrorString recupera una cadena de mensaje que corresponde a un código de error RAS devuelto por una de las funciones de administración del servidor RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString, función RAS
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
ms.openlocfilehash: a45c768daef7c889351744c5e046c83f4de7e220f59752c1db271067efb68366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028611"
---
# <a name="rasadmingeterrorstring-function"></a>Función RasAdminGetErrorString

\[Esta función solo se proporciona por compatibilidad con versiones anteriores Windows NT Server 4.0. Devuelve ERROR \_ CALL \_ NOT \_ IMPLEMENTED en Windows Server 2003. Las aplicaciones deben usar [**la función MprAdminGetErrorString.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)\]

La **función RasAdminGetErrorString** recupera una cadena de mensaje que corresponde a un código de error RAS devuelto por una de las funciones de administración del servidor RAS (RasAdmin). Estas cadenas de mensaje se recuperan de la Rasmsg.dll que se instala como parte de RAS.

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

*ResourceId* \[ En\]
</dt> <dd>

Especifica un código de error devuelto por una de las funciones RasAdmin. Este valor debe estar en el intervalo de códigos de error de RASBASE a RASBASEEND. Se definen en Raserror.h.

</dd> <dt>

*lpszString* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el mensaje de error que corresponde al código de error especificado.

</dd> <dt>

*InBufSize* \[ En\]
</dt> <dd>

Especifica el tamaño, en caracteres, del *búfer lpszString.* Los mensajes de error suelen tener 80 caracteres o menos. un tamaño de búfer de 512 caracteres siempre es adecuado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error. Este valor puede ser un último valor de error establecido por las [**funciones LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)o [**LoadString;**](/windows/win32/api/winuser/nf-winuser-loadstringa) o puede ser uno de los siguientes códigos de error.



| Value                                                                                                      | Significado                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>   | Los *parámetros ResourceId* o *lpszString* no son válidos.<br/>      |
| <dl> <dt>**ERROR \_ BÚFER \_ INSUFICIENTE**</dt> </dl> | El tamaño especificado por el *parámetro InBufSize* es demasiado pequeño.<br/> |



 

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

Las funciones RasAdmin pueden devolver códigos de error que no están en el intervalo admitido por la **función RasAdminGetErrorString.** Por ejemplo, las funciones RasAdmin pueden devolver códigos de error definidos en Lmerr.h y Winerror.h. Antes de **llamar a RasAdminGetErrorString,** compruebe que el código de error está en el intervalo RASBASE a RASBASEEND, tal como se define en Raserror.h.

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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

